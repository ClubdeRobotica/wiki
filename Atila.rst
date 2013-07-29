 . Grupo de desarrollo del RSL "Atila"

<<TableOfContents()>>
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;         ;text-align:center"> {{attachment:Atila.jpg||width="200"}} ||




 * [[GermanOntivero|Germán Ontivero.]]
 * Marcos Ciceri.
 * Luigi Vazquez.
 * Gustavo Spessot.

= Estado del Proyecto =
----
El proyecto actualmente se encuentra en un estado funcional con un control proporcional, este tipo de control tiene muchas limitaciones y debido a esto se está intentando lograr integrar al menos un control Proporcional-Derivativo para disminuir las oscilaciones del robot.
Para lograr el objetivo se deben completar los siguientes pasos:
 * '''Placa de Sensores:''' Se deben poner al menos tres sensores para detectar la posición relativa del robot sobre la línea (actualmente en desarrollo)
 * '''Control:''' es indispensable investigar sobre la implementación de un control PID en C para poder reprogramar el microcontralador.
 * '''Placa de Control:''' para introducir un control PID habrá que modificar un poco la placa de control para introducir dos o tres presets, que definan las constantes necesarias para la implementacion del control PID.
 * '''Regulador de tensión:''' si bien no es estrictamente necesario, sería muy bueno rediseñar el módulo regulador de tensión para integrarlo en la placa de control y agregar un switch de encendido.
 * '''Driver de Potencia:''' si bien consta de un solo integrado, hay que modificarlo para agregarle un pulsador que nos permita activar y desactivar los actuadores, para tener un control en la largada.
 

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;         ;text-align:center"> {{attachment:foto.jpg||width="300"}} ||


= Hardware del Proyecto =
----

== Sensores ==
Al igual que el año pasado vamos a usar siempre los sensores CNY70, su precio ronda los $10 y su rendimiento es muy bueno para este tipo de robots. Estos tendran que ir en la parte inferior del movil, a una distancia maxima de 5 mm del piso (el sensor funciona a distancias mayores, pero nos estaríamos exponiendo a la interferencia por la luz infrarroja de cualquier otra fuente)

Se pueden ver sus datos de funcionamiento en la [[http://www.micropik.com/pdf/cny70.pdf|hoja de datos]], sólo diremos que este sensor consta de un led infrarrojo y un fototransistor, cuando los polarizamos, la resistencia interna del transistor varía segun la superficie frente a él refleje o no la luz infrarroja emitida por el led. En nuestro caso, los valores o datos que vamos a obtener del transistor nos indicarán si el sensor se encuentra sobre una superficie blanca, o sobre la linea negra que debe seguir.

En el repositorio del proyecto se encuentra el PCB utilizado para la placa de sensores 2013.



== Motores ==
Los motores son pequeños motores de corriente continua, similares a los de la imagen. Ya que fueron extraídos de juguetes chinos, los datos no estan bien definidos, pero en base a los datos ed empresas que los venden podemos estimar lo siguiente:

 * tensión: 3V a 6V
 * corriente: sin carga 300 mA
 * corriente máxima: 1330 mA
 * eje salida diámetro: 2 mm.

Si estan sucios o viejos, generalmente se ponen mas duros y el consumo será mas alto y seguramente tendras menos rpm, tambien hay que tener en cuenta que esta sería la velocidad del eje central y que una reduccion mediante engranajes o poleas disminuiría la corriente necesaria cuando se le aplique una carga.

Para calcular la reducción de velocidades al usar engranajes se usa la formula: N·Z = n·z donde N y Z son la velocidad (en rpm) y la cantidad de engranajes del piñón, n y z son los mismos datos pero del siguiente engranaje, es decir, la velocidad del segundo engranaje sera: n = (N·Z)/z, si el piñón está conectado al eje central del motor N será la velocidad del motor.


== Gestión de Energía ==
 {{attachment:energia.png||width="200"}}
Para regular la tensión entregada por las baterías vamos a usar un regulador Step-Down, en este caso un TL2575-05 de TI, que conocimos en la página [[http://www.micropic.es/mpblog/2010/06/alimenta-tus-circuitos-con-un-regulador-step-down/|micropic.es]] y el circuito es el mismo que se puede encontrar en la hoja de datos del componente.
Este dispositivo nos entrega una tension constante de 5V con un muy bajo consumo energía y se puede alimentar sin problemas con tensiones que van de 6V a 40V. En el repositorio se encuentra en formato pdf el PCB utilizado.

== Placa de Control ==
Para el control de Atila, se utiliza un PIC16F886 ya que posee todos los modulos internos que necesitamos para el proyecto. Acoplado al PIC se hay un CD4049 que está formado por 6 compuertas inversoras CMOS y sirve de buffer entre el microcontrolador y el driver de potencia. El circuito completo es el que se puede ver en el repositorio donde tambien aparecen las imágenes para poder imprimir el PCB. La siguiente imagen es una vista 3D de la placa de control:

 {{attachment:control.png||width="200"}}

El circuito impreso mide 87x50 mm y sobre el mismo se ven cuatro conectores, uno para la alimentacion y otro para el ICSP y los otros dos son para conectar la placa de sensores y el puente H que controlará los motores.

----
[[RSL|Principal RSL]] | [[GruposRSL | Grupos RSL]]
