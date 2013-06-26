{{{#!wiki caution

En Construcción 




}}}

<<TableOfContents()>>


En esta segunda versión, incorporamos un microcontrolador (PIC), que nos permite adoptar una lógica de comportamiento, la cual es desarrollada en el [[https://es.wikipedia.org/wiki/C_%28lenguaje_de_programaci%C3%B3n%29.|Lenguaje C]]. Dicha lógica se basa en reconocer las señales provenientes de los sensores, clasificarla, y enviar una respuesta a los motores.



||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:bourbakibannerref.jpg||width="500"}}||

= Móvil =

Construido en su mayoría con acrílico, el móvil consta de dos partes: principalmente por el '''chasis''' (o base) donde se ubican los motorreductores, los cuales se sujetan al chasis con una lámina de aluminio por medio de tornillos; y el punto de apoyo, que fue pegado con un adhesivo instantaneo.- Por otro lado se encuentra el '''soporte para PCB''', que es ubicado sobre el bloque de motorreductores con dos varillas roscadas, tuerca y contratuerca. El PCB luego se monta al soporte por medio de separadores en las esquinas en donde se atornilla quedando bien sujeto.



=== Chasis ===

Diseñado con [[http://librecad.org|LibreCad]]. Dicho diseño se efectuó a LASER sobre un acrílico de 5mm.


[[attachment:chasisCAD.svg|ver diseño CAD|width="600"]]

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:chasisacrilicoref.jpg||width="500"}}||




=== Punto de apoyo ===

Diseñado conjuntamente con el chasis, el punto de apoyo se compone de dos piezas de acrílico, las cuales fueron pegadas con un adhesivo instantaneo. Consta de un cilindro y una media esfera con un espesor de 5 y 10 mm respectivamente, ambos con un radio de 17 mm.

/!\ imagen

=== Soporte para PCB ===

El soporte, tambien de acrílico, construye la segunda base del móvil. Se ubica con varillas roscadas desde la lámina de aluminio pasando por el bloque de motorreductores. Dicho soporte en sus esquinas tiene separadores de metal para atornillar la placa electronica, cerebro de nuestro RSL-Bourbaki.-

/!\ imagen

=== Motorreductores ===

Dado que en la [[Bourbaki_v1| primer versión]] del proyecto tuvimos dificultades con el control de los motores en esta versión optamos por utilizar motorreductores, que no es mas que un motor de CC con una caja reductora acoplada a él.

 En el siguiente enlace se describe detalladamente el modelo que instalamos [[http://www.apys.com.ar/pdf/SP4L_satelital.pdf|SP4L-200]]

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:chasismotoresref.jpg||width="500"}}||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:chasisAlumref.jpg||width="500"}}||



=== Materiales ===


----- 

= Electrónica =

Nuestro proyecto se basa en el [[RSL#Desarrollo_con_microcontrolador_PIC|desarrollo con microcontrolador PIC]] con la diferencia que no utilizamos ( por el momento ) la etapa del inclinómetro.-

 Se implementó en una sola placa principal, que constituye las etapas de sensores, micro, driver y alimentación, descriptas a continuación.

Dicha placa tiene dos versiones. Una realizada por nosotros tanto el diseño como el PCB, que nos sirvió para dar los primeros pasos, observando como reaccionaba el robot. Al ver encaminado el proyecto decidimos encargar el PCB con nuestro diseño a un particular.

/!\ version 1  imagen

/!\ version 2 imagen

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:PCBfinal1ref.png||width="800"}}||




=== Sensores ===

[[CNY70|Sensores]]

=== Microcontrolador ===

[[placaPIC_RSL |Microcontrolador]]

=== Driver de Motorreductores ===

[[driverRSL | Driver]]


=== Alimentación ===

=== Materiales ===
==== Lista de componentes ====
||<rowbgcolor="#6495ED"> '''Resistencias [Ohm]'''||||'''Diodos'''||||'''Capacitores'''||||'''CI'''||||'''Otros'''||
|| R1 470 |||| LED-Power||||C1 0.1uf |||| U2 PIC16F877(/A) |||| BT1 9v ||
|| R2 100 |||| D2 LED-Live |||| C2 0.1uf |||| U4 L293b ||||JP1 POWER||
|| R3 100 |||| D3 1N4007 |||| C3 220uf |||| U3 GD4049B ||||JP2 RESET ||
|| R4 10k |||| D4 1N4007 |||| C4 47uf |||| U1 LM7805 ||||JP3 SERIAL ||
|| R5 100 |||| D5 1N4004 |||| C5 0.1uf ||||-||||JP3 MOTOR-ENA ||
||R6 100 |||| D6 1N4007 ||||C6 0.1uf ||||-||||MOTOR1 MCC_5v_DER ||
||R7 100 ||||D7 1N4007 |||| C7 27pf ||||-|||| MOTOR2 MCC_5v_IZQ ||
|| R8 2k ||||D8 1N4007 |||| C8 27pf ||||-||||U5 CNY70 ||
||R9 470 ||||D9 1N4007 |||| C9 1uf ||||-||||U6 CNY70 ||
|| R10 330 ||||D10 1N4007 |||| C10 0.1uf ||||-||||X1 4MHz ||
|| R11 10k ||||D11 1N4148 |||| C11 0.1uf ||||-||||1x zócalo para CI 2x20 pts||
|| R12 330 ||||-||||C12 100uf ||||-||||2x zócalos para CI 2x8 pts||
||R13 10k ||||-|||| C13 1uf ||||-||||Placa de islas o multiproposito, PCB||
||R14 100 ||||-||||C14 0.1uf ||||-||||-||
|| R15 100 ||||-|||| C15 0.1uf ||||-||||-||
||-||||-|||| C16 0.1uf ||||-||||-||
||-||||-|||| C17 0.1uf ||||-||||-||
||-||||-|||| C18 0.1uf ||||-||||-||

----
[[Bourbaki|Volver]] | [[RSL | Principal de RSL]] | [[GruposRSL | Grupos RSL]]
