== Red de Trabajo para los Miembros del CdR UTN-FRC ==
||<tablewidth="100%" tablealign="center":100% style="border: medium none;"> {{attachment:botito_pop_transp_red.png||width=300}} ||

<<TableOfContents()>>


La ''Red de Trabajo'' para los miembro del CdR está compuesta por:

 * La wiki del CdR.
 * La lista de correo, e-mails de la comisión y encargados de proyectos.
 * El Servidor principal SVN del CdR --(y su [[http://trac.usla.org.ar/cdr/browser/trunk/|mirror]].)--
 * El Servidor del [[LabRemoto|Laboratorio Remoto]] accesible por SSH (en etapa de proyecto!).
 * El canal IRC

=== Servidores del CdR ===

Todos los servicios están en marcha. Si por algún motivo no está en línea o falla alguno de los servicios, por favor comuníquelo a la brevedad!

==== Repo SVN ====

El servidor SVN se utiliza para versionado (control de versiones[0][5]) de los archivos (código y documentación) del CdR.

Se puede acceder a la documentación del CdR utilizando un cliente SVN (como kdesvn, qsvn o rapidsvn para Linux, o TortoiseSVN para Win$), --(o por medio de un navegador como firefox si sólo se desean ver los archivos y no modificarlos [[http://trac.usla.org.ar/svn/cdr/trunk/| -- navegar archivos --]])--

Para bajar una copia del Proyecto CdR completo no hace falta autentificación. Para poder hacer un commit (subir cambios o nuevos archivos) hay que estar registrado con nombre de usuario y contraseña. Estos datos deberán ser solicitados por correo electrónico al [[Contacto|administrador]].

Dirección del servidor para checkout: svn://cdrutnfrc.linuxsecured.net/CdR-Principal

--(Para navegar por el repositorio (mirror, sólo lectura): http://trac.usla.org.ar/cdr/browser/trunk/ El mismo se encuentra en servicio continuo.)--

==== Acceso SSH ====

Se podrá acceder al LabRemoto por SSH para hacer ensayos en Linux (hacer prácticas con el SVN, compilar, correr programas, utilizar el laboratorio remoto, etc...)

Para aquellos usuarios que así lo requieran, se les asignará un nombre de usuario y contraseña (también se podrá trabajar con claves públicas) para ingresar al servidor del LabRemoto del CdR.

El LabRemoto se encuentra actualmente offline. Si alguien quiere hacer algún ensayo, envíen un correo al [[Contacto|administrador]] para ponerlo en línea. 

=== ¿Cómo bajar una copia del Proyecto CdR? ===

==== Desde Linux ====

 * Instalar un cliente[3] “subversion” (SVN) apto para su distribución de Linux. Puede ser “kdesvn” si utilizan el escritorio KDE (también qsvn o simplemente usarlo por línea de comando)
 * Verificar que el puerto que utiliza SVN esté abierto en el contrafuegos. SVN utiliza normalmente el puerto 3690.
 * Abrir una consola (por ejemplo: “konsole”) y crear una carpeta en nuestro directorio de trabajo llamada “Proyectos”, y dentro de ella otra carpeta llamada “CdR”.
{{{
usr@linux:~>mkdir Proyectos

usr@linux:~>cd Proyectos

usr@linux:~/Proyectos>mkdir CdR
}}}
 * Hacer un primer “checkout” del proyecto. Para ello dentro de la carpeta “Proyectos” ejecutar el siguiente comando:

{{{
usr@linux:~/Proyectos>svn checkout svn://cdrutnfrc.linuxsecured.net/CdR-Principal/trunk ./CdR
}}}
Así obtenemos nuestra working copy del proyecto y podemos comenzar a trabajar sobre él.
 * Usuarios autentificados pueden hacer “commit” del proyecto (subir su copia local modificada al servidor de versiones) ejecutando el siguiente comando dentro de la carpeta “CdR”:
{{{
usr@linux:~/Proyectos/CdR>svn commit -m “comentario enriquecedor sobre lo que se modificó de no más de un renglón”
}}}
El servidor les preguntará por su nombre de usuario y contraseña. No olvidar los comentarios sobre que se edito!

==== Desde Win$ ====

1º Instalar TortoiseSVN[4] y Firefox (versión >= 3.6.10)

2º Abrir el TortoiseSVN configurar la dirección del repositorio para checkout: svn://cdrutnfrc.linuxsecured.net/CdR-Principal/trunk y el directorio donde vamos a bajar la copia local (working copy)

3º La descarga puede tardar varios minutos (aprox. 30 min. para el primer CO, luego para actualizar o confirmar, los tiempos son mucho menores)

4º Como norma general, antes de comenzar a trabajar hacer un “svn update”. Luego de que han terminado de trabajar (modificación o generación de código o documentación) hacen “checkin”: Esta operación guarda en el servidor de versiones una copia de su proyecto. Normalmente se hace un “checkin” o “commit” al finalizar el día o luego de algún cambio muy importante en el proyecto. Siempre hay que agregar un comentario sobre lo que se modifico cuando se hace un “commit”.

* Si están trabajando en un proyecto y no tienen autentificación en el servidor hagan el pedido por email (si no, no podrán guardar los cambios en el servidor SVN)

=== Procedimiento básico para trabajar con el SVN: ===

SVN puede hacer bien su tarea con archivos de texto plano (típico .txt) Si no lo son la cosa se complica. Es el caso de los archivos ODT y otros relacionados a LibreOffice. Éstos poseen formato XML comprimido, y SVN los trata como si fueran archivos binarios ya que no puede leer en su interior.

Por lo tanto, no es posible hacer la operación de mezcla o fusión automáticamente cuando dos personas modificaron el mismo archivo al mismo tiempo y hay que hacerlo a mano. Para prevenir mayores inconvenientes en esta situación se recomienda el siguiente procedimiento a la hora de comenzar a trabajar:

{{{
up=update; → ci=commi; (+bloqueo/desbloqueo)
}}}

'''Descripción:'''

 * Al inicio del momento/día de trabajo SIEMPRE hacer un 
{{{
svn up
}}}
para actualizar la copia de trabajo local;
 * Luego de haber trabajado sobre la copia local siempre hacer un
{{{
svn ci -m "comentario enriquecedor"
}}}
para subir la copia local al servidor (por ejemplo al final del día/momento de trabajo). En lo posible no hay que dejar pasar mucho tiempo sin hacer un commit para evitar luego mayores problemas en la fusión de la información.

 * Una opción complementaria al punto 1 y 2 es la de bloquear el archivo que se va a editar en el servidor (esto se puede hacer con kdesvn, qsvn o TortoiseSVN), trabajar sobre él, hacer un commit e inmediatamente después sacarle el bloqueo para que otro usuario pueda modificarlo.

Si por algún motivo no recuerdan si han hecho un commit anteriormente y no sabes el estado de tu copia de trabajo, ejecuten
{{{
svn status
}}}
y les indicará que cambios en su copia local se han producido (no así los cambios en el server)

=== ¿Cómo conectarse el servidor del LabRemoto del CdR? ===

Desde Linux:

 * Instalar y habilitar SSH, configurar el contrafuegos, etc... (para ello pueden consultar con [[http://sluc.org.ar|SLUC]])
 * Desde cualquier consola mediante el comando ''ssh'', por ejemplo:
{{{
usr@linux:~>ssh -p puerto usr@cdrutnfrc.linuxsecured.net
}}}
El servidor les preguntará su ''psw''.

Pónganse en contacto para obtener el nombre de usuario, contraseña y número de puerto (se cambió el puerto por defecto por razones de seguridad)

Desde Win$:

1º Tienen que bajar el paquete de programas PUTTY[2]

2º Ejecutan el programa putty.exe y configuran el número de puerto y la dirección del servidor:

servidor: cdrutnfrc.linuxsecured.net

puerto: *(consultar puerto)

Para loguearse el servidor les pedirá el nombre de usuario y la contraseña.

Pónganse en contacto para obtener el nombre de usuario, contraseña y número de puerto (se cambió el puerto por defecto por razones de seguridad)


En la www se puede encontrara mucha y muy buena información referida a ''subversion'' y ''ssh''. Este tutorial sólo pretende ser una pequeña guía de introducción.

=== Canal IRC ===

Contamos con un canal IRC, que es una sala de chat la cual utilizamos para abordar los temas relacionados al CdR.

==== ¿Cómo conectarse al canal? ====

Utilizando como ejemplo el software XChat: Para instalarlo es necesario simplemente el comando desde terminal:

{{{
usr@linux:~> apt-get install xchat
}}}

 Una vez instalado, ejecutamos XChat y nos saldrá una ventana para ingresar nuestro Nick y Red a la que queremos acceder. Cuya red se llama FreeNode, se selecciona y se clickea en editar donde podran encontrar opciones como por ejemplo de ingreso automatico y canal destino.

 En caso particular el canal literal es: "#CdR-UTNFRC" (sin comillas).

-RED: FreeNode

-CANAL: #CdR-UTNFRC

Otra forma de acceder al canal es desde [[ChatIRC]].-



--



Éxitos!

[0] http://es.wikipedia.org/wiki/Subversion

[1] http://www.sluc.org.ar

[2] http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html

[3] http://www.tecsisa.com/index.igw?item=1651

[4] http://tortoisesvn.net

MANUAL SVN

[5] http://svnbook.red-bean.com/

Nota: Si éste tutorial contiene errores por favor háganlo saber a la [[ComisionDirectiva|Comisión Directiva]] del CdR a la brevedad!
