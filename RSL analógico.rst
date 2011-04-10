= Análisis y construcción del seguidor de líneas analógico (año 2010) =
== Fase 1 ==
=== Circuito I ===
{{attachment:Circuito1.jpg}}

Usando un circuito presentado por la página www.x-robotics.com como punto de partida, el mismo es un circuito analógico muy simple que nos servirá para afinar la parte mecánica (si se logra un vehículo que funcione con este circuito, probablemente sea muy fácil adaptarlo a circuitos mas complejos que usen microcontroladores). El funcionamiento de este circuito es muy simple ya que todos los transistores aparecen funcionando como llaves al igual que el fototransistor del CNY70, que al detectar una superficie reflejante desactiva uno de los motores para que el vehículo doble en dirección contraria.

El circuito es el que se presenta en la figura y se necesita uno como estos para cada motor, teniendo siempre en cuenta que el sensor CNY70 que se ubique a la derecha controlará el motor izquierdo y viceversa.

Como se vé el circuito es muy simple y no ofrece muchas posibilidades a la hora de variar por ejemplo la sensibilidad del sensor o la velocidad del motor, es por eso que surgió la necesidad de hacerle ciertas modificaciones para facilitar un poco el desarrollo mecánico.



== Fase 2 ==
=== Circuito II ===
Navegando un poco por internet caímos en la página __www.electronica2000.com__ y nos encontramos con otro circuito, que si bien utiliza casi los mismos componentes, esta configurado para tener una especie de "memoria", es decir que cuando el vehículo se sale por completo de la línea negra el RSL recuerda cual fue el primer sensor en detectar pisar sobre blanco y mantiene al vehículo doblando en la dirección contraria. El circuito lo modificamos para reutilizar los componentes del anterior y es el que se muestra en la figura, se ve que es tan sencillo como el primero pero un poco mas potente:

{{attachment:Circuito2.gif}}

VR1 y VR2 son potenciómetros lineales que se usan para variar la velocidad del motor,

Q6 y Q3 pueden ser los mismos BD140 que se usaron para el primer circuito, los demás pueden ser transistores BC557

R1 y R3 serán resistencias de 100 K. Aconsejamos reemplazarlas por potenciómetros para variar la sensibilidad sensorial.

Esta configuración fue simulada y funciona correctamente, tanto la memoria como la regulación de velocidad de los motores.
