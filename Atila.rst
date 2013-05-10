 . Grupo de desarrollo del RSL "Atila"

<<TableOfContents()>>
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;         ;text-align:center"> {{attachment:Atila.jpg||width="200"}} ||




 * Germán Ontivero.
 * Marcos Ciceri.
 * Luigi Vazquez.
 * Gustavo Spessot.

Horarios: Nos juntamos los martes en la parte nueva Laboratorio Central

= Estado del Proyecto =
El proyecto actualmente se encuentra en un estado funcional con un control proporcional, este tipo de control tiene muchas limitaciones y debido a esto se está intentando lograr integrar al menos un control Proporcional-Derivativo para disminuir las oscilaciones del robot.
Para lograr el objetivo se deben completar los siguientes pasos:
 * '''Placa de Sensores:''' Se deben poner al menos tres sensores para detectar la posición relativa del robot sobre la línea (actualmente en desarrollo)
 * '''Control:''' es indispensable investigar sobre la implementación de un control PID en C para poder reprogramar el microcontralador.
 * '''Placa de Control:''' para introducir un control PID habrá que modificar un poco la placa de control para introducir dos o tres presets, que definan las constantes necesarias para la implementacion del control PID.
 * '''Regulador de tensión:''' si bien no es estrictamente necesario, sería muy bueno rediseñar el módulo regulador de tensión para integrarlo en la placa de control y agregar un switch de encendido.
 * '''Driver de Potencia:''' si bien consta de un solo integrado, hay que modificarlo para agregarle un pulsador que nos permita activar y desactivar los actuadores, para tener un control en la largada.
 


----
= Hardware del Proyecto =
Ya que cada uno de los desarrolladores del RSL puede construir su propio botito seguidor, vamos a estandarizar un poco las plaquetas, lo que servirá tambien para orientar a los que no sepan por donde empezar.

== Sensores ==
Al igual que el año pasado vamos a usar siempre los sensores CNY70, su precio ronda los $10 y su rendimiento es muy bueno para este tipo de robots. Estos tendran que ir en la parte inferior del movil, a una distancia maxima de 5 mm del piso (el sensor funciona a distancias mayores, pero nos estaríamos exponiendo a la interferencia por la luz infrarroja de cualquier otra fuente)

Se pueden ver sus datos de funcionamiento en la [[http://www.micropik.com/pdf/cny70.pdf|hoja de datos]], sólo diremos que este sensor consta de un led infrarrojo y un fototransistor, cuando los polarizamos, la resistencia interna del transistor varía segun la superficie frente a él refleje o no la luz infrarroja emitida por el led. En nuestro caso, los valores o datos que vamos a obtener del transistor nos indicarán si el sensor se encuentra sobre una superficie blanca, o sobre la linea negra que debe seguir.

El diagrama de conexiones está en la siguiente figura, al armar el pcb hay que tener en cuenta el ancho de la linea de la pista para colocar los sensores centrales y la separacion entre la linea central y las perpendiculares que señalan las curvas para ubicar los sensores del costado.



== Motores ==
Los motores son pequeños motores de corriente continua, similares a los de la imagen. Ya que fueron extraídos de juguetes chinos, los datos no estan bien definidos, pero en base a los datos ed empresas que los venden podemos estimar lo siguiente:

 * tensión: 3V a 6V
 * corriente: sin carga 300 mA
 * corriente máxima: 1330 mA
 * eje salida diámetro: 2 mm.

Si estan sucios o viejos, generalmente se ponen mas duros y el consumo será mas alto y seguramente tendras menos rpm, tambien hay que tener en cuenta que esta sería la velocidad del eje central y que una reduccion mediante engranajes o poleas disminuiría la corriente necesaria cuando se le aplique una carga.

Para calcular la reducción de velocidades al usar engranajes se usa la formula: N·Z = n·z donde N y Z son la velocidad (en rpm) y la cantidad de engranajes del piñón, n y z son los mismos datos pero del siguiente engranaje, es decir, la velocidad del segundo engranaje sera: n = (N·Z)/z, si el piñón está conectado al eje central del motor N será la velocidad del motor.
