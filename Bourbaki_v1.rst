 Cambiamos el nombre del grupo NiEz por '''Bourbaki''' 

== Estado del Proyecto  ==
Desarrollado en un 80 % 
=== Etapa de Alimentación ===
* A definir
==== Sensores ====
* CNY70 : Es uno de los sensores que más se suele usar para los robots seguidores de línea, es un cubo de 7mm de lado aproximadamente. Está compuesto por un fotodiodo y un fototransistor como se puede ver en la imagen.

Los utilizamos para diferenciar la linea a seguir


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:cny70.svg||width="250"}} ||
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:cny70esquema.svg||width="250"}} ||
PCB
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:cny70pcb.png||width="250"}} ||

vista 3D

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:cny70mas.png||width="400"}} ||

===== Comparador =====

éste circuito lo utilizamos para amplificar la señal que recibimos de los sensores, para así enviar dichas señales, a la etapa de potencia

PCB
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:lm358pcbm.png||width="400"}} ||

vista 3D

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:LM358-3D.png||width="400"}} ||





===== Etapa de Potencia =====

Circuito que nos permitirá el manejo de los motores.

*L293B

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:aplicacionl293.svg||width="400"}} ||


PCB
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:l293pcb.png||width="400"}} ||

vista 3D

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:l293-3D.png||width="400"}} ||


====== Móvil ======

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:movil.JPEG||width="450"}} ||



======= Descargar Copia del Proyecto (En desarrollo) =======
 
V 0.1 --> [[attachment:Seguidor_de_linea_Bourbaki.pdf]]


 * El documento esta creado en [[http://es.wikipedia.org/wiki/LaTeX|Latex]], el cual es un sistema de composición de textos, orientado especialmente a la creación de libros, documentos científicos y técnicos; facilitando así la inserción de formulas,gráficos y tablas.

======= Descargar PCB's del Proyecto =======

[[attachment:l293med.brd]]

[[attachment:LM358.brd]]

[[attachment:cny70med.brd]]



======== Fotos ========

* Primeras placas de sensores y potencia.
 
   



||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:S6301701.JPG||width="400"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:S6301727.JPG||width="400"}} ||

Desarrolladas con el software para creación de circuitos impresos [[http://www.lis.inpg.fr/realise_au_lis/kicad/Kicad_files/LogicielKicad_es.htm|Kicad]]

Luego son impresas a tóner, planchadas sobre la placa de cobre y sumergidas en cloruro férrico.
