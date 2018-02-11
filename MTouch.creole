== P201004-008 Proyecto M-Touch (SCTI) ==

Resumen:
Panel de control utilizando sensado capacitivo, usa un comparador para saber si se esta o no tocando el pad táctil impreso en el PCB.

Responsable del proyecto: Martín Exequiel Rosas <rosas.martin.exequiel@gmail.com>


Introducción y objetivos:

Sistema de control táctil independiente (SCTI) o en inglés Touch control system independent (TCSI). Se busca desarrollar un panel de control/debug para tareas de campo utilizando censado capacitivo (M-Touch: usa un comparador para saber si se esta o no tocando el pad táctil impreso en el PCB)


Objetivos:

1- desarrollar un teclado táctil utilizando la tecnología m-touch. La primera fase de este objetivo es comprender y definir los métodos de construcción y control del censado capacitivo.
- en primera instancia construiremos un censor capacitivo de un solo switch. Para luego avanzar en la implementación de múltiples switch.
- desarrollo del panel táctil.
2- desarrollar el sistema de control maestro.
3- realizar los distintos módulos, ya sea de transmisión o de adquisición de datos.
4- generar la interfase que conectará el teclado con los dispositivos a controlar o a realizar el debug pertinente.
5-realizar un sistema de transmisión inalámbrica o por medio de cables.
6-si se realiza una transmisión inalámbrica se debe desarrollar un sistema de baterías que sea eficiente con respecto al tiempo de autonomía que posea el panel sin necesidad de recarga de las mismas.

Datos importantes:

En si mismo el panel sería "la herramienta de debug". Tendría que poder hacer o poseer:

-como mínimo dos señales de pwm configurables tanto en frecuencia de funcionamiento (ideal: 100hz->80Khz) como en ciclo de trabajo (ideal: 1%->99%)

-como mínimo un puerto de comunicaciones serial norma rs232 (si posee mas de uno el otro estaría bueno que sea rs485 o similar) totalmente
configurable, donde por funciones pre-programadas o mediante el teclado se puedan mandar por el puerto los bytes deseados y visualizar
los datos recibidos. Hay que diseñar un protocolo, portable, escalable, reutilizable, etc...

-un display lcd y un conjunto de leds (8).

-un panel táctil (teclado) con un mínimo de 12 teclas.

-un puerto de 8bits tipo GPIO (puerto digital de entrada/salida) totalmente aislado y buffereado (las entradas se mostrarían en los
leds y en el display, las salidas solamente en el display)
 
* La idea sería poder intervenir un sistema de control de un robót en cualquiera de sus etapas, ya sea para monitoreo o para suplantación de señales, para poder modificar o verificar las condiciones de funcionamiento, etc...



¿Cómo participar?

Si te interesa el proyecto y querés participar, escribí a la dirección de contacto del club o directamente al responsable directo del proyecto. A la brevedad nos pondremos en contacto informándote de los pormenores. Esperamos tu participación!
