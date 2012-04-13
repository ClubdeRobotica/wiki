~+'''P201003-002: Vehículo Robotizado con Tracción Diferencial - VRTD'''+~

(Inicialmente denominado Auto(ro)Bot, luego AutoRoBot, ahora VRTD)

<<TableOfContents()>>

= Equipo =

== Responsable del proyecto ==

 * Marco Alvarez Reyna <<MailTo(marcoar AT SPAMFREE cdr DOT usla DOT org DOT ar)>>

== Desarrolladores ==

=== Placa de control ===
 * Luis Vazquez <<MailTo(luisvazquez AT SPAMFREE cdr DOT usla DOT org DOT ar)>> -> Coordinador
 * Andres Gariboglio <<MailTo(andresgariboglio AT SPAMFREE gmail DOT com)>>
=== Driver de potencia ===
 * Gustavo Martinez Spessot <<MailTo(gdrake84 AT SPAMFREE gmail DOT com)>>

=== Sistema energético ===
 * Javier Gohlke <javiergohlke@gmail.com> -> Coordinador
 * Juan Ignacio Morales <morales.juan.ignacio@gmail.com>

== Adherentes: a confirmar ==
2011
 * Germán Ontivero <gerbonti377@gmail.com> -> Etapa de control;
 * Elias Caceres Mendoza <frodoelias@hotmail.com>

2010
 * Martín Exequiel Rosas <martin.helldead@gmail.com> -> Placa control V1.1: Hardware;
 * Guillermo Gómez <guillegomez35@gmail.com> -> Sistema energético: Fuente conmutada (fase 2);
 * Frank D Schefer <frankdschefer@gmail.com> -> Sistema energético: Fuente conmutada (fase 2);
 * Gaspar Santamarina <gaspa.92@gmail.com> -> Sistema energético;
 * Jorge Montaño <jorge_jiv@hotmail.com> -> Sistema energético; 
 * Ezequiel Molina <martinezequielmolina@gmail.com> -> Sistema energético;
 * Jeremías Palacios <palacios.jeremias@gmail.com> -> Placa control V1.0: Hardware && Software;
 * Cristhian Mauricio Blas <mauricio_blas@hotmail.com> -> Sistema energético: Cargador de baterías;

{{{#!wiki note
Quienes ya estén vinculados a una tarea y no figuren en la lista anotense! Para poder editar la wiki tienen que crearse un usuario y contraseña, y pedir ser agregados al grupo de editores.
}}}

= Introducción y objetivos =

Como punto de partida contamos con una plataforma lista para usar desde el punto de vista mecánico (fue desarrollada en el ITS-Vilada por un grupo de alumnos [OZAB]). Es un robot con orugas de 25x35x~20cm, tracción diferencial, caja con dos relaciones (H/L), construido en [[http://www.worldlingo.com/ma/enwiki/en/Duralumin/1|duraluminio]] T-6 y poliamida 6. Apto para maltrato y experimentación. También cuenta con un cabezal móvil con dos grados de libertad (azimut y elevación) dotado de motores de paso y reductores, con su respectiva etapa de potencia e interfaz. En términos generales hay que implementar el sistema de baterías, el gestor de energía y servicios, drivers de potencia, la UCP y Control, sensorística, sistema de comunicaciones y transmisión de datos y visualización (interfaz humana). También contamos con un pequeño stock de electrónica (uControladores varios 16F,18F, Kit PicStart Plus, placas de prueba, sensores de temperatura, amp. op., acelerómetros, GPS y drivers de potencia) como para largar sin una gran inversión. En este punto el capital humano es lo prioritario. En función de su aplicación (a definir) hay que bautizarlo! Y trazar las líneas de desarrollo.

== Propuesta de aplicación ==
{{{
 1. Utilizarlo como un robot entrenador. Para que los miembros ingresantes al club se introduzcan a la electrónica y la robótica. Se podría implementar un seminario.

 2. Utilizarlo en apoyo a la Cátedra de Informática 2 para que los alumnos realicen algún práctico extracurricular de programación en C/C++.

 3. Plataforma sobre la cual alumnos de la cátedra de Sistemas de Control puedan implementar algún algoritmo para el control sobre los motores.

 4. También podría ser utilizado por la cátedra de Técnicas Digitales 3 para implementar algún algoritmo para el procesamiento de señales.
}}}

= Descripción general =

== Hoja de ruta ==
 1. Representación básica de la idea; '''TERMINADO'''
 1. Título del proyecto; '''TERMINADO'''
 1. Convocar y definir a los desarrolladores; '''EN MARCHA'''
 1. Definir los objetivos; '''TERMINADO'''
 1. Definir las fases (progresivas); '''TERMINADO'''
 1. Establecer los requerimientos y especificaciones en función de los objetivos; '''EN MARCHA'''
 1. Diagramar las tareas; '''EN MARCHA'''
 1. Dividir las tareas según recursos; '''EN MARCHA'''
 1. Analizar las tecnologías de software y hardware involucradas; '''EN MARCHA'''
 1. Analizar la bibliografía disponible;
 1. Análisis de tiempos;
 1. Perspectivas/Estimaciones;
 1. -> DESARROLLO <- '''EN MARCHA'''
 1. Manual de usuario;
 1. Futuras mejoras;
 1. Análisis de mercadeo;
 1. Aplicación comercial;
 1. Plan de negocios;
 1. Estrategias de marketing;

{{{#!wiki note
Normalmente los proyectos se comienzan por los últimos puntos, pero dadas las propuestas de aplicación de índole pedagógicas del mismo, las dejamos para analizar en instancias posteriores.
}}}

== Alcance de cada fase ==

=== Fase 1 ===
Comando a distancia. Se implementaría una CPU esclava montada sobre el Auto(ro)Bot, en este caso podría ser una placa con PIC que ya fue desarrollada por un miembro de la CEE, con puerto serial, ADC, 2 salidas PWM y un puerto digital de salida, que reciba ordenes de una CPU remota por medio de un vínculo cableado. El sistema energético estará montado directamente sobre la plataforma.

=== Fase 2 ===
Control autónomo. Algunas ideas para implementar en esta fase, propuestas por un compañero de la CEE:

  * Utilizar la placa con DSPIC diseñada para Técnicas Digitales como unidad central de proceso: la cooperativa fabrica el programador.

  * Utilizar la nueva placa con núcleo ARM diseñada para Técnicas Digitales 2 como unidad central de proceso: hay buena experiencia de aplicación en robótica en el CIII.

=== Fase 3 ===
Control autónomo. Telemetría. Sería posible la reprogramación a distancia y la lectura remota de los sensores. Habría que implementar un lazo de comunicación bidireccional inalámbrico.

== Tareas asignadas a cada fase ==

=== Fase 1 ===

 1. Interfaz humana: (tarea distribuida) Indicadores luminosos a bordo del VRTD: indicación de estado con leds; Impresión en pantalla en el host remoto.
 1. [[GestorEnergiaServicios|Sistema energético]] básico: Diseñar el gestor de energía y servicios (cargador de baterías, protecciones, distribución de energía, reguladores); Indicadores y alarmas; Medir el VRTD para ver cual es la batería más grande que puede entrar (ya hablamos un poco del formato); Seleccionar y comprar las [[baterias|baterías]] en función de la calidad/precio; Diseñar la sujeción mecánica de las baterías.
 1. Poner en marcha el driver de potencia para tracción con el que contamos (propietario): Disipadores y ventilación.
 1. Implementar una transmisión bidireccional Robot<->PC mediante un canal cableado: Armar el cable con los conectores.
 1. Armar el gabinete para la placa de control y los drivers de potencia: En función del espacio disponible sobre la plataforma (hay que medir la plataforma)
 1. Placa de control: Documentar el Hardware (re-editarlo con KiCad o similar, SL); Documentar el Software (re-editarlo con SL y analizar los compiladores para PIC en Linux, escribir un pequeño informe).
 1. Desarrollo de la tecnología de software para el control del robot y monitoreo de la sensorística: Escribir un programa para controlar en robot de forma remota con realimentación visual; Imprimir en pantalla periódicamente el estado del robot (tensión de las baterías); Implementar un comando de emergencia que desconecte la etapa de potencia.
 1. Búsqueda de bibliografía y desarrollo del material del curso de robótica.
 1. Hacer Ing. Inversa sobre la plataforma y hacer el plano con software CAD, SL.
 1. Documentar placa decontrol: SW y HW.

=== Fase 2 ===
(completar)

 1. Interfaz humana. Indicadores.
 1. Analizar y corregir el corrimiento de las orugas (para mecánicos)
 1. Desarrollar las llaves H para los motores de tracción.
 1. Implementar una transmisión bidireccional Robot<->PC mediante un canal de transmisión de datos inalámbrico.
 1. Desarrollo de la sensorística. Arreglo de fotodiodos/fototransistores. Sensor estéreo ultrasónico.
 1. Diseñar el sistema energético. Protección. Monitores.
 1. Diseñar el cargador de baterías.
 1. Diseñar la UCP. Algoritmo de control. WDT.
 1. Desarrollo del material de curso y búsqueda de bibliografía básica.

=== Fase 3 ===
(completar)

 1. Interfaz humana. Indicadores.
 1. Implementación del control en una plataforma con tecnología ARM.
 1. Desarrollo del material de curso y búsqueda de bibliografía avanzada.

== Fotos de la plataforma ==
----
||<tablewidth="100%" tablestyle="text-align: left"100%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD.jpg||width="400"}} ||
||<50%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD1.jpg||width="400"}} ||
||<100%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD2.jpg||width="400"}} ||
||<100%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD3.jpg||width="400"}} ||
----
= Herramientas de Software =
Para los desarrolladores:

Cómo saben, el CdR adhiere al movimiento de SL, utiliza la plataforma GNU/Linux y herramientas de desarrollo libres. La recomendación es comenzar a relacionarse con el SO Linux y el uso de herramientas libres. Aquí tienen una lista de los programas que muy posiblemente utilicemos en los desarrollos:

 * '''SO Linux''' (SuSE Linux es una buena opción para principiantes, otra muy recomendable y estable es Ubuntu, amigable para comenzar)
 * '''kicad:''' esquemáticos, electrónica.
 * ngspice: simulación.
 * gspiceui: GUI for the Spice Simulators ngspice and gnucap.
 * ng-spice-rework: Mixed-level, Mixed-signal Circuit Simulator Based on spice.
 * gwave2: Waveform Viewer for Spice and Gnucap Simulations.
 * '''emacs:''' editor de texto, para codificación.
 * '''doxigen:''' generación de documentación.
 * doxywizard: generación automática del arch. de conf. para doxygen.
 * doxygate: DoxyGate is Doxygen GUI Frontend written in Qt.
 * '''subversion:''' servidor/cliente SVN para control de revisiones de documentación.
 * kdesvn: cliente SVN (también: qsvn, rapidsvn, etc...)
 * jmeld: visual diff.
 * gtkterm: termina serial para Linux.
 * '''gnuplot:''' ploteo de series de datos.
 * plotutils: GNU Plotting Utilities.
 * kmplot: ploteo de func matemáticas.
 * '''octave:''' matemática (like matlab)
 * qoctave: octave en Qt.
 * R: estadística.
 * pcb: pcb.
 * planner: planeamiento de proyectos.
 * '''qucs:''' simulación de circuitos electrónicos.
 * xv: visor múltiple de imágenes.
 * geda: edición de circ. y creación de netlist, y pcb.
 * SDCC: compilador libre, de C, para microcontroladores
 * '''i4uc''' : IDE multiplataforma para el desarrollo del firmware de microcontroladores
Si necesitan ayuda, contamos con 100% de apoyo de SLUC para todo lo que tenga que ver con SL. [[http://www.sluc.org.ar/|SLUC]] organiza reuniones periódicas para instalar Linux y estas herramientas. También dan soporte. Si alguien necesita ayuda póngase en contacto con ellos.


= ¿Cómo participar? =
Si te interesa el proyecto y querés participar, escribí a la dirección de contacto del club o directamente al responsable directo del proyecto. A la brevedad nos pondremos en contacto informándote de los pormenores. Esperamos tu participación!
