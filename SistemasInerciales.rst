== Sistema de Navegación INS/GPS para un Vehículo Aéreo no Tripulado Controlado ==

Se trata de un sistema de referencia de actitud y rumbo (AHRS por sus siglas en inglés). Entrega como salida un vector de variables de estado correspondientes a la actitud del vehículo (posición angular), su rumbo (respecto del norte), y su posición GPS (LLT + PPS para sincronismo). Está inspirado fuertemente en sistemas de alta disponibilidad para vuelo (redundancia, simplicidad, robustez, etc.). El sistema de información implementa actualmente un filtro MARG. El objetivo del AHRS es servir de fuente de información para que un vehículo aéreo no tripulado pueda volar de forma autónoma -no es un controlador, es sólo un sensor-. También tiene aplicación en otras áreas como: robótica, rehabilitación, automovilismo, industria naval, construcción, etc.

=== Título original (proyecto final de grado): "Corrección de AHRS usando fusión de sensores" ===

{{{#!wiki note

''' Proyecto presentado en Expotrónica 2014, ganador del Premio UIC a los Proyectos Universitarios (feria de prototipos): ''' [[attachment:Folleto-Correccion_AHRS_Fusion_Fensores-Expotronica-2014.pdf]]

}}}

'''Divulgación'''

[[https://picasaweb.google.com/111965233620023947875/Expotronica2014?authkey=Gv1sRgCOXa8O3R3ufpigE|Premio en Expotrónica 2014]]
[[https://picasaweb.google.com/111965233620023947875/PFDivulgacion?authkey=Gv1sRgCIf7pNnTn8Ws7wE|Demo]]

'''Videos demostrativos'''

<<YouTube(id=amFIGsXWszw)>>
<<YouTube(id=SHOHCvFu0cs)>>
<<YouTube(id=HtqoTNLiiGI)>>


'''HMI'''

||<tablewidth="100%" tablestyle="text-align: left"100%  style="border:medium none; ;text-align: left"> {{attachment:isr-gui_1.png||width="650"}} ||

'''Simulación''' (fusión de aceleración sensada:a/calculada:ac)

||<tablewidth="100%" tablestyle="text-align: left"100%  style="border:medium none; ;text-align: left"> {{attachment:sfusim.png||width="650"}} ||

'''Antecedentes'''

[[http://www.fitc.unc.edu.ar/Eventos.html#Proyecto2005 | Concurso de Proyectos ITC 2005]]

'''Responsables del proyecto'''

Ing. Andrés Buraschi <<MailTo(andres DOT buraschi AT SPAMFREE gmail DOT com)>>

Ing. Marco Alvarez Reyna <<MailTo(marcoar AT SPAMFREE cdr DOT usla DOT org DOT ar)>>

UTN - FRC
