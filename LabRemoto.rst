= Laboratorio Remoto =

Desarrollador: vacante!

== Introducción ==

El ''Laboratorio Remoto'' es un emprendimiento enmarcado en el ''Proyecto VANT''. El objetivo de este emprendimiento es comenzar a hacer experiencia en telemetría y teleoperación.

=== Configuarión actual del Laboratorio Remoto ===
{{{
Actuadores+Sensores <---> Server CdR <---> Router <---> INTERNET <---> PC Cliente (miembros CdR) <---> Aplicación
}}}

--( Por lo pronto contamos con una WebCam y un GPS en línea (a modo experimental). )-- Próximamente agregaremos más señales y actuadores. La aplicación remota puede correr nativa en el servidor por medio de un túnel SSH.

==== Link a las señales ====

--( http://cdrutnfrc.mooo.com/index-cam.html )--

*** El servidor del LabRemoto se encuentra offline ***

Para tener acceso exclusivo a los recursos hay que solicitar una ventana de tiempo. Si los servicios no están accesibles escriban a la dirección "marcoar AT SPAMFREE cdr DOT usla DOT org DOT ar" comentando la anomalía.

===== Software para comunicación con el GPS (serial) =====

Disponible en el Servidor SVN del CdR (/>CdR/Proyectos/VANT/software/gps). Debe correr nativo en el servidor del LabRemoto. Para acceder al servidor deben solicitar una cuenta SSH.

* Una guía de lo que es un Laboratorio Remoto se presenta en la siguiente figura:

||<tablewidth="100%" tablealign="center":100% style="border: medium none;"> {{attachment:Modelo-LabRemoto.jpg||width=500}} ||

== Tareas ==

 * Ya tenemos un servidor andando y hay que levantar un servidor de backup (al estilo hot-plug), por si se cae el principal. Hay que clonar todos los servicios y validar el hardware.

 * Hay que realizar varias tareas relacionadas a la integridad del servicio y conservación de los datos.

 * Trabajar en políticas y estrategias de seguridad en la red.

 * Levantar nuevos servicios: implicaría algo de programación html básica, C++, java y quizás algo de python. 

 * Hay que programar una aplicación Cliente/Servidor para publicar los datos y poder interactuar con la planta (orientados a telemetría y teleoperación) y así independizarse del software nativo en el servidor. Tienen que ser necesariamente aplicaciones portables, escalables, reutilizables y bien documentadas. En un futuro (esperemos no muy lejano), la aplicación servidor tendría que poder correr embebida en una SBC con núcleo ARM (Linux ~2.6.32.x / Debian)

 * Investigar cuán factible es integrar las OpenCV (intel) a este proyecto, en vistas de generar un entorno para competencia de robots.

 * Reacondicionamiento de la clase "serialCom".

=== Tips ===

 * GNU/Linux. Apache2, Subversion, servidores.
 * Modelo del canal de comunicaciones (delays)
 * Calidad del servicio (continuidad)
        
== Links de interés ==

http://lab.dia.uned.es/rlab/
