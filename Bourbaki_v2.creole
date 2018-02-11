{{{#!wiki caution

En Construcción
}}}
<<TableOfContents()>>

En esta segunda versión, incorporamos un microcontrolador (PIC), que nos permite adoptar una lógica de comportamiento, la cual es desarrollada en el [[https://es.wikipedia.org/wiki/C_(lenguaje_de_programación).|Lenguaje C]]. Dicha lógica se basa en reconocer las señales provenientes de los sensores, clasificarla, y enviar una respuesta a los motores.
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:bourbakibannerref.png||width="480"}} ||




= Móvil =
Construido en su mayoría con acrílico, el móvil consta de dos partes: principalmente por el '''chasis''' (o base) donde se ubican los motorreductores, los cuales se sujetan al chasis con una lámina de aluminio por medio de tornillos; y el punto de apoyo, que fue pegado con un adhesivo instantaneo.- Por otro lado se encuentra el '''soporte para PCB''', que es ubicado sobre el bloque de motorreductores con dos varillas roscadas, tuerca y contratuerca. El PCB luego se monta al soporte por medio de separadores en las esquinas en donde se atornilla quedando bien sujeto.

=== Chasis ===
Diseñado con [[http://librecad.org|LibreCad]]. Dicho diseño se efectuó a LASER sobre un acrílico de 5mm.

[[attachment:chasisCAD.svg|ver diseño CAD]]
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:chasisacrilicoref.jpg||width="500"}} ||




=== Punto de apoyo ===
Diseñado conjuntamente con el chasis, el punto de apoyo se compone de dos piezas de acrílico, las cuales fueron pegadas con un adhesivo instantaneo. Consta de un cilindro y una media esfera con un espesor de 5 y 10 mm respectivamente, ambos con un radio de 17 mm.

/!\ imagen

=== Soporte para PCB ===
El soporte, tambien de acrílico, construye la segunda base del móvil. Se ubica con varillas roscadas desde la lámina de aluminio pasando por el bloque de motorreductores. Dicho soporte en sus esquinas tiene separadores de metal para atornillar la placa electronica, cerebro de nuestro RSL-Bourbaki.-

/!\ imagen

=== Motorreductores ===
Dado que en la [[Bourbaki_v1|primer versión]] del proyecto tuvimos dificultades con el control de los motores en esta versión optamos por utilizar motorreductores, que no es mas que un motor de CC con una caja reductora acoplada a él.

 . En el siguiente enlace se describe detalladamente el modelo que instalamos [[http://www.apys.com.ar/pdf/SP4L_satelital.pdf|SP4L-200]]

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:chasismotoresref.jpg||width="500"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:chasisAlumref.jpg||width="500"}} ||


=== Materiales ===
-----

= Electrónica =
Nuestro proyecto se basa en el [[RSL#Desarrollo_con_microcontrolador_PIC|desarrollo con microcontrolador PIC]] con la diferencia que no utilizamos ( por el momento ) la etapa del inclinómetro.-

 . Se implementó en una sola placa principal, que constituye las etapas de sensores, micro, driver y alimentación, descriptas mas abajo.

Dicha placa tiene dos versiones. La primera realizada por nosotros tanto el diseño como el PCB, que nos sirvió para dar los primeros pasos, observando como reaccionaba el robot. Al ver encaminado el proyecto decidimos encargar el PCB con nuestro diseño a un particular, definiendo la version 2, de fibra de vidrio y con máscara antisoldante.-

En la version 2 también se modificó el diseño al agregar 2 interruptores-PCB que controlan la alimentación general del circuito y el driver de motores.-
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:pcbv1ref.jpg||width="500"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:pcbver2.jpg||width="500"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:pcbfv1ref1.jpg||width="500"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:pcbfinalv2ref.jpg||width="500"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{attachment:PCBfinal1ref.png||width="800"}} ||




=== Programación ===
 . /!\ imagen ICD2

[[Programacion|Programación]]

==== Código Bourbaki ====
=== Sensores ===
[[CNY70|Sensores]]

=== Microcontrolador ===
[[placaPIC_RSL|Microcontrolador]]

=== Driver de Motorreductores ===
[[driverRSL|Driver]]

=== Alimentación ===
Batería recargable de 9V

==== circuito del cargador ====
 . /!\

----

=== Materiales ===
=== Lista de componentes ===
==== PCB ====
||<rowbgcolor="#6495ED">'''Resistencias [Ohm]''' ||||<style="text-align:center">'''Diodos''' ||||<style="text-align:center">'''Capacitores''' ||||<style="text-align:center">'''CI''' ||||<style="text-align:center">'''Otros''' ||
||R1 470 ||||<style="text-align:center">LED-Power ||||<style="text-align:center">C1 0.1uf ||||<style="text-align:center">U2 PIC16F877(/A) ||||<style="text-align:center">BT1 9v ||
||R2 100 ||||<style="text-align:center">D2 LED-Live ||||<style="text-align:center">C2 0.1uf ||||<style="text-align:center">U4 L293b ||||<style="text-align:center">JP1 POWER ||
||R3 100 ||||<style="text-align:center">D3 1N4007 ||||<style="text-align:center">C3 220uf ||||<style="text-align:center">U3 GD4049B ||||<style="text-align:center">JP2 RESET ||
||R4 10k ||||<style="text-align:center">D4 1N4007 ||||<style="text-align:center">C4 47uf ||||<style="text-align:center">U1 LM7805 ||||<style="text-align:center">JP3 SERIAL ||
||R5 100 ||||<style="text-align:center">D5 1N4004 ||||<style="text-align:center">C5 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">JP3 MOTOR-ENA ||
||R6 100 ||||<style="text-align:center">D6 1N4007 ||||<style="text-align:center">C6 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">MOTOR1 MCC_5v_DER ||
||R7 100 ||||<style="text-align:center">D7 1N4007 ||||<style="text-align:center">C7 27pf ||||<style="text-align:center">- ||||<style="text-align:center">MOTOR2 MCC_5v_IZQ ||
||R8 2k ||||<style="text-align:center">D8 1N4007 ||||<style="text-align:center">C8 27pf ||||<style="text-align:center">- ||||<style="text-align:center">U5 CNY70 ||
||R9 470 ||||<style="text-align:center">D9 1N4007 ||||<style="text-align:center">C9 1uf ||||<style="text-align:center">- ||||<style="text-align:center">U6 CNY70 ||
||R10 330 ||||<style="text-align:center">D10 1N4007 ||||<style="text-align:center">C10 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">X1 4MHz ||
||R11 10k ||||<style="text-align:center">D11 1N4148 ||||<style="text-align:center">C11 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">1x zócalo para CI 2x20 pts ||
||R12 330 ||||<style="text-align:center">- ||||<style="text-align:center">C12 100uf ||||<style="text-align:center">- ||||<style="text-align:center">2x zócalos para CI 2x8 pts ||
||R13 10k ||||<style="text-align:center">- ||||<style="text-align:center">C13 1uf ||||<style="text-align:center">- ||||<style="text-align:center">Placa de islas o multiproposito, PCB ||
||R14 100 ||||<style="text-align:center">- ||||<style="text-align:center">C14 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">- ||
||R15 100 ||||<style="text-align:center">- ||||<style="text-align:center">C15 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">- ||
||- ||||<style="text-align:center">- ||||<style="text-align:center">C16 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">- ||
||- ||||<style="text-align:center">- ||||<style="text-align:center">C17 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">- ||
||- ||||<style="text-align:center">- ||||<style="text-align:center">C18 0.1uf ||||<style="text-align:center">- ||||<style="text-align:center">- ||


==== Fuente/Cargador ====
----
[[Bourbaki|Volver]] | [[RSL|Principal de RSL]] | [[GruposRSL|Grupos RSL]]
