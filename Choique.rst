= Grupo de desarrollo del RSL "Choique" =

== Reuniones ==

Horarios : '''Miercoles de 18hs a 20hs'''

Lugar: '''LTD UTN-FRC'''

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choique.jpg||width="250"}} ||

== Características ==

Sensor: 4xCNY70 (2+2)

Controlador: ucPIC 16f877/A

Driver: Puente H L293b

Motores: 2xCC, rotor bobinado, estator imán permanente.

Vehículo: 4x4, tracción diferencial? 2x2, triciclo?

Nota: Se pueden utilizar las cajas reductoras de los autitos comerciales, no hay ningún inconveniente afirman los organizadores de la competencia de Bahia Blanca.

== Hardware && Software ==

Listado de materiales: PIC16f877, XTal4MHz, 2x capa. ceram.27pf, 5x LED(2xRojo-2xVerde-Amarillo), 5x R1k, zócalo 40 pts., capa 220uf electrol., capa 1uf electrol., R22k, pulsador, 9x capa. ceram. 0.1uf,  conectores..., L293b, GD4049B, 3x capa. electrol. 100uf, 5x R100, 2x R10k

=== Placa ===
Esquemático y el PCB de la Placa Pic en su version V1.1 (.zip) Cualquier cambio que quieran realizarle, pueden hacerlo desde Proteus 7, y creo que es posible importarlo a Kicad. Los archivos están en el repo SVN del club (lugar para subir los cambios)

Dentro del .zip, también hay una pequeña nota, con el contenido de cosas que tiene, y que hacen falta cambiar, o definir bien.

Placa Pic V1.1 (con capacitor filtro en un conector pero no electrolítico) :

[[attachment:placapic.zip]]


=== SO ===

Entorno de desarrollo con PikLab y fuentes (preliminar):

SVN para checkout: 
{{{
svn co svn://cdrutnfrc.linuxsecured.net/CdR-Principal/trunk/Proyectos/RSL/Choique ./CdR_RSL-Choique
}}}

Para sólo lectura: 
{{{
firefox http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL/Choique/RSL-PIC16F877-C
}}}

Algunas fotos del prototipo:

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueA.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueB.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueC.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueD.jpg||width="350"}} ||


Ensayando el algoritmo de control:

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueE.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueF.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueG.jpg||width="350"}} ||
