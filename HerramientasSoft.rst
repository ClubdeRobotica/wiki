= Herramientas de Programación =

<<TableOfContents()>>

Esta página contiene una guia de como instalar y configurar las herramientas necesarias para programar la Stellaris Launchpad desde un entorno linux usando Code::Blocks como IDE un toolchain basado gcc como compilador de arm y las librerías y herramientas que nos provee Texas Instruments. Todos los tutoriales estan pensados para un sistema ''ubuntu'' o ''mint lmde'', aunque deberían funcionar sin problemas en ''debian''.

== Code::Blocks ==
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


== Configuracion del Code::Blocks ==
Esta configuración fue extraída de [[http://alexkaltsas.wordpress.com/2012/12/19/stellaris-launchpad-codeblocks/|alexkaltsas.wordpress.com]] es un tutorial muy completo paso a paso, pero tiene el inconveniente de estar escrito en griego.
Vamos a seguir paso a paso el tutorial omitiendo la parte del OpenOCD que es un debugger, aunque nos resultaría de gran ayuda a la hora de hacer un programa, esto nos dio bastantes problemas y todavía no se ha podido hacer andar bien.
Comenzamos bajando este archivo: [[http://dl.dropbox.com/u/31742622/stellaris.zip|Stelaris.zip]] y lo descomprimimos en '''home/.codeblocks/share/codeblocks/templates/wizard/''' o donde sea que se haya instalado el codeblocks (si no está en esa ruta puede estar en '''/usr/local/share/codeblocks/templates/wizard/''' se necesitan permisos de root para escribir en esa ubicación).
Luego, dentro de la carpeta stellaris localizamos el archivo '''config.script''' lo abrimos y agregamos:
{{{
RegisterWizard(wizProject, _T(“stellaris”), _T(“Stellaris Launchpad”), _T(“Embedded Systems”));
}}}
Entre las otras lineas similares a esa.


------------
