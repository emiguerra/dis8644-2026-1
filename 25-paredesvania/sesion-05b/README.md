# sesion-05b 10.04

**UX** aplicado a sistemas electrónicos.

La idea es empezar a pensar no solo en que funcione, sino en **cómo se usa**:
- Qué controla el usuario  
- Qué tan intuitivo es  
- Cómo se entiende la interacción  

Referencia:
- _Push Turn Move_ (interfaces en instrumentos electrónicos)

> “campo de sentido”,es cómo percibimos el sistema (más desde lo estético/experiencial).

## Secuenciadores 

En esta clase empezamos a trabajar con sistemas que **organizan en el tiempo**.

Un secuenciador va activando salidas una por una, siguiendo un orden, lo que permite generar patrones (por ejemplo, luces o sonido).

## Chip 4017

Trabajamos con el **CD4017**, que es un contador de décadas.

![chip](./imagenes/cd4017.png)

Este chip tiene 10 salidas (Q0 a Q9) y las va activando secuencialmente cada vez que recibe un pulso de reloj.

Es decir:
- Llega un pulso → se activa Q0  
- Llega otro → Q1  
- Después Q2…  
- Y así hasta Q9, luego vuelve a empezar  

En el fondo, “va contando” y distribuyendo la señal.

## Clock / Reloj

Para que el 4017 funcione, necesita un **clock** (reloj), que es una señal que marca el ritmo.

Este reloj se puede hacer con:
- 555 
- 4093 

El clock define la velocidad de todo: mientras más rápido, más rápido avanza la secuencia.

![chip](./imagenes/digital-logic.gif)

### Pines importantes

- **CLK (clock)**: donde entra el pulso  
- **CI (clock inhibit)**: detiene el conteo si está activado  
- **MR (reset)**: vuelve todo a la salida inicial  
- **VCC / GND**: alimentación  

CI (Clock Inhibitor) -> si está en alto, el contador se pausa.

Cada salida se activa en orden, generando una especie de recorrido.

Esto se puede usar para:
- Prender LEDs en secuencia  
- Generar ritmos  
- Activar distintos módulos  

### En clase

Hicimos un circuito secuenciador donde los LEDs se iban prendiendo en distintos tiempos según el clock.

![chip](./imagenes/clockgenerator.png)
![chip](./imagenes/aroundtheworld.gif)

Al principio no funcionaba, revisamos varias veces las conexiones y al final el problema era uno que me pasa regularmente, que se me olvida conectar el pin7 del 555 jeje.
