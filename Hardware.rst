En esta sección se especifica el Hardware utilizado en el proyecto.



==  Diagrama General ==

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:DiagramaARM.png||width="500"}}||

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

==== Orientación ====

Para la orientación se utilizan sensores de efecto hall, con los cuales, a partir de las mediciones sobre el campo magnético terrestre , podemos conocer hacia donde está el NORTE de la plataforma.


==== Proximidad ====

Para evitar colisiones con objetos del entorno se utilizan sensores de ultrasonido, a modo de detectores de proximidad; estos trabajan libres de roces mecánicos y  detectan objetos a distancias de hasta 8[m]. El sensor emite un sonido y mide el tiempo que la señal tarda en regresar. Estos reflejan en un objeto, el sensor recibe el eco producido y lo convierte en señales eléctricas, las cuales son adaptadas para su posterior proceso mediante el microcontrolador .

==== Distancia ====

Para medir la distancia recorrida tomamos mediciones sobre la cantidad de vueltas que dan los motores mediante sensores ópticos.
----
== Potencia ==

Esta es la etapa que gestiona el movimiento de los motores , la misma se basa en una placa de Driver (Puente H) para los motores.

El circuito se puede observar descargándolo desde aquí 

----
