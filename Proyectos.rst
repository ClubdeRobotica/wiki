||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:LogoProyectos-CdR.png}} ||


La sección ''Proyectos'' del CdR está dividida en dos sub-secciones:

 * [[ProyectosInstitucionales|Proyectos Institucionales]]
 * [[ProyectosIndependientes|Proyectos Independientes]]

Los ''Proyectos Institucionales'' son parte de la iniciación de los miembros ingresantes al CdR. Éstos son dirigidos y coordinados mayoritariamente por la comisión directiva del club, con la colaboración de delegados, y tienen como objetivo estandarizar el nivel de quienes entran al CdR, y se inician en la electrónica y la robótica.

Los ''Proyectos Independientes'' pueden ser propuestos, elegidos, iniciados y llevados adelante, tanto en su dirección, coordinación y ejecución por miembros del CdR, bajo el esquema propuesto.

Durante el transcurso del año 2010 esta metodología sera tan flexible como se requiera, a fin de poder comenzar a trabajar en los proyectos sin tantas etapas previas.

[[ModalidadTrabajo|Modalidad de trabajo]]

[[Implementacion|Implementación]]

[[Financiamiento]]

=== Proyectos Institucionales ===
'''P#1 MiniLab'''
||<#00ff00>''Proyecto Activo'' ||




Construcción del MiniLab. Para ingresantes al CdR, alumnos de los primeros años de Ing. Electrónica y todo estudiante de otra especialidad que lo desee. Ideal para comenzar a desarrollar proyectos e introducirse a la electrónica. Podría acompañarse con la construcción de una fuente de laboratorio y un curso básico de electrónica, soldadura, etc... Se haría en el primer semestre para que luego puedan continuar con el curso de Introducción a Laboratorio brindado por la CEE. Cumplimentada estas dos etapas (MiniLab+Fuente;Curso de la CEE) estarían en condiciones de tomar al año siguiente un proyecto propio. Durante esta primer etapa de formación los ingresantes trabajarían en conjunto con desarrolladores de los años superiores o proyectos ya avanzados introduciéndose a las técnicas de la robótica.

Nota: De todas maneras, si un grupo de los primeros años se siente en condiciones de afrontar un proyecto, sin haber transitado esta etapa de iniciación, puede hacerlo.

'''P#2 VRTD - Robot con tracción diferencial'''
||<#00ff00>''Proyecto Activo'' ||




Como punto de partida contamos con una plataforma lista para usar desde el punto de vista mecánico. Es un robot con orugas de 25x35x~20cm, tracción diferencial, caja con dos relaciones (H/L), construido en duraluminio T-6 y poliamida 6. Apto para maltrato y experimentación. También cuenta con un cabezal móvil con dos grados de libertad (azimut y elevación) dotado de motores de paso y reductores, con su respectiva etapa de potencia e interfaz. En términos generales hay que implementar el sistema de baterías, el gestor de energía y servicios, drivers de potencia, la UCP y Control, sensorística, sistema de comunicaciones y transmisión de datos y visualización (interfaz humana). También contamos con un pequeño stock de electrónica (uControladores varios 16F,18F, Kit PicStart Plus, placas de prueba, sensores de temperatura, amp. op., acelerómetros, GPS y drivers de potencia) como para largar sin una gran inversión. En este punto el capital humano es lo prioritario. En función de su aplicación (a definir) hay que bautizarlo! Y trazar las líneas de desarrollo.

 . '''Fase 1:''' Comando a distancia. Se implementaría una CPU esclava montada sobre el VRTD, en este caso podría ser una placa con PIC que ya fue desarrollada por un miembro de la CEE, con puerto serial y ADC, que reciba ordenes de una CPU maestra remota por medio de un vínculo cableado. '''Fase 2:''' Control autónomo. Algunas ideas para implementar en esta fase, propuestas por otro miembro de la CEE:
  1. Utilizar la placa con DSPIC diseñada para Técnicas Digitales 3 como unidad central de proceso: la cooperativa fabrica el programador.
  1. Utilizar la nueva placa con núcleo ARM diseñada para Técnicas Digitales 2 como unidad central de proceso: hay buena experiencia de aplicación en robótica en el CIII.
 '''Fase 3:''' Control autónomo. Telemetría. Sería posible la reprogramación a distancia y la lectura de datos de los sensores. Habría que implementar un lazo de comunicación bidireccional inalámbrico.

'''Propuesta de aplicación:'''

 * Utilizarlo en apoyo a la Cátedra de Informática 2 para que los alumnos realicen algún práctico extracurricular de programación en C/C++.

 * Plataforma sobre la cual alumnos de la cátedra de Sistemas de Control puedan implementar algún algoritmo para el control sobre los motores.

 * También podría ser utilizado por la cátedra de Técnicas Digitales 3.

'''Fotos de la plataforma:  '''
||<tablewidth="100%" tablestyle="text-align: left;"100%  style="border: medium none ; text-align: center;"> {{attachment:VRTD.jpg||width="200"}} ||
||<tablewidth="100%" tablestyle="text-align: left;"50%  style="border: medium none ; text-align: center;"> {{attachment:VRTD1.jpg||width="200"}} ||
||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:VRTD2.jpg||width="200"}} ||
||<tablewidth="100%" tablestyle="text-align: left;"100%  style="border: medium none ; text-align: center;"> {{attachment:VRTD3.jpg||width="200"}} ||




'''P#3 Robot Seguidor de Línea'''
||<#00ff00>''Proyecto Activo'' ||




Aprovechando la experiencia y conocimientos capitalizados en el desarrollo del P#2, los miembros del CdR se dividirían en grupos de trabajo para conformar cada uno un Robot Seguidor de Línea, en vistas de realizar una demostración y competencia al finalizar el ciclo. Se trazarían líneas generales de desarrollo y luego cada grupo las implementaría bajo su criterio y posibilidades, con el asesoramiento del CdR.

Un ejemplo de robots seguidores de línea del CdR de la FIUBA:

'''P#4 Banco de datos'''
||<#00ff00>''Proyecto Activo'' ||




A partir de un torbellino de ideas, se busca generar un banco de datos sobre proyectos que involucren en alguna medida el área de la robótica, buscando que éstos nazcan a partir de necesidades concretas, y tengan una potencial aplicación comercial. Ésta base de datos puede ser muy útil para estudiantes de 3ro, 4to, 5to y 6to año que estén buscando temas para sus proyectos integradores y finales. También sería un lugar donde los nuevos miembros del CdR puedan encontrar proyectos a desarrollar, o generar nuevas ideas a partir de estas propuestas.

Este banco de datos puede hacer las veces de ese caldo primigenio en el cual se comienzan a gestar los proyectos hasta que se dan las condiciones justas para que cobren vida. Muchas veces solo una idea no basta, hacen falta recursos humanos y materiales, condiciones de entorno propicias (económicas, políticas, etc…) que hacen que estratégicamente convenga o no sacar un proyecto a la luz. Mientras tanto pueden encontrar aquí un nicho en el cual adquirir fuerza.

Una vez que un proyecto se selecciona de la base de datos pasa a la zona de proyectos activos.

Un pequeño ejemplo lo que podría ser este proyecto es esta misma página.

==== __Propuestas__ ====
=== Proyectos Independientes ===
'''P#5 Lego Robot'''

Conformar un grupo y presentar un proyecto para acceder al Kit de Robótica Lego que pertenece al “Grupo de Investigación y Desarrollo Lego UTN”, dependiente de la carrera de Ing. en Sistemas de la Información.
||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:legorobot.jpg||width="200"}} ||

En Internet: [[http://mindstorms.lego.com/en-us/default.aspx|Lego Robot]]

'''P#6 VANT'''

Vehículo Aéreo no Tripulado. Para entusiastas! Existen en el mercado pequeños helicópteros semi-robotizados a bajo costo, listos para usar. Adquiriendo uno de éstos vehículos podría abrirse una rama muy interesante dentro de la robótica. Requeriría una inversión inicial. Si algún grupo estuviera dispuesto a hacer la inversión y a comprometerse con el proyecto a largo plazo, contaría con desarrollos previos y el apoyo de por lo menos dos miembros del CdR con experiencia en aviónica. Existe la posibilidad de ensayar aviónica en vuelo sobre aviones reales. Le podría servir al grupo que lo lleve adelante como entorno de desarrollo para casi todos los proyectos integradores de la carrera de Ing. Electrónica.

||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:vant.jpg||width="200"}} ||
||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:vant1.jpg||width="200"}} ||


'''P#7 Portador Articulado (móvil)'''

En condiciones similares a la propuesta del P#2, contamos con un brazo robótico  articulado, compuesto de: hombro, brazo, antebrazo y muñeca, construido en fibra de carbono, duraluminio y acero. Con dimensiones similares a la del brazo de un niño de 12 años. El tren cinemático aún no se encuentra en condiciones de operar. Hace falta incorporar los motores, reducciones y transductores de todos los ejes, salvo el motor y reducción del hombro que ya están. También hace falta rediseñar el sistema de sujeción de la mano. No hay electrónica asociada, esta todo por hacer. Este proyecto es ideal para cubrir necesidades en las áreas de manipulación de material biológico, químico, operación remota de dispositivos, montaje electrónico, etc… Podría articularse algún tipo de relación con el P#2, trabajando en dos proyectos con aplicaciones concurrentes. Hace falta una buena idea de aplicación y manos a la obra!

||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:brazo.jpg||width="200"}} ||


''' P#8 Proyecto M-Touch '''
||<#00ff00>''Proyecto Activo'' ||




Panel de control utilizando sensado capacitivo, usa un comparador para saber si se esta o no tocando el pad táctil impreso en el PCB.

''' P#9 Proyecto LITO '''

Silla de ruedas robotizada utilizando ruedas mecanum wheels.

''' P#10 Proyecto Acua(ro)Bot VSANT '''

Vehículo no tripulado acuático, submarino, tele operado, autónomo. Para inspección, rescate.






=== ¿Cómo proponer un proyecto? ===
Todo aquel que haya trabajado, que este trabajando actualmente, o que tenga una propuesta de proyecto en el área de robótica, está invitado a acercarse al CdR para compartirla y analizar su viabilidad.

Para poder elevar un proyecto como propuesta, deben enviar un informe por e-mail a: clubrobotica (dot) utnfrc (at) gmail (dot) com, con: la propuesta de proyecto con aplicación u objetivos, descripción y funcionamiento básico, estado de avance (todo como máximo media página A4 de texto) y una foto o gráfico de no mas de 200kB adjunta al e-mail. Si desean que su nombre salga publicado relacionado al proyecto aclárenlo. Si quien propone ya pertenece a la lista de correo del CdR, puede generar un nuevo hilo colocando en el asunto el “Propuesta de proyecto: <título>”, con los  ítems anteriormente descriptos y comenzar un debate con los miembros del CdR para ir redondeando el proyecto (y de paso buscar adeptos) Una vez que se llega a una versión mínima de la idea del proyecto, con acuerdo de quienes lo propusieron, se sube el proyecto a la página Web pública del CdR (a la base de datos de proyectos) para su promoción y búsqueda de interesados. Cuando el proyecto alcance cierta masa crítica (adeptos, recursos materiales, asesor, etc..) se decidirá su lanzamiento e .[[Implementacion|implementación]].



  Como consejo, intentar que todo lo que se escribe: se difunda en un formato libre, y que tenga por lo menos una revisión por un tercero, tanto ortográfica como de contenido.

||<tablewidth="100%" tablestyle="text-align: center;"100%  style="border: medium none ; text-align: center;"> {{attachment:linux.jpg||width="200"}} ||
                 




 * El hardware adquirido y desarrollado por los miembros le pertenece a ellos, salvo que deseen donarlo al CdR. En cuanto al desarrollo teórico, se espera que todo lo que se genere en el marco del CdR sea abierto a la comunidad. El tema de la propiedad intelectual queda libre a discusión.
