Mi idea de esta sección es contar casos en los que tuvimos algún problema o simplemente queremos destacar alguna situación.

===== SVN =====

Algo que me paso un par de veces al querer hacer un checkout es que me dé un aviso de svn OPTIONS ...200 Ok
 Que por el momento ( a mi parecer ) indica que el URL está mal.
{{{
nnico@nnico:~/choiqueRSL$ svn co http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL/Choique

svn: OPTIONS de 'http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL/Choique': 200 Ok (http://trac.usla.org.ar)
}}}
La situación era esta.. navegando por el trac de usla ( http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL ) para buscar gráficamente algo puntual. Específicamente quería bajar todo sobre Choique, asique fui a http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL/Choique. Bien, para bajar esos archivos haríamos un svn co y dicha URL .. osea
{{{
 svn co http://trac.usla.org.ar/cdr/browser/trunk/Proyectos/RSL/Choique
}}}
 Bueno esa era mi lógica. Pero está mal porque yo le daba la URL justamente para el browser.

para bajar correctamente hay que borrar las palabras "browser" y agregarle "svn" a la URL, quedaría así 

http://trac.usla.org.ar/svn/cdr/trunk/Proyectos/RSL/Choique

la orden final para ejecutar seria
{{{
 svn co http://trac.usla.org.ar/svn/cdr/trunk/Proyectos/RSL/Choique
}}}
