<<TableOfContents()>>



En esta sección se especifica el Hardware utilizado en el proyecto.


==  Diagrama General ==

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:left">{{attachment:DiagramaARM.png||width="790"}}||

----
== Unidad de control ==





||<tablewidth="100%" tablestyle="text-align:center"50%  style="border:medium none; ;text-align:center">{{attachment:stellaris.jpg|Stellaris Launchpad|width="300"}}||<tablewidth="100%" tablestyle="text-align:center"50%  style="border:medium none; ;text-align:center">{{attachment:ARMLPC1768_versionWiki.png|Kit LPC1768|width="300"}}||


El control del VRTD está a cargo de un microcontrolador de la familia  [[http://es.wikipedia.org/wiki/Arquitectura_ARM.|ARM]](Advanced RISC Machines), el cual posee un núcleo de arquitectura [[http://es.wikipedia.org/wiki/RISC.|RISC]] (Reduced Instruction Set Computer), de 32 bits.

El microcontrolador utilizado es el LM4F120H5QR con núcleo  cortex-M4 de la firma [[http://es.wikipedia.org/wiki/Texas_Instruments|Texas Instruments]]

Este micro se encuentra montado sobre la placa de desarrollo [[http://www.ti.com/lit/ug/spmu289c/spmu289c.pdf|Stellaris Launchpad]] la cual posee, entre otras cosas, interfaz ICDI USB , conexión micro USB-B para depuración, conexión micro USB-B para usuario,cristal principal de 16 MHz . 

Para obtener un control mas preciso sobre la plataforma se decidió utilizar dos de las placas mencionadas para dividir las tareas y generar independencia en los servicios , de esta manera se evita perder el control total del equipo previniendo incidentes por  fallas eventuales. 


----
== Telemetría ==
La telemetría del VRTD  consta de x sensores encargados de obtener datos acerca de orientación,proximidad con objetos y distancia recorrida.Para ello subdividiremos esta sección en 3 bloques (Orientación,Proximidad y Distancia), los cuales constan de diversos tipos de sensores.

=== Orientación ===

Para la orientación se utilizan sensores de efecto hall, con los cuales, a partir de las mediciones sobre el campo magnético terrestre , podemos conocer hacia donde está el NORTE de la plataforma.


=== Proximidad ===

Para evitar colisiones con objetos del entorno se utilizan sensores de ultrasonido, a modo de detectores de proximidad; estos trabajan libres de roces mecánicos y  detectan objetos a distancias de hasta 4[m]. El sensor emite una onda sonora de alta frecuencia que al reflejar en un objeto, vuelve al sensor en forma de eco. El sensor convierte el tiempo en que tarda en llegar el eco en un pulso de ancho variable, que puede medirse con el microcontrolador para calcular la distancia al objeto.

=== Distancia ===

Mediante sensores reflectivos infrarrojos, se contaran las rpm de cada motor para traducirlas en distancia recorrida por el robot.

=== Gestion de Energía ===

Mediante mediciones de corriente entregada por la batería y la tensión a los bornes de la misma, se va a intentar predecir la autonomía de la misma. Este bloque tambien incluye protecciones de corto circuito que desconectan la batería en caso de detectarse una corriente muy elevada y ademas una desconexión automática para el caso en que la tensión de la batería sea inferior a la tensión de descarga completa.

=== Comunicación ===

Todos los datos recolectados por el robot, serán enviados al bloque de control para su procesamiento. Ademas, el bloque de control, tendrá la posibilidad de enviar datos para guiar remotamente al robot.

=== Control ===

El control, será efectuado por un joystick conectado al bloque de control. Esto permitirá guiar remotamente al robot por el camino deseado para tomar mediciones, el robot, debería ser capaz de reproducir este camino en sentido contrario, para volver al punto de partida de manera autónoma.

=== Actuadores ===

El control de los actuadores se realizará por medio de PWM para controlar las velocidades individuales de los motores.


----
== Potencia ==

Esta es la etapa que gestiona el movimiento de los motores , la misma se basa en una placa de Driver (Puente H) para los motores.

----
