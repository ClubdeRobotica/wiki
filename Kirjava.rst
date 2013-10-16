= Robot Seguidor de Linea '' Kirjava '' =
 
Desarrollador:
 * [[OchoaDario|OCHOA, Darío Martín E.]]

== Introducción ==

Un Robot Seguidor de Linea (RSL) es un robot que sigue una linea marcada en el piso, pudiendo ser esta blanca sobre fondo negro(nuestro caso) o negra sobre fondo blanco.
Si bien existen multitud de posibilidades para su fabricación la mayoría posee ciertos elementos comunes:
 a. '''Sensores''': Encargados de recolectar datos del exterior para diferenciar la linea del fondo.
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
Por otro lado, cuando el haz de luz del LED incida sobre el área negra el fototransistor permanecerá abiero, con lo cual un valor cercano a la tensión de alimentación (9v) llegará al pin v- del comparador, reaccionando este de igual forma que en el caso anterior. (si v- es menor al valor de referencia entonces la salida será un 1, y un 0 en el caso que v- sea mayor al valor de referencia)

'''Nota:'''El valor de referencia que se  pone en el pin v+ de ambos comparadores tiene por objetivo poder adaptar a Kirjava para ambientes con diferentes intensidades de luz y pistas con distintas características reflectivas. Este valor se genera con una resistencia variable dispuesta como divisor de tensión.


----
[[RSL | Principal RSL]] | [[GruposRSL | Grupos RSL]]
