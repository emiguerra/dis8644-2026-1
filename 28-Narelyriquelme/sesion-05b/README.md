# sesion-05b
## Apuntes 10 abr
![apuntes](./imagenes/apuntes.jpg)

## utilizamos un chip nuevo
![chip](./imagenes/chip-4017.png)

## Circuito Secuenciador de Luces
![circuito](./imagenes/ejercicio-clases.png)

**Generador de Reloj:** es la parte izquierda del diagrama y se encarga de marcar el ritmo de las luces.
+ Componente Central: Se utiliza un temporizador 555 configurado en modo astable.
+ Funcionamiento: Genera un pulso constante de voltaje a través de su pin 3.
+ Ajuste de Velocidad: El ritmo del pulso es controlado por el condensador C1 y el potenciómetro RV1. Al variar la perilla de RV1, el pulso se vuelve más rápido o más lento.

**El Secuenciador:** Esta es la parte derecha del circuito, encargada de encender las luces en orden.
+ Componente Central: Utiliza el chip CD4017, que es un contador de décadas con 10 salidas posibles (Q0 a Q9).
+ Sincronización: El pulso del 555 entra al pin 14 (CLK) del 4017; cada pulso indica al chip que avance un paso.
+ Secuencia Visual: Las salidas Q0, Q1, Q2 y Q3 (pines 3, 2, 4 y 7) se conectan a 4 LEDs, los cuales se irán encendiendo uno por uno.

El circuito izquierdo (555) crea un ritmo que podemos modificar, y el circuito derecho (4017) utiliza esos "latidos" para encender 4 LEDs en fila, creando un ciclo visual infinito.

## Resultados del ejercicio
![Ejercicio](./imagenes/gif-ejercicio.gif)
