## page was renamed from VHDL
/!\ en construcción
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:portadacuboled.png||width="800"}} ||

= CuboLED =

<<TableOfContents()>>

== Responsables ==

 * [[GuillermoD.Zarate|Guillermo D.Zarate]]

 * [[FrancoBecutti|Becutti Franco]]

 * [[NicolasIgnacio|Ignacio Nicolás]]

== Objetivo ==

Como objetivo nos planteamos desarrollar tecnología de visualización 3D. Desarrollando funciones
que la implenten, en este caso de dimensiones acotadas, para luego pasar a hardware mas interesante y
competitivo.

== Descripción ==

El Cubo de LED, de dimensiones 6x6x6, será el medio gráfico donde expresaremos visualmente
distintas funciones descriptas en VHDL. La configuracion se realiza en una FPGA Nexys 2


== Esquema general ==

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:esquemacuboxinforme.jpg||width="600"}} ||


== Etapa de control ==

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:controlinforme.JPG||width="500"}} ||

== FPGA ==

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:fpgainforme.JPG||width="500"}} ||

== Funciones ==

Cada función cuenta con distintas variantes. Las cuales son en Frecuencia, Forma y Secuencia. A cada una le corresponde una llave con la cual podrá ser seleccionada.

Disponemos de 6 funciones:

 * Caras: se encienden las caras del Cubo, una a la vez.-

 * Barrido de caras: barre, encendiendo las caras, en todos los sentidos.-

 * Rotación de caras: se toman los tres ejes (x,y,z) como rotacion de las caras.-

 * Rebote de cubo: se forma un cubo 2x2 que rebota al tocar una cara.-

 * Cubo con Variación de tamaño: va cambiando sus dimensiones mientras se desplaza a distintas esquinas.-

 * UTN: graficamos las iniciales UTN, en un barrido de profundidad.-

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:generalinforme.JPG||width="500"}} ||


== Demo ==
||<tablewidth="100%" tablestyle="text-align:center"> <<YouTube(id=uZXlh5CuTjQ)>>||
