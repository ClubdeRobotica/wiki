En esta sección se especifica el Hardware utilizado en el proyecto.



 ==  Diagrama General ==

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:Bloque_trabajo.png||width="500"}}||

----
== Unidad de control ==





||<tablewidth="100%" tablestyle="text-align:center"50%  style="border:medium none; ;text-align:center">{{attachment:ARMLPC2114_versionWiki.png|ARM LPC2114|width="300"}}||<tablewidth="100%" tablestyle="text-align:center"50%  style="border:medium none; ;text-align:center">{{attachment:ARMLPC1768_versionWiki.png|Kit LPC1768|width="300"}}||


El control del VRTD está a cargo de dos microcontroladores de la familia  [[http://es.wikipedia.org/wiki/Arquitectura_ARM.|ARM]](Advanced RISC Machines), los cuales poseen un núcleo de arquitectura [[http://es.wikipedia.org/wiki/RISC.|RISC]] (Reduced Instruction Set Computer), de 32 bits.

Los microcontroladores utilizados en es este caso son : LPC2124 y LPC1768 cortex-M3 de la firma [[http://es.wikipedia.org/wiki/NXP_Semiconductors|NXP Semicondcutors]]

* Datasheet [[attachment:lpc2124.pdf]]

* Datasheet [[attachment:LPC1768.pdf]]


Para el '''LPC2124''' se utiliza una placa de desarrollo diseñada en la UTN-FRC por la [[http://www.organizaciones.frc.utn.edu.ar/cee/|CEE]]. Esta consiste en una placa con el microcontrolador y sus respectivas I/O + placa programadora.

El '''LPC1768''' esta montado sobre el kit de desarrollo [[http://www.hotmcu.com/lpc1768minidk2-development-board-28-tft-lcd-p-12.html|LPC1768-Mini-DK2]] de la firma THAOYU Electronics.
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
