~+'''''201003-003'''' ''''Robot Seguidor de Línea''''' +~

<<TableOfContents()>>

= Equipo =
'''Responsables del proyecto'''

 * [[http://cdr.usla.org.ar/NicolasIgnacio|Nicolás Ignacio]]
 * [[http://cdr.usla.org.ar/HernanPaez|Hernán Paez]]

 . ''Los  que estén interesados en formar parte del proyecto, envien mail a la lista de correo del CdR, solicitando ser incluidos en la lista de mails donde informamos noticias y respondemos consultas: ''[[ListaGrupoRSL|Lista del Grupo RSL]].

 *[[GruposRSL|Grupos de Trabajo]] para el desarrollo de los RSL velocistas!

= Noticias importantes y actividades =
* El jueves 2 de mayo '''iniciamos las actividades del ciclo 2013'''. Nos reuniremos todos los jueves en el laboratorio central de electrónica, de 16:00hs a 18:15hs. Más adelante según los horarios disponibles, tal vez nos empecemos a juntar dos veces por semana.

* El '''repositorio''' del proyecto está en''' ''svn://cdrutnfrc.linuxsecured.net/CdR-Principal/trunk/Proyectos/RSL'' ''' ante cualquier duda, en el link http://cdr.usla.org.ar/RedTrabajo se explica paso a paso como conectarse/trabajar con el repo.


Recomendamos ver los siguientes [[LinksRecomendadosRSL|links]] y bajar software libre para aprender, experimentar, investigar y realizar proyectos.

= Introducción y objetivos =
----
Los RSL son robots que se caracterizan por seguir líneas trazadas en el piso. Son muy usados en la industria donde se requieren robots que se muevan por lugares bien definidos y de forma repetida. Estos agilizan el transporte de material de un lugar a otro dentro de una fábrica o lugar de almacenamiento tipo stock. Son muy rápidos y se caracterizan por la precisión y por su rigurosidad en seguir el camino trazado por la línea previamente definida, son programables, y trabajando varios en conjunto, se comunican entre sí para no colisionar en los momentos que comparten el trazado. Hoy en día el depósito/extracción de cajas/objetos se ve completamente automatizado por estos sistemas móviles, que reciben constantemente información de los paquetes que existen en stock y los requeridos por la gente, que generalemente hace los pedidos cómodamente desde sus casas vía web.

A nivel académico, existen competencias a nivel nacional y mundial en las que participan distintas instituciones de nivel secundario o universitario. El Club de Robótica, mediante este proyecto, a partir del año 2011 se propuso participar de la competencia nacional de robótica organizada anualmente por la UTN Facultad Regional Bahía Blanca, cosa que se logró en el año 2012. Dicha competencia consiste en una serie de carreras en las que participan dos robots velocistas siguiendo una línea blanca en la que gana el robot que diera una vuelta mas rápido.

= Consideraciones Previas =
Algunos aspectos a tener en cuenta a la hora de diseñar tanto el hardware como el software son las siguientes:

 * '''Dimensiones''': el robot completo no puede superar 20 cm de largo, 12 de ancho y 10 de alto

 * '''Pista''': la pista consiste en una linea de 2,5±0,3  cm de ancho de color blanco sobre un fondo negro

 * '''Curvas''': 10 cm antes y despues de cada curva, hay dos marcas de blancas que pueden ser usadas para que el robot se prepare para doblar.

{{http://cdr.usla.org.ar/RSLHard?action=AttachFile&do=get&target=disenio.jpg}}

El reglamento completo se puede descargar desde la pagina: BahiaBlanca

= Estado del Proyecto =
Actualmente nos encontramos en el diseño y armado de un '''seguidor de líneas basado en PIC'''.

En el año 2010,  concluimos nuestras experiencias con un '''seguidor de líneas totalmente analógico'''. Aquí el link para que vean el añalisis y desarrollo que hicimos del [[RSL analógico]]. Paralelamente, se dieron clases, charlas, y explicaciones de cómo programar los microcontrolades en lenguaje C, se mostraron simulaciones y también el paso a paso de la programación de PICs. . También terminamos el informe "'''Introducción a la  programación de microcontroladores en lenguaje C'''", con el cual se puede  empezar sin saber algo previamente. Con la idea de facilitar nuestras actividades referidas a robótica, confeccionamos un '''DVD''' donde pueden encontrar información muy útil que les puede servir como ayuda tanto para aprender como para elaborar proyectos.

Seguiremos buscando la forma de lograr una plataforma mecanica confiable y versatil, para eso tambien, vamos a diseñar varios circuitos o modulos que se encargaran de realizar las diferentes funciones del robot, a medida que vayamos mejorando los PCB, los iremos subiendo en la página correspondiente a [[RSLHard|Hardware]].

Actualmente, estamos armando una plataforma de hardware que nos sirva para experimentación con microcontroladores PIC, el estado del proyecto se puede ver en la página de  [[PLACAPIC_RSL|PLACA PIC]].
