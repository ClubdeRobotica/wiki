= Herramientas de Programación =

<<TableOfContents()>>

Esta página contiene una guia de como instalar y configurar las herramientas necesarias para programar la Stellaris Launchpad desde un entorno linux usando Code::Blocks como IDE un toolchain basado gcc como compilador de arm y las librerías y herramientas que nos provee Texas Instruments. Todos los tutoriales estan pensados para un sistema ''ubuntu'' o ''mint lmde'', aunque deberían funcionar sin problemas en ''debian''.

== Code::Blocks 12 ==
Lo primero que vamos a instalar es el Code::Blocks, si bien se encuentra en los repositorios, la version de algunas distribuciones no es la versión 12 que es la que necesitamos. Para esto, seguimos una guia encontrada en el siguiente link  [[http://www.sempreupdate.com.br/2013/04/instalando-versao-atualizada-do.html|sempreupdate.com.br]] los pasos son los siguientes:

 * 1. Agregar el repositorio: 
{{{
$ sudo add-apt-repository ppa:pasgui/ppa
}}}

 * 2. Actualizar:
{{{
$ sudo apt-get update -y
}}}

 * 3. Instalar codeblocks y dependencias:
{{{
$ sudo apt-get install wx-common build-essential checkinstall cdbs devscripts dh-make fakeroot libxml-parser-perl check avahi-daemon codeblocks -y 
}}}



== Programador LM4Flash ==
Es el programa que vamos a usar para grabar el programa en el microcontrolador. Siguiendo el tutorial que encontramos en [[https://labi.fi.uba.ar/chiliproject/projects/club-robotica/wiki/Programando_la_Stellaris_LaunchPad_%28LM4F120%29|Club De Robotica FIUBA]] se instalará esta herramienta y las siguientes. Cabe aclarar que tal como se explica en esa página, usaremos como carpeta base para todo esto /home/usuario/stellaris
El código del programador se debe bajar de un repositorio git, si no se tiene instalado, se debe instalar el git. Entonces situados en la carpeta antes mensionada:
{{{
git clone https://github.com/utzig/lm4tools.git
cd lm4tools/lm4flash
}}}
Ahora tenemos que asegurarnos de tener instalada la libusb:
{{{
sudo apt-get install libusb-1.0-0-dev -y
}}}
Una vez terminada la operacion anterior construimos con
{{{
make
}}}

Esto nos genera un binario que será el encargado de programar el arm. Luego generamos un archivo de configuración
{{{
sudo gedit /etc/udev/rules.d/70-stellaris.rules
}}}
Con el contenido:
{{{
SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", ATTRS{idVendor}=="1cbe", ATTRS{idProduct}=="00fd", GROUP="plugdev", MODE="0660" 
SUBSYSTEM=="tty", ATTRS{idVendor}=="1cbe" ATTRS{idProduct}=="00fd" GROUP="plugdev" MODE="0660" 
}}}
Y reiniciamos udev:
{{{
sudo service udev restart
}}}


== StellarisWare ==
Este es un archivo ejecutable para windows, pero si se descomprime encontraremos que tiene todas las librerías y ejemplos que nos ayudarán a crear los programas para la stellaris launchpad.
Bajamos este archivo: [[https://www.dropbox.com/s/7bykk2tar1dt220/SW-EK-LM4F120XL-9453.exe|StelarisWare]] lo copiamos en la carpeta: /home/usuario/ti y lo descomprimimos con:
{{{
unzip SW-EK-LM4F120XL-9453.exe -d StellarisWare
}}}

== SAT (arm-elf-eabi) ==
Esto está extraido de la [[http://ciii.frc.utn.edu.ar/TecnicasDigitalesII/WebHome|wiki]] de la cátedra de Técnicas Digitales II de la UTN-FRC.

{{{
    sudo su
}}}
Agregar el repositorio al directorio source.list.d 
{{{
    echo deb http://sat.debian.org.ar/debian/ unstable main > /etc/apt/sources.list.d/sat.list
}}}
Agregar la clave 
{{{
    wget -O - http://sat.debian.org.ar/tin@hemera.debian.org.ar.gpg.key | apt-key add -
}}}
Luego se actualiza el repositorio y se instala el paquete 
{{{
    apt-get update
    apt-get install sat-linaro
}}}
Esta instalación presupone que la distribución es unstable, si el paquete no se puede instalar por no cumplir alguna dependencia, existe la posibilidad de que la distribución corresponda a stable para cambiar se realiza lo siguiente.
{{{
echo deb http://sat.debian.org.ar/debian/ stable main > /etc/apt/sources.list.d/sat.list
}}}
Esto cambiará el archivo generado en sources.list.d

Ahora se procede nuevamente con
{{{
    apt-get update
    apt-get install sat-linaro
}}}
Una vez instalado el paquete, se tendrá las herramientas con denominación arm-elf-eabi- en lugar de arm-elf- como se tenía antes, se debe cambiar los nombres de las mismas en los ejemplos, (donde aparece arm-elf-as se cambia a arm-elf-eabi-as y así con los demás) 


== Configuracion del Code::Blocks ==
Esta configuración fue extraída de [[http://alexkaltsas.wordpress.com/2012/12/19/stellaris-launchpad-codeblocks/|alexkaltsas.wordpress.com]] es un tutorial muy completo paso a paso, pero tiene el inconveniente de estar escrito en griego. La única modificacion que se le hizo a esa guia es que tenemos distinta versión del sat, por lo que en las imágenes se va a ver que el prefijo de las herramientas es '''arm-none-eabi-...''' pero para nuestraa version, el prefijo será: '''arm-elf-eabi-...'''
Vamos a seguir paso a paso el tutorial omitiendo la parte del OpenOCD que es un debugger, aunque nos resultaría de gran ayuda a la hora de hacer un programa, esto nos dio bastantes problemas y todavía no se ha podido hacer andar bien.
Comenzamos bajando este archivo: [[http://dl.dropbox.com/u/31742622/stellaris.zip|Stelaris.zip]] y lo descomprimimos en '''home/.codeblocks/share/codeblocks/templates/wizard/''' o donde sea que se haya instalado el codeblocks (si no está en esa ruta puede estar en '''/usr/share/codeblocks/templates/wizard/''' se necesitan permisos de root para escribir en esa ubicación).
Luego, dentro de la carpeta wizard localizamos el archivo '''config.script''' lo abrimos y agregamos:
{{{
RegisterWizard(wizProject,	    _T("stellaris"),    _T("Stellaris Launchpad"),   _T("Embedded Systems"));
}}}
Entre las otras lineas similares a esa. Guardamos, y cerramos el archivo.

Ahora abrimos el Code::Blocks y vamos al menú Settings, seleccionamos '''Debuger'''
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{http://alexkaltsas.files.wordpress.com/2012/12/debugger_1.png||width="800"}} ||

Seleccionamos GDB debugger y presionamos el boton que dice '''Create Config''', en el cuadro de texto escribimos '''ARM''' y presionamos Ok. Seleccionamos la opción ARM que acaba de aparecer y completamos como se muestra en la imágen (recorda que en vez de escribir "arm-none-eabi-gdb" se debe escribir "arm-'''elf'''-eabi-gdb"

||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{http://alexkaltsas.files.wordpress.com/2012/12/debuger_4.png||width="800"}} ||

Finalmente ok y la ahora vamos al nuevamente al menu '''Settings''' seleccionamos '''Compiler'''
En select compiler elegimos '''GNU ARM gcc compiler''' apretamos el boton '''Set as Default''' y seleccionamos la pestaña '''Toolchains executables'''
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{http://alexkaltsas.files.wordpress.com/2012/12/gcc_3.png||width="800"}} ||
En esta pestañana completamos como se muestra en la imágen, recordando que el prfijo para todos es arm-elf-eabi
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{http://alexkaltsas.files.wordpress.com/2012/12/gcc_4.png||width="800"}} ||
Finalmente nos movemos a la pestaña Other Settings y nos aseguramos de que en Compiler Loggin estñe seleccionada la opción '''Full Command Line'''

Presionamos Ok y vamos ahora al menu '''Tools''' seleccionamos '''Configure Tools''' ahora elegimos '''Add''' y completamos como se muestra en la imágen:
||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none;   ;text-align:center"> {{http://alexkaltsas.files.wordpress.com/2012/12/tools_4.png||width="800"}} ||
Lo único que tenemos que tener en cuenta en esto es que en el cuadro Executable, se debe buscar el programa en la carpeta '''/home/<usuario>/stellaris/lm4tools/lm4flash/'''

Una vez configurado, podemos bajar el proyecto blinky desde [[https://www.dropbox.com/s/an8wm3uhxwuee5a/Blinky.zip|Este link]] descomprimirlo y probar que todo funcione. Para esto intentaremos compilarlo y luego, con la Stellaris Launchpad conectada vamos al menu '''Tools''' y seleccionamos '''LM4Flash''' y vemos que nos grabe el programa.

En la [[http://alexkaltsas.wordpress.com/2012/12/19/stellaris-launchpad-codeblocks/|página]] de la cual obtuvimos este tutorial, se puede ver un video donde se explica y se muestra como crear un proyecto desde cero y hacer debug con el openOCD

------------

[[http://cdr.usla.org.ar/VRTD_2013|Volver al Proyecto VRTD]]
