= Robot Seguidor de Linea '' Kirjava '' =
 
Desarrollador:
 * [[OchoaDario|OCHOA, Darío Martín E.]]

<<TableOfContents()>>
== Introducción ==

Un Robot Seguidor de Linea (RSL) es un robot que sigue una linea marcada en el piso, pudiendo ser esta blanca sobre fondo negro(nuestro caso) o negra sobre fondo blanco.
Si bien existen multitud de posibilidades para su fabricación la mayoría posee ciertos elementos comunes:
 * '''Sensores''': Encargados de recolectar datos del exterior para diferenciar la linea del fondo.
 * '''Procesadores de Datos''': Es la parte del robot que se encargará de tomar las decisiones con la información proporcionada por los sensores y determinará el funcionamiento o no de los actuadores. El prosecsamiento de datos y toma de decisiones puede ser realizado tanto por microcontroladores programables, por elementos digitales discretos o simplemente de forma analógica.
 * '''Actuadores''': Los actuadores se encargaran de los movimientos necesarios del robot para que este pueda cumplir con su objetivo de seguir la linea marcada. Generalmente, variedad de motores con diferentes agregados mecánicos.
 * '''Fuente de Energía''': Es la fuente de alimentación del RSL, generalmente baterías.

== Objetivos ==

El objetivo de este proyecto es el desarrollo de un RSL sencillo y económico pero aún así con un desempeño lo suficientemente aceptable para las competencias.
Con esas premisas se decidió por no utilizar microcontrolador para el procesamiento de datos, puesto que a pesar de que en la actualidad estos no son costosos, para utilizarlos es necesario una infraestructura extra(por ejemplo: soporte, programador, PC). El control de manera analógica puede ser fiable, pero a baja velocidad.

Por lo cual se de optó por un nivel intermedio entre control por uC y control analógico, lo que es un control digital, pero con componentes discretos para los cuales no es necesario programación alguna(amplificadores operacionales, compuertas digitales, transistores en su zona de Corte/Saturación).

== Desarrollo ==

=== Sensores ===
Para censar la linea a seguir se utilizan 2 fototransitores con 2 LEDs infrarojos. Para el acondicionamiento de señal se utiliza un Amplificador Operacional dispuesto como Comparador utilizando una resistencia variable para polarizarlo a fin de poder configurar a Kirjava según la luz del ambiente y la pista.
{{attachment:sensores.png||width="600"}}

==== Funcionamiento ====
El funcionamiento se basa en el trío LED-Fototransistor-Comparador.
Tanto el Led como el fototransitor se colocan orientados hacia la pista, mientras el haz de luz incida sobre la linea blanca el fototransitor permanecerá cerrado, puesto que la luz reflejada exitara la Base cerrando el fototransistor, con lo cual un valor cercano a los 0v llegará al pin v- del comparador(Amplificador Operacional configurado como comparador). El comparador comparará este valor con el valor de referencia generado por la resistencia variable dando a la salida un 1 (en caso que el valor en v- sea menor al valor de referencia) o un 0 (cuando el valor de v- sea mayor al valor de referencia).
Por otro lado, cuando el haz de luz del LED incida sobre el área negra el fototransistor permanecerá abierto, con lo cual un valor cercano a la tensión de alimentación (9v) llegará al pin v- del comparador, reaccionando este de igual forma que en el caso anterior. (si v- es menor al valor de referencia entonces la salida será un 1, y un 0 en el caso que v- sea mayor al valor de referencia)
Las de salidas de ambos comparadores se conecta a las entradas de la etapa de '''Procesamiento de Datos'''

(agregar imagen de disposición de LEDs y fototransitores)

'''Nota:'''El valor de referencia que se  pone en el pin v+ de ambos comparadores tiene por objetivo poder adaptar a Kirjava para ambientes con diferentes intensidades de luz y pistas con distintas características reflectivas. Este valor se genera con una resistencia variable dispuesta como divisor de tensión.


=== Procesamiento de Datos ===
Esta etapa se encarga de decidir el funcionamiento de los '''actuadores''' segun los valores que vienen desde la etapa de '''sensores'''. Se basa en un circuito combinacional digital con dos entradas(Izquierda y Derecha, salidas de los comparadores) y dos salidas, una para girar hacia la izquierda y la otra para girar a la derecha. 
==== Funcionamiento ====
El funcionamiento se basa, como todo circuito digital combinacional, en los distintos estados de las entradas, los cuales explicaremos a continuación para luego plasmarlos en el circuito con compuertas.

 * Mientras las entradas '''Izquierda''' y '''Derecha''' sean '''1''' significa que Kirjava esta alineado con la linea blanca que debe seguir por lo tanto no debería girar hacia ningún lado.
 * Si '''Izquierda''' es '''0''' y '''Derecha''' es '''1''', significa que Kirjava se salio de la linea blanca por la izquierda, por lo tanto debe girar hacia la '''Derecha'''
 * Si '''Derecha''' es '''0''' e '''Izquierda''' es '''1'''', significa que Kirjava se salio de la linea blanca por la derecha, por lo tanto debe girar hacia la '''Izquierda'''
 * Si tanto '''Derecha''' e '''Izquierda''' son '''0''' significa que Kirjava perdió totalmente la linea blanca.

Esto último puede ser un tanto complicado de entender, por lo tanto lo plasmaremos en una '''Tabla de Verdad''' para tratar de entenderlo de otra forma.

||||<style="background-color: #E0E0FF;"> '''Entradas'''||||<style="background-color: #E0E0FF;"> '''Salidas'''||
||<:> Izquierda          ||<:> Derecha                 ||<:> giro hacia la Izquierda ||<:> Giro hacia la Derecha ||
||<:>    0               ||<:>    0                    ||<:>          0              ||<:>           0           ||
||<:>    0               ||<:>    1                    ||<:>          0              ||<:>           1           ||
||<:>    1               ||<:>    0                    ||<:>          1              ||<:>           0           ||
||<:>    1               ||<:>    1                    ||<:>          0              ||<:>           1           ||



----
[[RSL | Principal RSL]] | [[GruposRSL | Grupos RSL]]
