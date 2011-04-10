~+'''201003-003 Robot Seguidor de Línea '''+~

<<TableOfContents()>>

= Equipo =
== Responsable del proyecto ==
Gustavo Martinez Spessot <<MailTo(gdrake84 AT SPAMFREE gmail DOT com)>>

== Delegados ==
 * Marcos Ciceri

 * Germán Ontivero

= Noticias importantes y actividades =
 . En estos momentos el grupo RSL no inició actividades correspondientes al año 2011. Todavía no organizamos encontrarnos, aún así estamos preparando

material para trabajar este año. Cualquier cosa les avisaremos por mail qué se necesita y las actividades a realizar. Por lo pronto, escriban a gdrake84@gmail.com para informarse o ser parte del grupo.

 .
 . Estamos por crear una''' lista de la gente que está interesada''',''' '''en donde cada uno aparecerá con los intereses que tiene al formar parte del grupo.
 .

          Recordamos a la gente del club que tienen un '''servidor''' a su disposición en donde dejamos documentos, informes, datos, etc. que se elaboraron en el transcurso del 2010. Cualquier duda para ingresar al servidor, acceder al link , o en su defecto enviar mail pidiendo ayuda para tener acceso a la información del server.

 .

          Además existe un canal de comunicación que usamos la gente del CdR para postear o dejar mensajes/noticias. Sólo tienen que registrarse, es muy simple y es uno de los canales que tiene el CdR, ojalá encontrarlos posteando ahí.

 .

         Actualmente '''necesitamos gente''' que sepa trabajar con ''WikiSpaces'' porque tenemos fuertes intenciones de mejorar esta página. Si alguien está interesado, envíe mail al coordinador.



= Introducción y objetivos =
----
          Los RSL son robots que se caracterizan por seguir líneas trazadas en el piso. Son muy usados en la industria donde se requieren robots que se muevan por lugares bien definidos y de forma repetida. Estos agilizan el transporte de material de un lugar a otro dentro de una fábrica o lugar de almacenamiento tipo stock. Son muy rápidos y se caracterizan por la precisión y por su rigurosidad en seguir el camino trazado por la línea previamente definida, son programables, y trabajando varios en conjunto, se comunican entre sí para no colisionar en los momentos que comparten el trazado. Hoy en día el depósito/extracción de cajas/objetos se ve completamente automatizado por estos sistemas móviles, que reciben constantemente información de los paquetes que existen en stock y los requeridos por la gente, que generalemente hace los pedidos cómodamente desde sus casas via web.

          Así mismo existen competencias entre universidades, de seguidores de líneas, donde el objetivo es llegar lo más rápido a destino, o girar tantas vueltas como se pueda sin descarrilar. En youtube pueden ver varios videos escribiendo en el buscador "seguidores de línea" o también "line followers". Aquí algunos links:

http://www.youtube.com/watch?v=H0rBGFp7y1o

http://www.youtube.com/watch?v=LE9lU-a9OoE

http://www.youtube.com/watch?v=2agFiaqJX_4

http://www.youtube.com/watch?v=S72ASR9mcCE&feature=related

http://www.youtube.com/watch?v=4XiRxNkZleY



== Estado del Proyecto ==
            Actualmente nos encontramos en el diseño y armado de un seguidor de líneas basado en PIC. Ya terminamos un informe que explica paso a paso como programar PICs desde cero, el cual se encuentra almacenado en el servidor a disposición de todo el club. El año pasado (2010) concluimos nuestras experiencias con un seguidor de líneas totalmente analógico. Paralelamente, se dieron clases, charlas, y explicaciones de cómo programar los microcontrolades en lenguaje C, se mostraron simulaciones y también el paso a paso de la programación de PICs.

= Descripción general =
----
Fase 1. Basados en un circuito electrónico, se construirá el seguidor de línea. Se analizará la construcción mecánica, el ensamblado de partes, materiales que puedan ser usados como chasis. Se harán pruebas y se tratará de mejorar el circuito básico. El resultado final de esta fase será la realización de un modelo mecánico sólido que funcione con cualquier circuito de las fases posteriores.

Fase 2. Se agregará el uso de PIC, introduciendo a los desarrolladores en la programación de microcontroladores.

Fase 3. Análisis y mejoras del sistema de lazo abierto.

Fase 4. Análisis para implementación de lazos cerrados.

Fase 5. Implementación de sistemas retroalimentados en todas las partes que traiga mejoras al funcionamiento del sistema en general.

Fase 6. Mejoras continuas, tanto funcionales, de rendimiento, mecánicas, y electrónicas.

Todas las fases vendrán acompañadas con mejoras en la tecnología de los materiales, información y ayuda por parte del CdR, aumento de experiencia práctica y conocimiento teórico.

= Fase 1 =
----
== Circuito I ==
Usando un circuito presentado por la página www.x-robotics.com como punto de partida, el mismo es un circuito analógico muy simple que nos servirá para afinar la parte mecánica (si se logra un vehículo que funcione con este circuito, probablemente sea muy fácil adaptarlo a circuitos mas complejos que usen microcontroladores). El funcionamiento de este circuito es muy simple ya que todos los transistores aparecen funcionando como llaves al igual que el fototransistor del CNY70, que al detectar una superficie reflejante desactiva uno de los motores para que el vehículo doble en dirección contraria.

El circuito es el que se presenta en la figura y se necesita uno como estos para cada motor, teniendo siempre en cuenta que el sensor CNY70 que se ubique a la derecha controlará el motor izquierdo y viceversa.

{{attachment:Circuito1.jpg}}

Como se vé el circuito es muy simple y no ofrece muchas posibilidades a la hora de variar por ejemplo la sensibilidad del sensor o la velocidad del motor, es por eso que surgió la necesidad de hacerle ciertas modificaciones para facilitar un poco el desarrollo mecánico.

== Circuito II ==
Navegando un poco por internet caímos en la página www.electronica2000.com y nos encontramos con otro circuito, que si bien utiliza casi los mismos componentes, esta configurado para tener una especie de "memoria", es decir que cuando el vehículo se sale por completo de la línea negra el RSL recuerda cual fue el primer sensor en detectar pisar sobre blanco y mantiene al vehículo doblando en la dirección contraria.El circuito lo modificamos para reutilizar los componentes del anterior y es el que se muestra en la figura, se ve que es tan sencillo como el primero pero un poco mas potente:

{{attachment:Circuito2.gif}}

VR1 y VR2 son potenciómetros lineales que se usan para '''variar la velocidad''' del motor,

Q6 y Q3 pueden ser los mismos BD140 que se usaron para el primer circuito, los demás pueden ser transistores BC557

R1 y R3 serán resistencias de 100 K. Aconsejamos reemplazarlas por potenciómetros para '''variar la sensibilidad sensorial'''.

Esta configuración fue simulada y funciona correctamente, tanto la memoria como la regulación de velocidad de los motores.
