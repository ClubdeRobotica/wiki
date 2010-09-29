~+'''201003-003 Robot Seguidor de Línea '''+~

<<TableOfContents()>>

= Equipo =
== Responsable del proyecto ==
Gustavo Martinez Spessot < coordinacion.cdr.utnfrc@gmail.com >

== Delegados ==
 * Marcos Ciceri

 * Germán Ontivero

<agregarse usando el link editar>

= Introducción y objetivos =
----
Primer proyecto de robótica de los miembros del CdR. Aprovechando la experiencia y conocimientos capitalizados en el desarrollo del P201003-002, los miembros del CdR se dividirán en grupos de trabajo para conformar cada uno un Robot Seguidor de Línea, en vistas de realizar una demostración y competencia al finalizar el ciclo. Se trazarían líneas generales de desarrollo y luego cada grupo las implementaría bajo su criterio y posibilidades, con el asesoramiento del CdR. Una alternativa para homogeneizar la plataforma y poder centralizarse en el desarrollo electrónico (por lo menos hasta que se conforme una sección de mecánica) es adquirir vehículos comerciales, y adaptarlos para que nos sean de utilidad. Una vez reocrridas todas las fases del proyecto, se pretende que todos tengan una base en electrónica analógica y digital con conocimientos en tipo de microcontroladores.

Un ejemplo de robots seguidores de línea del CdR de la FIUBA: http://www.sase.com.ar/workshop

Este es otro ejemplo de seguidor de linea http://www.x-robotics.com el cual es un circuito analógico y sera nuestro punto de partida.

== Estado del Proyecto ==
Actualmente nos encontramos cerrando el Circuito II  de la Fase I, paralelamente se está desarrollando un pequeño  manual de programación de PICs en lenguaje C para iniciar la Fase II

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

= Anexos =
----
== Links de interés ==
Robogroup empresa dedicada a la robótica educativa http://www.robotgroup.com.ar/web/

Manuales útiles: http://www.iit.upcomillas.es/~alvaro/teaching/Clases/Robots/teoria/

Wiki de un grupo similar al CdR http://www.iearobotics.com/

== ¿Cómo participar? ==
{{{#!wiki note
Si te interesa el proyecto y querés participar, '''escribí a la dirección de contacto del club o directamente al responsable directo del proyecto'''. A la brevedad nos pondremos en contacto informándote de los pormenores.
También podés acercarte los días '''jueves de 16 a 19 hs al Laboratorio Central de Electrónica''' y hablar con nosotros personalmente. Esperamos tu participación!
}}}
