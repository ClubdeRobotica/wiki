{{{#!wiki caution

En Construcción 


EDITAR y Subir foto real

}}}

<<TableOfContents()>>

En esta segunda versión, incorporamos un microcontrolador (PIC), que nos permite adoptar una lógica de comportamiento, la cual es desarrollada en el [[https://es.wikipedia.org/wiki/C_%28lenguaje_de_programaci%C3%B3n%29.|Lenguaje C]]. Dicha lógica se basa en reconocer las señales provenientes de los sensores, clasificarla, y enviar una respuesta a los motores.



||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center">{{attachment:bourbakiwiki3.png||width="400"}}||

= Móvil =

Construido en su mayoría con acrílico, el móvil consta de dos partes: principalmente por el '''chasis''' (o base) donde se ubican los motorreductores, los cuales se sujetan al chasis con una lámina de aluminio por medio de tornillos; y el punto de apoyo, que fue pegado con un adhesivo instantaneo.- Por otro lado se encuentra el '''soporte para PCB''', que es ubicado sobre el bloque de motorreductores con dos varillas roscadas, tuerca y contratuerca. El PCB luego se monta al soporte por medio de separadores en las esquinas en donde se atornilla quedando bien sujeto.

'''Referencias:'''

=== Chasis ===

Diseñado con [[http://librecad.org|LibreCad]]. Dicho diseño se efectuó a LASER sobre un acrílico de 5mm.


[[attachment:chasisCAD.svg|ver diseño|width="600"]]


=== Motorreductores ===

Dado que en la [[Bourbaki_v1| primer versión]] del proyecto tuvimos dificultades con el control de los motores en esta versión optamos por utilizar motorreductores, que no es mas que un motor de CC con una caja reductora acoplada a él.

 En el siguiente enlace se describe detalladamente el modelo que instalamos [[http://www.apys.com.ar/pdf/SP4L_satelital.pdf|SP4L-200]]

=== Punto de apoyo ===

Diseñado conjuntamente con el chasis, el punto de apoyo se compone de dos piezas de acrílico, las cuales fueron pegadas con un adhesivo instantaneo. Consta de un cilindro y una media esfera con un espesor de 5 y 10 mm respectivamente, ambos con un radio de 17 mm.

/!\ imagen

=== Soporte para PCB ===

El soporte, tambien de acrílico, construye la segunda base del móvil. Se ubica con varillas roscadas desde la lámina de aluminio pasando por el bloque de motorreductores. Dicho soporte en sus esquinas tiene separadores de metal para atornillar la placa electronica, cerebro de nuestro RSL-Bourbaki.-

/!\ imagen

=== Materiales ===


----- 

= Electrónica =

Se basa en el [[RSL#Desarrollo_con_microcontrolador_PIC|desarrollo con microcontrolador PIC]]

En nuestro proyecto se implementó en una sola placa principal, que constituye las etapas de sensores, micro, driver y alimentación descriptas a continuación

/!\ imagen




=== Sensores ===

[[CNY70|Sensores]]

=== Microcontrolador ===

[[placaPIC_RSL |Microcontrolador]]

=== Driver de Motorreductores ===

[[driverRSL | Driver]]


=== Alimentación ===

=== Materiales ===

----
[[Bourbaki|Volver]] | [[RSL | Principal de RSL]] | [[GruposRSL | Grupos RSL]]
