== Sistema de Navegación INS/GPS y AHRS para Vehículos Aéreos no Tripulados Controlados ==

Se trata de un sistema de navegación inercial (INS) con soporte de GPS, y referencia de actitud y rumbo (AHRS). Entrega como salida un vector de variables de estado correspondientes a la actitud del vehículo (orientación en un marco de referencia), su rumbo (respecto del norte), y su posición GPS (LLT + PPS para sincronismo). Está inspirado fuertemente en sistemas de alta disponibilidad para vuelo (redundancia, simplicidad, robustez, etc.). El sistema implementa actualmente un filtro MARG. El objetivo del sistema es servir de fuente de información para que un vehículo aéreo no tripulado pueda volar de forma autónoma -no es un controlador, es sólo un sensor-. También tiene aplicación en otras áreas como: robótica, rehabilitación, automovilismo, industria naval, construcción, agronomía de precisión, etc.

=== Título original (proyecto final de grado): "Corrección de AHRS usando fusión de sensores" ===

{{{#!wiki note

''' Proyecto presentado en Expotrónica 2014, ganador del Premio UIC a los Proyectos Universitarios (feria de prototipos): ''' [[attachment:Folleto-Correccion_AHRS_Fusion_Fensores-Expotronica-2014.pdf]]

}}}

{{{#!wiki note

''' Proyecto enviado al concurso Innovar 2014, ganador en la categoría "Innovación en la Universidad", se expuso en Tecnópolis entre los días 11 y 13 de Noviebre: ''' [[attachment:AHRS-AB-MAR_Flyer-Tecnopolis.pdf]]

}}}

'''Divulgación'''

[[https://picasaweb.google.com/111965233620023947875/Expotronica2014?authkey=Gv1sRgCOXa8O3R3ufpigE|Premio en Expotrónica 2014]]
[[https://plus.google.com/u/0/photos/111965233620023947875/albums/6081647573569717905?authkey=CJbnsdvimPqYnAE|Premio INNOVAR 2014]]
[[https://picasaweb.google.com/111965233620023947875/PFDivulgacion?authkey=Gv1sRgCIf7pNnTn8Ws7wE|Demo LCE UTN-FRC]]

'''Videos demostrativos'''

<<YouTube(id=amFIGsXWszw)>>

<<YouTube(id=SHOHCvFu0cs)>>

<<YouTube(id=HtqoTNLiiGI)>>

'''Sistema INS/GPS completo'''

||<tablewidth="100%" tablestyle="text-align: left"100%  style="border:medium none; ;text-align: left"> {{attachment:Sistema-INS-GPS.jpg||width="650"}} ||


'''HMI'''

||<tablewidth="100%" tablestyle="text-align: left"100%  style="border:medium none; ;text-align: left"> {{attachment:isr-gui_1.png||width="650"}} ||

'''Trimble GPS Studio''' Una tarde con buena visibilidad

||<tablewidth="100%" tablestyle="text-align: left"100%  style="border:medium none; ;text-align: left"> {{attachment:campillo3.png||width="650"}} ||

'''Simulación (datos sintéticos):''' fusión de aceleración sensada (a) con la calculada (ac)

||<tablewidth="100%" tablestyle="text-align: left"100%  style="border:medium none; ;text-align: left"> {{attachment:sfusim.png||width="650"}} ||

''' 1er Ensayo IMUn(marg) vs IMUr(TiltAng=f(Incl) (2014)'''

<<YouTube(id=cQV8eSwq85A)>>

'''Demostrador tecnológico (2012)'''

<<YouTube(id=7VWxRLxSwqs)>>

'''Tecnologías involucradas'''

PicLAB/SDCC, QT, KiCAD, Jenkins, Achievo, SVN, Octave, GNUPlot, OpenGL, Blender, GNU/Linux

'''Antecedentes'''

[[http://www.fitc.unc.edu.ar/Eventos.html#Proyecto2005 | Concurso de Proyectos ITC 2005]]

'''Agradecimientos'''

Al Departamento de Ingeniería Electrónica, CIII, LCE, y a todos los docentes, compañeros, colegas, amigos y familiares que apoyan el proyecto.

'''Responsables del proyecto'''

Ing. Andrés Buraschi <<MailTo(andres DOT buraschi AT SPAMFREE gmail DOT com)>>

Ing. Marco Alvarez Reyna <<MailTo(marcoar AT SPAMFREE cdr DOT usla DOT org DOT ar)>>

UTN - FRC
