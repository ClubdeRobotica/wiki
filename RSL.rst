~+'''201003-003 Robot Seguidor de Línea '''+~

<<TableOfContents()>>

= Equipo =
== Responsable del proyecto ==
 * Gustavo Martinez Spessot <<MailTo(gdrake84 AT SPAMFREE gmail DOT com)>>

== Delegado ==
 * Germán Ontiver <<MailTo(gerbonti377 AT SPAMFREE gmail DOT com)>>


 . ''Los que estén interesados en formar parte del proyecto, envien mail al responable o al delegado, solicitando ser incluidos en la lista de mails donde informamos noticias y respondemos consultas: ''[[ListaGrupoRSL|Lista del Grupo RSL]].

= Noticias importantes y actividades =
* El miércoles 27 de Abril '''iniciamos las actividades del ciclo 2011''' y a partir del 4 de mayo nos reuniremos todos los miércoles en el laboratorio de técnicas digitales de 18 a 20 Hs. Mas adelante según los horarios disponibles, tal vez nos empecemos a juntar dos veces por semana. Los que no hayan anotado sus horarios envíen un mail a Germán Ontivero (ver mail en la [[ListaGrupoRSL|lista]]) especificando que días están disponibles y con ganas de juntarse.

'''NEW!''' 29 de abril. Creamos una sección donde pondremos todas las dudas, inquietudes, y sugerencias que nos plantearon. Click en el siguiente link: DudasSugerenciasPedidos

* El '''repositorio''' del proyecto está en http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL se puede acceder a todos los archivos desde cualquier browser, pero ante cualquier duda, en el link http://cdr.usla.org.ar/RedTrabajo se explica paso a paso como conectarse.

* Además existe un canal de comunicación que usamos la gente del CdR para postear o dejar mensajes/noticias

http://pipio.usla.org.ar/. Sólo tienen que registrarse, es muy simple y es uno de los canales que tiene el CdR, ojalá podamos encontrarlos posteando ahí.

* En las reuniones, '''estamos repartiendo copias del DVD''' que hicimos el año pasado, ahí estan todos los programas y libros que vamos a usar para el desarrollo del RSL. Para acceder a una copia, sólo hay que llevar un DVD virgen.

Recomendamos ver los siguientes [[LinksRecomendadosRSL|links]] y bajar software libre para aprender, experimentar, investigar y realizar proyectos.

= Introducción y objetivos =
----
Los RSL son robots que se caracterizan por seguir líneas trazadas en el piso. Son muy usados en la industria donde se requieren robots que se muevan por lugares bien definidos y de forma repetida. Estos agilizan el transporte de material de un lugar a otro dentro de una fábrica o lugar de almacenamiento tipo stock. Son muy rápidos y se caracterizan por la precisión y por su rigurosidad en seguir el camino trazado por la línea previamente definida, son programables, y trabajando varios en conjunto, se comunican entre sí para no colisionar en los momentos que comparten el trazado. Hoy en día el depósito/extracción de cajas/objetos se ve completamente automatizado por estos sistemas móviles, que reciben constantemente información de los paquetes que existen en stock y los requeridos por la gente, que generalemente hace los pedidos cómodamente desde sus casas via web.

Así mismo existen competencias entre universidades, de seguidores de líneas, donde el objetivo es llegar lo más rápido a destino, o girar tantas vueltas como se pueda sin descarrilar. En youtube pueden ver varios videos escribiendo en el buscador "seguidores de línea" o también "line followers". Aquí algunos links:

http://www.youtube.com/watch?v=H0rBGFp7y1o

http://www.youtube.com/watch?v=LE9lU-a9OoE

http://www.youtube.com/watch?v=2agFiaqJX_4

http://www.youtube.com/watch?v=S72ASR9mcCE&feature=related

http://www.youtube.com/watch?v=4XiRxNkZleY

= Estado del Proyecto =
Actualmente nos encontramos en el diseño y armado de un '''seguidor de líneas basado en PIC'''.

En el año 2010,  concluimos nuestras experiencias con un '''seguidor de líneas totalmente analógico'''. Paralelamente, se dieron clases, charlas, y explicaciones de cómo programar los microcontrolades en lenguaje C, se mostraron simulaciones y también el paso a paso de la programación de PICs. Aquí el link para que vean el añalisis y desarrollo que hicimos del [[RSL analógico]]. También terminamos el informe "'''Introducción a la  programación de microcontroladores en lenguaje C'''", con el cual se puede  empezar sin saber algo previamente. Con la idea de facilitar nuestras actividades referidas a robótica, confeccionamos un '''DVD''' donde pueden encontrar información muy útil que les puede servir como ayuda tanto para aprender como para elaborar proyectos.

= Desarrollo del Proyecto =
== Hardware ==
Ya que cada uno de los desarrolladores del RSL puede construir su propio botito seguidor, vamos a estandarizar un poco las plaquetas, lo que servirá tambien para orientar a los que no sepan por donde empezar.

=== Sensores ===
Al igual que el año pasado vamos a usar siempre los sensores CNY70, su precio ronda los $10 y su rendimiento es muy bueno para este tipo de robots. Estos tendran que ir en la parte inferior del movil, a una distancia maxima de 5 mm del piso (el sensor funciona a distancias mayores, pero nos estaríamos exponiendo a la interferencia por la luz infrarroja de cualquier otra fuente)

Se pueden ver sus datos de funcionamiento en la [[http://www.micropik.com/pdf/cny70.pdf|hoja de datos]], sólo diremos que este sensor consta de un led infrarrojo y un fototransistor, cuando los polarizamos, la resistencia interna del transistor varía segun la superficie frente a él refleje o no la luz infrarroja emitida por el led. En nuestro caso, los valores o datos que vamos a obtener del transistor nos indicarán si el sensor se encuentra sobre una superficie blanca, o sobre la linea negra que debe seguir.

El PCB que vamos a usar es el que se ve en la siguiente figura, es sólo a modo ilustrativo y se puede dibujar directamente sobre la placa, sólo hay que tener cuidado de que la distancia entre las caras externas de los sensores sea de 1,5 cm, para que no nos quede por afuera de la linea. Los valores de R1 y R2 son los mismos que las resistencias usadas en el RSL analógico (680 y 10K), ya que esta parte del circuito no va a cambiar en ninguna de las fases del proyecto. El punto negro al lado de los sensores indica que de ese lado está el area marcada del sensor.

{{attachment:CNY70PCB.jpg||height="236px",width="406px"}}

Si alguien no tiene idea de hacer una plaqueta de circuito impreso y esta interesado en aprender, se puede poner en contacto con cualquiera de los responsables y hacemos una especie de tutorial, es bastante simple, pero nadie nace sabiendo y la idea del cdr es aprender

----
