== Gestor de Energía y Servicios ==

=== Sistema energético: ===

Requerimientos de diseño:

---> Fase 1:

Batería/s + fuente lineal:

 * fuente primaria (entrada): 12[V], ~7Ah
 * fuente secundaria #1 (salida): 5[V] @ pot>5[W] (Imáx>1[A]) Nota: Ya está implementada en la placa de control V1.0
 * fuente secundaria #2 (salida): 9[V] @ 20[W] aprox. (2.22[A]) PENDIENTE

---> Fase 2 y 3:

Batería/s + fuente conmutada (driver potencia, interfaces), fuente lineal (uControlador):

 * fuente primaria (entrada): 12[V], ~7Ah
 * fuente secundaria #1 (salida): 5[V] @ pot>10[W] (Imáx>2[A]) PENDIENTE
 * fuente secundaria #2 (salida): características pendientes, depende del tipo de driver de potencia que utilicemos para los motores en estas fases. PENDIENTE

Común a todas las fases: Diseñar los conductores/conectores para que soporten 4[A]@5[V] y 6[A]@~12[V]

'''Tips para el diseño:'''

- Baterías: tipos, características, parámetros, criterios de selección;

- Protección;

- Fuente conmutada;

- Regulador lineal de tensión;

- Cargador de batería;
