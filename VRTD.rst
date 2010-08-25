== P#2 VRTD - Robot con tracción diferencial ==

Proyecto Activo

Como punto de partida contamos con una plataforma lista para usar desde el punto de vista mecánico. Es un robot con orugas de 25x35x~20cm, tracción diferencial, caja con dos relaciones (H/L), construido en duraluminio T-6 y poliamida 6. Apto para maltrato y experimentación. También cuenta con un cabezal móvil con dos grados de libertad (azimut y elevación) dotado de motores de paso y reductores, con su respectiva etapa de potencia e interfaz. En términos generales hay que implementar el sistema de baterías, el gestor de energía y servicios, drivers de potencia, la UCP y Control, sensorística, sistema de comunicaciones y transmisión de datos y visualización (interfaz humana). También contamos con un pequeño stock de electrónica (uControladores varios 16F,18F, Kit PicStart Plus, placas de prueba, sensores de temperatura, amp. op., acelerómetros, GPS y drivers de potencia) como para largar sin una gran inversión. En este punto el capital humano es lo prioritario. En función de su aplicación (a definir) hay que bautizarlo! Y trazar las líneas de desarrollo.

    *

      Fase 1: Comando a distancia. Se implementaría una CPU esclava montada sobre el VRTD, en este caso podría ser una placa con PIC que ya fue desarrollada por un miembro de la CEE, con puerto serial y ADC, que reciba ordenes de una CPU maestra remota por medio de un vínculo cableado. Fase 2: Control autónomo. Algunas ideas para implementar en esta fase, propuestas por otro miembro de la CEE:
         1. Utilizar la placa con DSPIC diseñada para Técnicas Digitales 3 como unidad central de proceso: la cooperativa fabrica el programador.
         2. Utilizar la nueva placa con núcleo ARM diseñada para Técnicas Digitales 2 como unidad central de proceso: hay buena experiencia de aplicación en robótica en el CIII. 

      Fase 3: Control autónomo. Telemetría. Sería posible la reprogramación a distancia y la lectura de datos de los sensores. Habría que implementar un lazo de comunicación bidireccional inalámbrico. 

Propuesta de aplicación:

    * Utilizarlo en apoyo a la Cátedra de Informática 2 para que los alumnos realicen algún práctico extracurricular de programación en C/C++.
    * Plataforma sobre la cual alumnos de la cátedra de Sistemas de Control puedan implementar algún algoritmo para el control sobre los motores.
    * También podría ser utilizado por la cátedra de Técnicas Digitales 3. 
