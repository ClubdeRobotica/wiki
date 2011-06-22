= Gestor de Energía y Servicios =
== Sistema energético: ==
=== Características ===
Algunas características del sistema energético del VRTD deberían ser: alto rendimiento, pequeño volumen, bajo peso, redundante, robusto, estabilidad térmica, gran rango de tensión de entrada, drift pequeño (variación de sus parámetros respecto de la temperatura), con protecciones y capacidad de reportar errores o situaciones límite, modular, baja radiación EMI.

==== Requerimientos de diseño: ====
---> Fase 1:

Batería/s + fuente lineal:

 * fuente primaria (entrada): de 9[v] a 14[V], ~7Ah
 * fuente secundaria #1 (salida): 5[V] @ pot>5[W] (Imáx>1[A]) (nominal)

  . Se adjunta un esquema tentativo de esta fuente. Consta de un regulador 7805 con un transistor que permite mayor consumo de corriente. Posee LED indicador de encendido y posibilidad de adicionar una protección contra sobrecorrientes mediante una R sensora. [[Esquema|ESQUEMA]]
 * fuente secundaria #2 (salida): 5[V] @ pot>2.5[W] (Imáx>1[A]) (redundante)

---> Fase 2:

Batería/s + fuente conmutada (driver potencia, interfaces), fuente lineal (uControlador):

 * fuente primaria (entrada): de 9[v] a 14[V], ~7Ah
 * fuente secundaria #1 (salida): 5[V] @ pot>10[W] (Imáx>2[A]) (nominal)
 * fuente secundaria #1 (salida): 5[V] @ pot>5[W] (Imáx>2[A]) (redundante)

---> Fase 3:

Batería/s + fuente conmutada + monitor de sistema microcontrolado:

 * fuente primaria (entrada): de 9[v] a 14[V], ~7Ah
 * fuente secundaria #1 (salida): 5[V] @ pot>10[W] (Imáx>2[A]) (nominal)
 * fuente secundaria #1 (salida): 5[V] @ pot>5[W] (Imáx>2[A]) (redundante)
 * gestor de energía y monitor de sistema microcontrolado.

Común a todas las fases: Diseñar los conductores/conectores de potencia para que soporten 4[A] @ 5[V] y 14[A] @ 12[V]

'''Tips para el diseño:'''

- [[baterias|Baterías]];

- Protección;

- Fuente conmutada;

- Regulador lineal de tensión;

- Cargador de batería;
