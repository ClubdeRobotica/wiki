## page was renamed from Bourbaki
= Bourbaki_v1 =


<<TableOfContents()>>
 

Bourbaki_v1 es una versión de control digital del proyecto, sirve para introducirse en el desarrollo de un "Robot Seguidor de Líneas" pero carece de las ventajas que ofrece un microcontrolador. 

=== Estado del Proyecto  ===
Desarrollado en un 80 % 
=== Etapa de Alimentación ===
* Batería de 9V con un regulador 7805.
==== Sensores ====

* CNY70 : Es uno de los sensores que más se suele usar para los robots seguidores de línea, es un cubo de 7mm de lado aproximadamente. Está compuesto por un fotodiodo y un fototransistor. 

Detalles '''[[CNY70 |AQUÍ]]'''

Los utilizamos para diferenciar la línea a seguir



----
PCB
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:cny70pcb.png||width="250"}} ||

* Vista 3D

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:cny70mas.png||width="400"}} ||

===== Comparador LM358 =====

Este circuito lo utilizamos para amplificar la señal que recibimos de los sensores, para luego enviar dichas señales a la etapa de potencia.

* PCB
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:lm358pcbm.png||width="400"}} ||

* Vista 3D

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:LM358-3D.png||width="400"}} ||




----
===== Etapa de Potencia =====

Circuito que nos permitirá el manejo de los motores.

* L293B

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:aplicacionl293.svg||width="400"}} ||


* PCB
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:l293pcb.png||width="400"}} ||

* Vista 3D

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:l293-3D.png||width="400"}} ||


----
* Fuente de alimentación  

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:placa-rsl-fuente.jpeg||width="500"}} ||




----
====== Móvil ======

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:movil.JPEG||width="450"}} ||

* El plano fue creado con la herramienta de Dibujo de la suite gratuita de productividad personal de código abierto de producción de documentos y procesamiento de datos [[http://es.libreoffice.org/|LibreOffice]].
----
======= Descargar Copia del Proyecto (En desarrollo) =======
 
V 0.1 --> [[attachment:Seguidor_de_linea_Bourbaki.pdf]]

{{{#!wiki note 

El documento esta creado en [[http://es.wikipedia.org/wiki/LaTeX|Latex]], el cual es un sistema de composición de textos, orientado especialmente a la creación de libros, documentos científicos y técnicos; facilitando así la inserción de formulas,gráficos y tablas.

Es importante que todos generemos este documento para pulir errores.

}}}

 

======= Descargar PCB's del Proyecto =======

[[attachment:l293med.brd]]

[[attachment:LM358.brd]]

[[attachment:cny70med.brd]]



======== Fotos ========


* Primeras placas de sensores y potencia.

 Desarrolladas con el software para creación de circuitos impresos [[http://www.lis.inpg.fr/realise_au_lis/kicad/Kicad_files/LogicielKicad_es.htm|Kicad]]
   



||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:S6301701.JPG||width="300"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:S6301727.JPG||width="300"}} ||




* Pre-ensamblado 

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:montaje.jpg||width="300"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:S6302911.JPG||width="300"}} ||




========= Últimos cambios =========

* Completar con los últimos cambios realizados ! 


========== Documentación útil ==========


* Hoja de datos L293B : [[attachment:L293b.pdf]]


* Hoja de datos del sensor CNY70 :[[attachment:cny70.pdf]]

----
[[Bourbaki|Volver]] | [[RSL | principal de RSL]] | [[GruposRSL | Grupos RSL]]
