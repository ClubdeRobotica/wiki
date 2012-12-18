= Grupo de desarrollo del RSL "Choique" =

== Reuniones ==

Horarios : '''Martes de 16:15hs a 18:15hs'''

Lugar: '''LCE Anexo UTN-FRC'''

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choique.jpg||width="250"}} ||

== Características ==

Sensor: 4xCNY70 (2+2)

Controlador: ucPIC 16f877/A

Driver: Puente H L293b

Motores: 2xCC, rotor bobinado, estator imán permanente.

Vehículo: 4x4, tracción diferencial? 2x2, triciclo?

Nota: Se pueden utilizar las cajas reductoras de los autitos comerciales, no hay ningún inconveniente afirman los organizadores de la competencia de Bahia Blanca.

== Hardware && Software ==

Listado de materiales: (preliminar!)
| BT1        9v          
| C1         0.1uf       
| C2         0.1uf       
| C3         220uf       
| C4         47uf        
| C5         0.1uf       
| C6         0.1uf       
| C7         27pf        
| C8         27pf        
| C9         1uf         
| C10        0.1uf       
| C11        0.1uf       
| C12        100uf       
| C13        1uf         
| C14        0.1uf       
| C15        0.1uf       
| C16        0.1uf       
| C17        0.1uf       
| C18        0.1uf       
| D1         LED-Power   
| D2         LED-Live    
| D3         1N4007      
| D4         1N4007      
| D5         1N4004      
| D6         1N4007      
| D7         1N4007      
| D8         1N4007      
| D9         1N4007      
| D10        1N4007      
| D11        1N4148      
| IC1        ADXL103     
| JP1        RESET       
| JP2        SERIAL      
| JP3        MOTOR-ENA   
| MOTOR1     MCC_5v_DER  
| MOTOR2     MCC_5v_IZQ  
| R1         470         
| R2         100         
| R3         100         
| R4         10k         
| R5         100         
| R6         100         
| R7         100         
| R8         2k          
| R9         470         
| R10        330         
| R11        10k         
| R12        330         
| R13        10k         
| R14        100         
| R15        100         
| U1         LM7805      
| U2         PIC16F877(/A)   
| U3         GD4049B        
| U4         L293b        
| U5         CNY70       
| U6         CNY70       
| X1         4MHz

Además:
 1. 1x zócalo para CI 2x20 pts
 1. 2x zócalos para CI 2x8 pts
 1. Placa de islas o multiproposito, PCB

=== Placa ===

Esquemático y el PCB de la Placa Pic en su version V1.1 (.zip) Cualquier cambio que quieran realizarle, pueden hacerlo desde Proteus 7, y creo que es posible importarlo a Kicad. Los archivos están en el repo SVN del club (lugar para subir los cambios)

Dentro del .zip, también hay una pequeña nota, con el contenido de cosas que tiene, y que hacen falta cambiar, o definir bien.

Placa Pic V1.1 (con capacitor filtro en un conector pero no electrolítico) :

[[attachment:placapic.zip]]

SVN para checkout: 
{{{
svn co svn://192.168.1.130/CdR-Principal/trunk/Proyectos/RSL/Choique/Hardware ./CdR_RSL-Choique-HW
}}}


--( Para sólo lectura: )--
--( firefox http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL/Choique/Hardware )--


Está disponible también la versión del esquemático en KiCAD. Como experiencia: es clave la buena gestión de las librerías y módulos!!!

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:placa-rsl-new.png||width="600"}} ||

=== SO ===

Entorno de desarrollo con PikLab y fuentes (preliminar):

SVN para checkout: 
{{{
svn co svn://cdrutnfrc.linuxsecured.net/CdR-Principal/trunk/Proyectos/RSL/Choique/RSL-PIC16F877-C ./CdR_RSL-Choique-SW
}}}

--( Para sólo lectura: )--
--( firefox http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL/Choique/RSL-PIC16F877-C )--

Algunas fotos del prototipo:

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueA.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueB.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueC.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueD.jpg||width="350"}} ||


Ensayando el algoritmo de control:

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueE.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueF.jpg||width="350"}} ||

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:choiqueG.jpg||width="350"}} ||

Foto del prototipo de la plataforma:

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:rsl-jp.jpg||width="350"}} ||

Prototipo sensores:

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:Imagen0002.jpg||width="350"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:Imagen003.jpg||width="350"}} ||

Bajó al suelo!!!!

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:Imagen0004-b.jpg||width="350"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:Imagen005-b.jpg||width="350"}} ||


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:Imagen006-b.jpg||width="350"}} ||

Nota: El inclinómetro (adxl) no es necesario para el funcionamiento del RSL. Es sólo un complemento.
