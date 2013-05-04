= Robot Seguidor de Linea '' Kirjava '' =
 
Desarrollador:
 * OCHOA, Darío Martín E.

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
