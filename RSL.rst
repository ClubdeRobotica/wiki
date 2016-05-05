~+'''''201003-003'''''+~

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;             ;text-align:center"> {{attachment:banner.png||width="500"}} ||

<<TableOfContents()>>



= Año 2015 = 


== Responsables ==
'''''Responsables del proyecto''' ''

 * [[NicolasIgnacio|Nicolás Ignacio]]
 * [[HernanPaez|Hernán Paez]]

 . Los  que estén interesados en formar parte del proyecto, envien mail a la lista de correo del CdR, solicitando ser incluidos en la lista de mails donde informamos noticias y respondemos consultas: ''[[ListaGrupoRSL|Lista del Grupo RSL]]. ''

== Grupos ==
 * ''[[GruposRSL|Grupos de Trabajo]] para el desarrollo de los RSL velocistas! ''


=== Interes general ===
 * Recomendamos ver los siguientes [[LinksRecomendadosRSL|links]] y bajar software libre para aprender, experimentar, investigar y realizar proyectos.

=== Introducción y objetivos ===
----
Los RSL son robots que se caracterizan por seguir líneas trazadas en el piso. Son muy usados en la industria donde se requieren robots que se muevan por lugares bien definidos y de forma repetida. Estos agilizan el transporte de material de un lugar a otro dentro de una fábrica o lugar de almacenamiento tipo stock. Son muy rápidos y se caracterizan por la precisión y por su rigurosidad en seguir el camino trazado por la línea previamente definida, son programables, y trabajando varios en conjunto, se comunican entre sí para no colisionar en los momentos que comparten el trazado. Hoy en día el depósito/extracción de cajas/objetos se ve completamente automatizado por estos sistemas móviles, que reciben constantemente información de los paquetes que existen en stock y los requeridos por la gente, que generalemente hace los pedidos cómodamente desde sus casas vía web.

A nivel académico, existen competencias a nivel nacional y mundial en las que participan distintas instituciones de nivel secundario o universitario. El Club de Robótica, mediante este proyecto, a partir del año 2011 se propuso participar de la competencia nacional de robótica organizada anualmente por la UTN Facultad Regional Bahía Blanca, cosa que se logró en el año 2012. Dicha competencia consiste en una serie de carreras en las que participan dos robots velocistas siguiendo una línea blanca en la que gana el robot que diera una vuelta mas rápido.

= Consideraciones Previas =
----
'' Algunos aspectos a tener en cuenta a la hora de diseñar tanto el hardware como el software son las siguientes: ''

 * '''''Dimensiones''': el robot completo no puede superar 20 cm de largo, 12 de ancho y 10 de alto ''

 * '''''Pista''': la pista consiste en una linea de 2 ±0,3  cm de ancho de color blanco sobre un fondo negro ''

 * '''''Curvas''': 10 cm antes y despues de cada curva, hay dos marcas de blancas que pueden ser usadas para que el robot se prepare para doblar. El circuito contará con curvas de un radio de curvatura mínimo de 30cm con una tolerancia del ±10% y todas tendrán un ángulo de peralte nulo.''
 * '''''Elevaciones''': La superficie del circuito podrá contar con irregularidades, las mismas en caso de ser elevaciones tendrán una pendiente máxima de 20 grados.  ''

'' {{http://cdr.usla.org.ar/RSLHard?action=AttachFile&do=get&target=disenio.jpg}} ''

''El reglamento completo se puede descargar desde la pagina: BahiaBlanca ''

= Estado del Proyecto =
----
'' En el año 2012 el proyecto se dividió en dos ramas, una que siguió la linea del 2011 gobernada por un microcontrolador PIC y apareció un nuevo circuito implementado por el grupo [[Kirjava]] apareciendo como una versión evolucionada del [[RSL analógico]] que se desarrolló en 2010.La misma está construida completamente con componentes discretos. Actualmente se siguen desarrollando las dos versiones. ''

''Las distintas versiones se pueden ver en las páginas de cada [[GruposRSL|Grupo de Desarrollo]] y en el repositorio del proyecto. ''

''En la página del desarrollo [[RSL analógico|analógico]] se da una breve explicación de como construir un seguidor de líneas usando sólo transistores, pero se debe tener en cuenta que la simplicidad en el circuito electrónico se paga con complejidad en el desarrollo mecánico. A modo de orientación, se creó un tutorial para modificar dos autitos baratos de juguete para lograr un móvil con tracción diferencial que es el que se necesita para la mayoría de las versiones, el mismo se puede encontrar en el repositorio del proyecto. ''

'' ''

= Desarrollo con microcontrolador PIC =
----
== Diagrama de Bloques ==
'' {{http://cdr.usla.org.ar/RSL?action=AttachFile&do=get&target=bloques.png}} ''

== Descripción de las Etapas Principales ==
''[[placaPIC_RSL|Placa PIC]] | [[CNY70|Sensores]]  |   [[driverRSL|Driver de motores]] ''

----
'' ''

= Desarrollo con Arduino =
----
'' ''
