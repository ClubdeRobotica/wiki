= Gestor de Energía y Servicios =

== Sistema energético: ==

=== Características ===

Algunas características del sistema energético del VRTD deberían ser: alto rendimiento, pequeño volumen, bajo peso, redundante, robusto, estabilidad térmica, gran rango de tensión de entrada, drift pequeño (variación de sus parámetros respecto de la temperatura), con protecciones y capacidad de reportar errores o situaciones límite, modular, baja radiación EMI.


==== Requerimientos de diseño: ====

---> Fase 1:

Batería/s + fuente lineal:

 * fuente primaria (entrada): de 9[v] a 14[V], ~7Ah
 * fuente secundaria #1 (salida): 5[V] @ pot>5[W] (Imáx>1[A])
 * fuente secundaria #2 (salida): 5[V] @ pot>2.5[W] (Imáx>1[A])

---> Fase 2 y 3:

Batería/s + fuente conmutada (driver potencia, interfaces), fuente lineal (uControlador):

 * fuente primaria (entrada): de 9[v] a 14[V], ~7Ah
 * fuente secundaria #1 (salida): 5[V] @ pot>10[W] (Imáx>2[A])
 * fuente secundaria #1 (salida): 5[V] @ pot>5[W] (Imáx>2[A])

Común a todas las fases: Diseñar los conductores/conectores de potencia para que soporten 4[A] @ 5[V] y 14[A] @ 12[V]

'''Tips para el diseño:'''

- Baterías;

- Protección;

- Fuente conmutada;

- Regulador lineal de tensión;

- Cargador de batería;
