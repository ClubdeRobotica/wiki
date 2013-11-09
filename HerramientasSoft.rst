= Herramientas de Programación =

<<TableOfContents()>>

Esta página contiene una guia de como instalar y configurar las herramientas necesarias para programar la Stellaris Launchpad desde un entorno linux usando Code::Blocks como IDE un toolchain basado gcc como compilador de arm y las librerías y herramientas que nos provee Texas Instruments

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
