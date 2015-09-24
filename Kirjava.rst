= Robot Seguidor de Linea '' Kirjava '' =
prueba

Desarrollador:

 * [[OchoaDario|OCHOA, Darío Martín E.]]

<<TableOfContents()>>

== Introducción ==
Un Robot Seguidor de Linea (RSL) es un robot que sigue una linea marcada en el piso, pudiendo ser esta blanca sobre fondo negro(nuestro caso) o negra sobre fondo blanco. Si bien existen multitud de posibilidades para su fabricación la mayoría posee ciertos elementos comunes:

 * '''Sensores''': Encargados de recolectar datos del exterior para diferenciar la linea del fondo.
 * '''Etapa de Control''': Es la parte del robot que se encargará de tomar las decisiones con la información proporcionada por los sensores y determinará el funcionamiento o no de los actuadores. El prosecsamiento de datos y toma de decisiones puede ser realizado tanto por microcontroladores programables, por elementos digitales discretos o simplemente de forma analógica.
 * '''Etapa de Potencia''': Se encarga de adaptar los niveles de tensión y corriente para poder conectar la etapa de control a los actuadores.
 * '''Actuadores''': Los actuadores se encargaran de los movimientos necesarios del robot para que este pueda cumplir con su objetivo de seguir la linea marcada. Generalmente, variedad de motores con diferentes agregados mecánicos.
 * '''Fuente de Energía''': Es la fuente de alimentación del RSL, generalmente baterías.

{{attachment:bloques.png||width="400"}}

== Objetivos ==
El objetivo de este proyecto es el desarrollo de un RSL sencillo y económico pero aún así con un desempeño lo suficientemente aceptable para las competencias. Con esas premisas se decidió por no utilizar microcontrolador para la Etapa de Control, puesto que a pesar de que en la actualidad estos no son costosos, para utilizarlos es necesario una infraestructura extra(por ejemplo: soporte, programador, PC). El control de manera analógica puede ser fiable, pero a baja velocidad.

Por lo cual se de optó por un nivel intermedio entre control por uC y control analógico, lo que es un control digital, pero con componentes discretos para los cuales no es necesario programación alguna(amplificadores operacionales, compuertas digitales, transistores en su zona de Corte/Saturación).

== Desarrollo ==
=== Sensores ===
Para censar la linea a seguir se utilizan 2 fototransitores con 2 LEDs infrarojos. Para el acondicionamiento de señal se utiliza un Amplificador Operacional dispuesto como Comparador utilizando una resistencia variable para polarizarlo a fin de poder configurar a Kirjava según la luz del ambiente y la pista. {{attachment:sensores2.png||width="600"}}

==== Funcionamiento ====
El funcionamiento se basa en el trío LED-Fototransistor-Comparador. Tanto el Led como el fototransitor se colocan orientados hacia la pista, mientras el haz de luz incida sobre la linea blanca el fototransitor permanecerá cerrado, puesto que la luz reflejada exitara la Base cerrando el fototransistor, con lo cual un valor cercano a los 0v llegará al pin v- del comparador(Amplificador Operacional configurado como comparador). El comparador comparará este valor con el valor de referencia generado por la resistencia variable dando a la salida un 1 (en caso que el valor en v- sea menor al valor de referencia) o un 0 (cuando el valor de v- sea mayor al valor de referencia). Por otro lado, cuando el haz de luz del LED incida sobre el área negra el fototransistor permanecerá abierto, con lo cual un valor cercano a la tensión de alimentación (9v) llegará al pin v- del comparador, reaccionando este de igual forma que en el caso anterior. (si v- es menor al valor de referencia entonces la salida será un 1, y un 0 en el caso que v- sea mayor al valor de referencia) Las de salidas de ambos comparadores se conecta a las entradas de la '''Etapa de Control'''

(agregar imagen de disposición de LEDs y fototransitores)

'''Nota:'''El valor de referencia que se  pone en el pin v+ de ambos comparadores tiene por objetivo poder adaptar a Kirjava para ambientes con diferentes intensidades de luz y pistas con distintas características reflectivas. Este valor se genera con una resistencia variable dispuesta como divisor de tensión.

=== Etapa de Control ===
Esta etapa se encarga de decidir el funcionamiento de los '''actuadores''' segun los valores que vienen desde la etapa de '''sensores'''. Se basa en un circuito combinacional digital con dos entradas(Izquierda y Derecha, salidas de los comparadores) y dos salidas, una para girar hacia la izquierda y la otra para girar a la derecha.

==== Funcionamiento ====
El funcionamiento se basa, como todo circuito digital combinacional, en los distintos estados de las entradas, los cuales explicaremos a continuación para luego plasmarlos en el circuito con compuertas.

 * Mientras las entradas '''Izquierda''' y '''Derecha''' sean '''1''' significa que Kirjava esta alineado con la linea blanca que debe seguir por lo tanto no debería girar hacia ningún lado.
 * Si '''Izquierda''' es '''0''' y '''Derecha''' es '''1''', significa que Kirjava se salio de la linea blanca por la izquierda, por lo tanto debe girar hacia la '''Derecha'''
 * Si '''Derecha''' es '''0''' e '''Izquierda''' es '''1'''', significa que Kirjava se salio de la linea blanca por la derecha, por lo tanto debe girar hacia la '''Izquierda'''
 * Si tanto '''Derecha''' e '''Izquierda''' son '''0''' significa que Kirjava perdió totalmente la linea blanca.

Esto último puede ser un tanto complicado de entender, por lo tanto lo plasmaremos en una '''Tabla de Verdad''' para tratar de entenderlo de otra forma.
||||<#E0E0FF style="text-align:center">'''Entradas''' ||||<#E0E0FF style="text-align:center">'''Salidas''' ||
||<style="text-align:center">Izquierda ||<style="text-align:center">Derecha ||<style="text-align:center">giro hacia la Izquierda ||<style="text-align:center">Giro hacia la Derecha ||
||<style="text-align:center">0 ||<style="text-align:center">0 ||<style="text-align:center">0 ||<style="text-align:center">0 ||
||<style="text-align:center">0 ||<style="text-align:center">1 ||<style="text-align:center">0 ||<style="text-align:center">1 ||
||<style="text-align:center">1 ||<style="text-align:center">0 ||<style="text-align:center">1 ||<style="text-align:center">0 ||
||<style="text-align:center">1 ||<style="text-align:center">1 ||<style="text-align:center">0 ||<style="text-align:center">0 ||




resumiendo:

 * Giro hacia la Derecha solo debe activarse cuando Izquierda=0 y Derecha=1

 * Giro hacia la Izquierda solo debe activarse cuando Izquierda=1 y Derecha=0

 * En los otros casos tanto Giro hacia la Izquierda como hacia la derecha deben ser 0.

De esta manera se obtienen las Funciones Booleanas para cada una de las salidas, siendo:

'''Giro hacia la Derecha'''   = Izquierda' * Derecha

'''Giro hacia la Izquierda''' = Derecha' * Izquierda

Conociendo las funciones se puede armar el Circuito, el consta de dos integrados de compuertas:

 * 4069 Sextuple NOT
 * 4081 Cuadruple AND

{{attachment:procesamiento.png||width="600"}}

=== Etapa de Potencia ===
Esta etapa es simplemente un '''Puente H''' basado en las explicaciones de [[http://robots-argentina.com.ar/MotorCC_PuenteH.htm/|Control de motores de CC con Puente H]]. El interlok no es necesario ya que la '''Etapa de Control''' se encarga de que las señales no se superpongan.

==== Funcionamiento ====
La señal de '''Giro hacia la Derecha''' activa '''Q3''' y '''Q9''' con lo cual el motor gira en una dirección, y la señal de '''Giro hacia la Izquierda''' activa '''Q4''' y '''Q8''' y el motor girará en dirección contraria.

{{attachment:puenteH.png||width="600"}}

=== Actuadores ===
Kirjava consta de dos motores para encargarse de sus movimientos. Un motor para encargarse de la tracción y otro motor que se encarga de la dirección.

==== Funcionamiento ====
 * Motor Tracción: Este motor mueve ambas ruedas de tracción, funciona constantemente. En el futuro se podría aumentar un '''Control de Velocidad por PWM''', aunque este control esta en el esquemático no se implementó en el modelo actual.
 * Motor de Dirección: Este motor esta acoplado a  un tornillo sin fin el cual mueve un engranaje que esta unido a la rueda que controla la dirección. También tiene un brazo en el que al final se encuentran los sensores.

El tornillo sin fin hace girar el engranaje en un sentido o en el otro, dependiendo de los transistores que esten activados en ese momento.

{{attachment:tornillosinfin.gif||width="300"}} {{attachment:sistemadireccion.gif||width="200"}}


<<YouTube(id=uZXlh5CuTjQ)>>

----
[[RSL|Principal RSL]] | [[GruposRSL|Grupos RSL]]
