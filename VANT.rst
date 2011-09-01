== P201004-006: Proyecto VANT ==

Responsable del proyecto: Marco Alvarez Reyna <<MailTo(marcoar AT SPAMFREE cdr DOT usla DOT org DOT ar)>>

||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:vant-V1.2.jpg||width="250"}} ||


Nueva propuesta de logo:

||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:vant-V2.0.png||width="350"}} ||

'''Introducción y objetivos:'''

Vehículo Aéreo no Tripulado. Para entusiastas! Existen en el mercado pequeños helicópteros/aviones semi-robotizados a relativamente bajo costo, listos para usar. Adquiriendo uno de éstos vehículos podría abrirse una rama muy interesante dentro de la robótica. Requeriría una inversión inicial. Si algún grupo estuviera dispuesto a hacer la inversión y a comprometerse con el proyecto a largo plazo, contaría con desarrollos previos y el apoyo de por lo menos dos miembros del CdR con experiencia en aviónica. Existe la posibilidad de ensayar aviónica en vuelo sobre aviones reales. Le podría servir al grupo que lo lleve adelante como entorno de desarrollo para casi todos los proyectos integradores de la carrera de Ing. Electrónica.

'''Claves para el desarrollo:'''
{{{
> Sistemas Estocásticos y Fuzzi Logic
> Filtro de Kalman
> Teoría de Control Moderna
}}}

{{{
* Modelo matemático: Red de vórtices; Derivativa; CFD
* Caracterización de los sistemas/subsistemas tanto eléctricos como mecánicos (motor)
* Modelo de elevación (topografía/orografía) de la NASA
* Simulación: Hardware-in-the-Loop (HIL)
* Carcasa, contenedor, sistema anti vibraciones
* Sistemas redundantes de energía y procesamiento
}}}

{{{
-> Estudio de mercado
-> Plan de negocios
-> Inversionistas
}}}

'''Áreas de vacancia en el mercado argentino referente a VATN`s:''' (análisis de mercado)

- despegue autónomo

- aterrizaje autónomo

- pérdida de GPS

- tiempo de divergencia de los cálculos realizados en función de acelerómetros y giróscopos

- cálculo de altura como referencia para el aterrizaje

- autonomía

- generación de energía eléctrica a bordo

- interferencias en el sistema inercial provocadas por el motor

- precisión y exactitud del GPS

- retardo de las señales de comando de la aeronave en el despegue y aterrizaje por medio del canal de comunicaciones digital

- integridad de las señales de RF y seguridad del canal de comunicaciones, sólo se utiliza el código de fábrica de los autopilotos

- costo de los autopilotos importados

- desarrollo de la tecnología de software necesaria para el autopiloto y la base terrena

- customización de sistemas open source, costo de integración y mantenimiento

- soporte de sistemas

- procesamiento digital de imágenes, para calcular superficies cubiertas con exactitud (posible cliente: Catastro)

- procesamiento digital de imágenes, para navegación cuando falta GPS

- niveles de seguridad/confiabilidad para hacerlos aptos para vuelos sobre la ciudad

- rango de temperaturas

- velocidad de viento soportado

- correción de la geometría de las fotos para poder formar un mosaico coherente y de buena calidad, este proceso es muy caro

- el autopiloto comercial no es capaz de tomar acciones de emergencia en función de parámetros externos (fuera de pérdida total de motor, pérdida de GPS, o pérdida de comunicacion con la BT) y es necesaria la intervención del operador del VANT para tomar acciones preventivas/correctivas.

- implementación de planes de emergencia totalmente autónomos en función de todas las situaciones principales de falla


'''Normativa:'''

No hay una regulación clara en Argentina sobre VANTs, sobretodo debido a la dificultad en la definición sobre que es un 
VANT. Se siguen en general las normas FAR21 y FAR23. Hay un grupo de normas internacionales de ejemplo que son las JARUS.

Para los canales de comunicaciones se utilizan las normas MIL-1553 / RS422

'''Planificación de la misión y operación:'''

->En función del operador de carga paga;

->En función del operador del VANT (metereología).

Ambos tiene que llegar a un acuerdo, normalmente es una solución de compromiso. Es clave la negociación!

'''Precios de los pilotos comerciales:'''

* Autopiloto completo (Piccolo II más periféricos + software): U$S22.000 + 60% importación Arg.

* SBC (computadora a bordo, o computadora de carga paga): U$S1.200 + 60% importación Arg.

'''Desarrollos en marcha actualmente en Argentina:'''

* generador eléctrico

* aterrizaje autónomo

'''Canales de comunicación utilizados:'''

* Datos: 2.4GHz, Spread Spectrum

* Video: 1.4GHz analógico

* Módem satelital Iridium http://www.iridium.com/

'''Alcance de las comunicaciones:'''

* Con antenas omnidireccionales: 7km (distancia segura)
* Con antenas direccionales: 40km (se sigue al VANT)

'''Redes de datos:'''

http://es.wikipedia.org/wiki/MIL-STD-1553

'''Tipos de vuelo:'''

* manual

* asistido

* autónomo


'''Autopilotos Open Source:''' (aprox. U$S500)

* Paparazzi

* ArduPilot

* Arduino

'''Autopiloto de ejemplo:''' (utilizado en Argentina)

* CloudCap Tech. Piccolo II http://www.cloudcaptech.com/piccolo_II.shtm

'''Sensor de orientación a modo de ejemplo:'''

* CG Robotics http://www.chrobotics.com/index.php?main_page=index

'''Baterías utilizadas en VANT`s:'''

* Li-Ión (polímero): alta densidad de energía vs peso, excelente para aeronáutica

'''Techo de vuelo:'''

* Altura de vuelo para sacar fotografías: 1.200m

-> De 300m a 1200m de altura hace falta un permiso especial de vuelo del ente regulador

-> por debajo de los 300m el vuelo es libre (no interfiere con rutas comerciales)

=== Desarrollos del CdR ===

'''Diagramas de aviónica:'''

||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:vant1.jpg||width="400"}} ||
||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:vant.jpg||width="400"}} ||
||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:VANT-Software-Diagrama-Modulos.jpg||width="400"}} ||


'''Proyecto [[LabRemoto|Laboratorio Remoto]]:'''
{{{
Actuadores+Sensores <---> Server CdR <---> Router <---> INTERNET <---> PC Cliente (miembros CdR) <---> Aplicación
}}}
Para tener acceso exclusivo a los recursos hay que solicitar una ventana de tiempo. Actualmente contamos con una [[http://cdrutnfrc.linuxsecured.net/index-cam.html|WebCam]] y un GPS en línea. Próximamente agregaremos actuadores.


'''Comunicación con GPS:'''

Software disponible en el Servidor SVN del CdR (mirror de solo lectura, versión alpha):

http://trac.usla.org.ar/svn/cdr/trunk/Proyectos/VANT/software/


=== Links de interés: ===

'''Lista de correo del CdR:''' (hace falta subscribirse a la lista para poder recibir/enviar correos)

https://listas.usla.org.ar/cgi-bin/mailman/listinfo/cdr

'''Servidor SVN del CdR:''' (accediendo a la rama troncal)

svn://cdrutnfrc.linuxsecured.net/CdR-Principal/trunk

'''Definiciones lenguaje aeronáutico:'''

http://www.md80.com.ar/definicion_perf.html

'''Tecnología de software:'''

http://es.wikipedia.org/wiki/Patron_de_diseno

http://es.wikipedia.org/wiki/Lenguaje_Unificado_de_Modelado

http://es.wikipedia.org/wiki/Ingenieria_de_software

http://es.wikipedia.org/wiki/Calidad_de_software

'''FMEA'''

http://en.wikipedia.org/wiki/Failure_mode_and_effects_analysis

'''Agradecimientos:'''

Logo: J.A.S., P.M.C.

'''¿Cómo participar?'''

Si te interesa el proyecto y querés participar, escribí a la dirección de contacto del club o directamente al responsable directo del proyecto. A la brevedad nos pondremos en contacto informándote de los pormenores. Esperamos tu participación!
