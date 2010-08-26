== P201003-002: Vehículo Robotizado con Tracción Diferencial - VRTD ==
Responsable del proyecto: Marco Alvarez Reyna <direccion (d ot) cdr (d ot) utnfrc (e t) gmail (d ot) com>

Introducción y objetivos:

Como punto de partida contamos con una plataforma lista para usar desde el punto de vista mecánico. Es un robot con orugas de 25x35x~20cm, tracción diferencial, caja con dos relaciones (H/L), construido en [[http://www.worldlingo.com/ma/enwiki/en/Duralumin/1|duraluminio]] T-6 y poliamida 6. Apto para maltrato y experimentación. También cuenta con un cabezal móvil con dos grados de libertad (azimut y elevación) dotado de motores de paso y reductores, con su respectiva etapa de potencia e interfaz. En términos generales hay que implementar el sistema de baterías, el gestor de energía y servicios, drivers de potencia, la UCP y Control, sensorística, sistema de comunicaciones y transmisión de datos y visualización (interfaz humana). También contamos con un pequeño stock de electrónica (uControladores varios 16F,18F, Kit PicStart Plus, placas de prueba, sensores de temperatura, amp. op., acelerómetros, GPS y drivers de potencia) como para largar sin una gran inversión. En este punto el capital humano es lo prioritario. En función de su aplicación (a definir) hay que bautizarlo! Y trazar las líneas de desarrollo.

Descripción general:

Fase 1: Comando a distancia. Se implementaría una CPU esclava montada sobre el Auto(ro)Bot, en este caso podría ser una placa con PIC que ya fue desarrollada por un miembro de la CEE, con puerto serial, ADC, 2 salidas PWM y un puerto digital de salida, que reciba ordenes de una CPU remota por medio de un vínculo cableado. El sistema energético estará montado directamente sobre la plataforma.

Fase 2: Control autónomo. Algunas ideas para implementar en esta fase, propuestas por un compañero de la CEE:

* Utilizar la placa con DSPIC diseñada para Técnicas Digitales como unidad central de proceso: la cooperativa fabrica el programador.

* Utilizar la nueva placa con núcleo ARM diseñada para Técnicas Digitales 2 como unidad central de proceso: hay buena experiencia de aplicación en robótica en el CIII.

Fase 3: Control autónomo. Telemetría. Sería posible la reprogramación a distancia y la lectura remota de los sensores. Habría que implementar un lazo de comunicación bidireccional inalámbrico.

Hoja de ruta:

 1. Representación básica de la idea; TERMINADO
 1. Título del proyecto; TERMINADO
 1. Convocar y definir a los desarrolladores; TERMINADO
 1. Establecer los objetivos; TERMINADO
 1. Definir las fases (progresivas); TERMINADO
 1. Diagramar las tareas; EN MARCHA
 1. Dividir las tareas según recursos; EN MARCHA
 1. Analizar las tecnologías de software y hardware involucradas; EN MARCHA
 1. Bibliografía;
 1. Análisis de tiempos;
 1. Perspectivas/Estimaciones;
 1. DESARROLLO
 1. Futuras mejoras.
 1. Aplicación comercial;
 1. Plan de negocios;
 1. Estrategias de marketing.

Nota: normalmente los proyectos se comienzan por los últimos tres puntos, pero dadas las propuestas de aplicación pedagógicas del mismo las dejamos para analizar en instancias superiores.

Tareas asignadas a este proyecto (ver caja de arena)

Propuesta de aplicación:

 . o Utilizarlo como un robot entrenador. Para que los miembros ingresantes al club se introduzcan a la electrónica y la robótica. Se podría implementar un seminario. o Utilizarlo en apoyo a la Cátedra de Informática 2 para que los alumnos realicen algún práctico extracurricular de programación en C/C++. o Plataforma sobre la cual alumnos de la cátedra de Sistemas de Control puedan implementar algún algoritmo para el control sobre los motores. o También podría ser utilizado por la cátedra de Técnicas Digitales 3 para implementar algún algoritmo para el procesamiento de señales.

'''Fotos de la plataforma:'''
||<tablewidth="100%" tablestyle="text-align: left"100%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD.jpg||width="200"}} ||
||<50%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD1.jpg||width="200"}} ||
||<100%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD2.jpg||width="200"}} ||
||<100%  style="border-right: medium none; border-top: medium none; border-left: medium none; border-bottom: medium none; text-align: center"> {{attachment:VRTD3.jpg||width="200"}} ||




¿Cómo participar?

Si te interesa el proyecto y querés participar, escribí a la dirección de contacto del club o directamente al responsable directo del proyecto. A la brevedad nos pondremos en contacto informándote de los pormenores. Esperamos tu participación!
