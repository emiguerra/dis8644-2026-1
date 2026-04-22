# sesion-05a

## Apuntes en clase ##

### ¿Qué es un sintetizador? ###

Un sintetizador es un sistema (físico o digital) que genera sonido a partir de señales eléctricas. En lugar de reproducir sonidos grabados, los crea mediante distintos módulos como osciladores, filtros y moduladores.

### Oscilador (VCO) ###

+ El oscilador es la base del sonido en un sintetizador.

+ Genera una señal eléctrica repetitiva (onda).
Esa señal se transforma en sonido.

Tipos de ondas comunes:

+ Senoidal (suave)
+ Cuadrada (más electrónica)
+ Diente de sierra (más intensa)

El VCO (Voltage Controlled Oscillator) cambia su frecuencia según el voltaje:

+ Más voltaje = sonido más agudo.
  
### LFO (Low Frequency Oscillator) ###

Es un oscilador de baja frecuencia.

+ No se escucha directamente.
+ Se usa para modular otros parámetros.

Ejemplos:

+ Vibrato (variación de tono)
+ Cambios rítmicos en el sonido
  
### VCV Rack y Eurorack ###
+ VCV Rack: simulador digital de sintetizadores modulares.
+ Eurorack: formato físico de sintetizadores modulares.

En ambos casos se conectan módulos como VCO, LFO, filtros, entre otros.

### Chip 4093 ###

![4093](./imagenes/4093.jpg/)

El 4093 es un circuito integrado que contiene:

+ Cuatro puertas lógicas NAND de dos entradas
+ Con tecnología Schmitt Trigger
  
### Lógica NAND ### 

Una puerta NAND funciona así:

+ Solo entrega 0 cuando ambas entradas son 1.
+ En cualquier otro caso, entrega 1.
  
### Schmitt Trigger ###

Es una característica que:

+ Limpia señales inestables o ruidosas.
+ Permite generar oscilaciones de forma simple.
  
### Cómo genera sonido el 4093 ###

Con muy pocos componentes:

+ 1 resistencia o potenciómetro
+ 1 capacitor

Se puede crear un oscilador de onda cuadrada.

Como el chip tiene cuatro puertas:

+ Se pueden hacer varios osciladores.
+ Se pueden conectar entre sí.

Esto permite:

+ Modulación cruzada
+ Sonidos complejos
+ Patrones rítmicos

  + Ventaja: Funciona en un rango amplio de voltaje (3V a 15V), lo que lo hace adecuado para circuitos con batería de 9V.
