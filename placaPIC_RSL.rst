{{{#!wiki caution
                           EN CONSTRUCCIÓN 
}}}
== Esquemático General del Proyecto RSL ==


||<tablewidth="100%" tablestyle="text-align:center"100%  style="border:medium none; ;text-align:center"> {{attachment:placa-rsl-new.png||width="800"}} ||
----
{i} para ampliar click derecho sobre la imagen; '''firefox:''' ver imagen | '''chrome:''' abrir imagen en una nueva pestaña.-
 
----

Dentro del .zip, hay una pequeña nota, con el contenido de cosas que tiene, y que hacen falta cambiar, o definir bien.

[[attachment:placapic.zip|Descargar .zip]]

=== Lista de componentes ===
||<rowbgcolor="#ffffcc"> '''Resistencias [Ohm]'''||||'''Diodos'''||||'''Capacitores'''||||'''CI'''||||'''Otros'''||
|| R1 470 |||| LED-Power||||C1 0.1uf |||| U2 PIC16F877(/A) |||| BT1 9v ||
|| R2 100 |||| D2 LED-Live |||| C2 0.1uf |||| U4 L293b ||||IC1 ADXL103 ||
|| R3 100 |||| D3 1N4007 |||| C3 220uf |||| U3 GD4049B ||||JP1 RESET ||
|| R4 10k |||| D4 1N4007 |||| C4 47uf |||| U1 LM7805 ||||JP2 SERIAL ||
|| R5 100 |||| D5 1N4004 |||| C5 0.1uf ||||-||||JP3 MOTOR-ENA ||
||R6 100 |||| D6 1N4007 ||||C6 0.1uf ||||-||||MOTOR1 MCC_5v_DER ||
||R7 100 ||||D7 1N4007 |||| C7 27pf ||||-|||| MOTOR2 MCC_5v_IZQ ||
|| R8 2k ||||D8 1N4007 |||| C8 27pf ||||-||||U5 CNY70 ||
||R9 470 ||||D9 1N4007 |||| C9 1uf ||||-||||U6 CNY70 ||
|| R10 330 ||||D10 1N4007 |||| C10 0.1uf ||||-||||X1 4MHz ||
|| R11 10k ||||D11 1N4148 |||| C11 0.1uf ||||-||||1x zócalo para CI 2x20 pts||
|| R12 330 ||||-||||C12 100uf ||||-||||2x zócalos para CI 2x8 pts||
||R13 10k ||||-|||| C13 1uf ||||-||||Placa de islas o multiproposito, PCB||
||R14 100 ||||-||||C14 0.1uf ||||-||||-||
|| R15 100 ||||-|||| C15 0.1uf ||||-||||-||
||-||||-|||| C16 0.1uf ||||-||||-||
||-||||-|||| C17 0.1uf ||||-||||-||
||-||||-|||| C18 0.1uf ||||-||||-||



'''Hola de datos''' [[http://ww1.microchip.com/downloads/en/devicedoc/30292c.pdf|DataSheet_PIC16F877]]



= Programación del PIC =


[[Programacion|Programación]]





















----
[[RSL | Principal RSL]] | [[GruposRSL | Grupos RSL]]
