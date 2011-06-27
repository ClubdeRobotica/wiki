{{attachment:Fuente - Version 0.1.jpg|Fuente - Version 0.1.jpg}}

El circuito propuesto está basado en la hoja de datos de los reguladores de tensión LM78XX. Mediante el análisis y la simulación (realizada en NI Multisim 10) se obtiene que para una potencia de salida 10W (2A-5V), el transistor PNP TIP42 (TO-220) disipará aprox. 13W (1.8A-7V). Según la hoja de datos del transistor, no soporta mas de 2W sin utilizar un disipador. Utilizando un disipador ZD-5 cuya resistencia térmica es 5ºC/W y un buen acoplamiento con grasa siliconada, el transistor podría disipar hasta 17W sin destruirse. Si los dispositivos alimentados por esta fuente no superarán las condiciones planteadas (Po=10W), es viable la construcción del circuito.

Realizando el mismo análisis de potencia para el regulador LM7805, se concluye que el mismo puede funcionar sin necesidad de disipador ya que su potencia disipada entra dentro de las especificaciones, aunque de ser necesario puede aumentarse la resistencia R1 (5.6 ohm, 6.8 ohm) para disminuir la corriente que circula por el regulador. Esta corriente es un 10% de la Itotal en el circuito propuesto.

Debido al bajo rendimiento de esta fuente lineal (42%), se vuelve indispensable la utilización de una fuente conmutada en las sucesivas mejoras del proyecto.

'''__Circuito de protección contra sobrecorriente__''' {{attachment:Proteccion sobrecorriente.jpg|Proteccion sobrecorriente.jpg}}

El circuito de la figura se compone de un amplificador operacional dual LM358 (de bajo offset), un SCR (MCR100 o similar), transistor PNP de baja potencia, un pulsador (J1, Normal Cerrado) y un relé inversor (representado por K1 en la figura). Cuando por la resistencia sensora R2 (0.05ohm) del esquema de principio de página circula una corriente de 2A, se genera una caída de tensión de 0.1V. Esta tensión es amplificada por el primer AO configurado como amplificador inversor con una ganancia de 48 (1+ 470k/10k). El segundo AO se configura como comparador, donde la entrada positiva es la salida del AO anterior y a la entrada negativa se regula una tensión de aproximadamente 4.8V con un potenciómetro. Cuando la salida del comparador es positiva (se calibra para la corriente deseada sobre R sensora, en este caso 2A) se dispara el SCR y el transistor conduce (las resistencias R8 y R9 se calculan en base al SCR). El relé inversor se activará y se interrumpirá la alimentación del circuito regulador, indicandose el estado de sobrecorriente mediante un led. Para reestablecer el circuito, se presiona el pulsador NC de la base del transistor y el SCR se desengancha. Si la corriente del circuito principal sigue siendo excesiva, se activará nuevamente la protección y asi sucesivamente.

La conexión del rele inversor es la siguiente:

{{attachment:Rele.jpg}}

Donde R12 y el Led correspondiente equivalen a R4 y el led verde del primer circuito. El fusible sirve de protección ante transitorios rápidos y puede ser de 3A. El relé debería ser del tipo SPDT para pcb, de unos 3A y 12V para la bobina.
