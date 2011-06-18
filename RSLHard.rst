<<TableOfContents()>>

= Consideraciones Previas =
Uno de los objetivos impuestos para este 2011, fue lograr un seguidor confiable mediante el uso de PICs que nos sirva para participar en la competencia organizada por el GRS de la facultad Bahia Blanca. Algunas cosas a tener en cuenta a la hora de diseñar tanto el hardware como el software son las siguientes:

 * '''Dimensiones''': el robot completo no puede superar 20 cm de largo, 12 de ancho y 10 de alto
 * '''Pista''': la pista consiste en una linea de 2,5±0,3  cm de ancho de color blanco sobre un fondo negro
 * '''Curvas''': 10 cm antes y despues de cada curva, hay dos marcas de blancas que pueden ser usadas para que el robot se prepare para doblar.



{{http://cdr.usla.org.ar/RSLHard?action=AttachFile&do=get&target=disenio.jpg}}

----

= Hardware del Proyecto =
Ya que cada uno de los desarrolladores del RSL puede construir su propio botito seguidor, vamos a estandarizar un poco las plaquetas, lo que servirá tambien para orientar a los que no sepan por donde empezar.

== Sensores ==
Al igual que el año pasado vamos a usar siempre los sensores CNY70, su precio ronda los $10 y su rendimiento es muy bueno para este tipo de robots. Estos tendran que ir en la parte inferior del movil, a una distancia maxima de 5 mm del piso (el sensor funciona a distancias mayores, pero nos estaríamos exponiendo a la interferencia por la luz infrarroja de cualquier otra fuente)

Se pueden ver sus datos de funcionamiento en la [[http://www.micropik.com/pdf/cny70.pdf|hoja de datos]], sólo diremos que este sensor consta de un led infrarrojo y un fototransistor, cuando los polarizamos, la resistencia interna del transistor varía segun la superficie frente a él refleje o no la luz infrarroja emitida por el led. En nuestro caso, los valores o datos que vamos a obtener del transistor nos indicarán si el sensor se encuentra sobre una superficie blanca, o sobre la linea negra que debe seguir.

El PCB que vamos a usar es el que se ve en la siguiente figura, es sólo a modo ilustrativo y se puede dibujar directamente sobre la placa, sólo hay que tener cuidado de que la distancia entre las caras externas de los sensores sea de 1,5 cm, para que no nos quede por afuera de la linea. Los valores de R1 y R2 son  220 y 10K respectivamente, ya que esta parte del circuito no va a cambiar en ninguna de las fases del proyecto. El punto negro al lado de los sensores indica que de ese lado está el area marcada del sensor.

{{http://cdr.usla.org.ar/RSLHard?action=AttachFile&do=get&target=sensores.jpg||height="209px",width="360px"}}

----
