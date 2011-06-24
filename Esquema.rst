{{attachment:Fuente - Version 0.1.jpg|Fuente - Version 0.1.jpg}}

El circuito propuesto está basado en la hoja de datos de los reguladores de tensión LM78XX. Mediante el análisis y la simulación (realizada en NI Multisim 10) se obtiene que para una potencia de salida 10W (2A-5V), el transistor PNP TIP42 (TO-220) disipará aprox. 13W (1.8A-7V). Según la hoja de datos del transistor, no soporta mas de 2W sin utilizar un disipador. Utilizando un disipador ZD-5 cuya resistencia térmica es 5ºC/W y un buen acoplamiento con grasa siliconada, el transistor podría disipar hasta 17W sin destruirse. Si los dispositivos alimentados por esta fuente no superarán las condiciones planteadas (Po=10W), es viable la construcción del circuito.

Realizando el mismo análisis de potencia para el regulador LM7805, se concluye que el mismo puede funcionar sin necesidad de disipador ya que su potencia disipada entra dentro de las especificaciones, aunque de ser necesario puede aumentarse la resistencia R1 (5.6 ohm, 6.8 ohm) para disminuir la corriente que circula por el regulador. Esta corriente es un 10% de la Itotal en el circuito propuesto.

Debido al bajo rendimiento de esta fuente lineal (42%), se vuelve indispensable la utilización de una fuente conmutada en las sucesivas mejoras del proyecto.
