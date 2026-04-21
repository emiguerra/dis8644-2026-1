# sesion-05a  07.04

Trabajar con señales binarias, donde 0 es GND y 1 es voltaje (en nuestro caso, 9V). Cuando estas señales cambian rápidamente, se traducen en una onda cuadrada, que finalmente es lo que podemos escuchar como sonido.

## Operadores y compuertas lógicas

Los operadores lógicos (AND, OR, NOT, etc.) son la base de las compuertas lógicas. Funcionan evaluando condiciones y entregando un resultado binario: verdadero (1) o falso (0).

- **AND (&&)**: solo da 1 cuando ambas entradas son 1  
- **OR (||)**: da 1 si al menos una entrada es 1  
- **NOT (!)**: invierte el valor (1 pasa a 0 y viceversa)  
- **XOR (^)**: da 1 solo si las entradas son distintas  

También aparece la **NAND**, que hace siempre uno, a no ser que le den dos unos, ahí, da cero.

![compuertas](./imagenes/compuertas.png)

## Chip 4093

Trabajamos con el **CD4093**, que contiene 4 compuertas NAND con **Schmitt Trigger**. 

Osciladores: ∼∼∼∼∼∼∼

![4093](./imagenes/4093.png)

- Siempre hay que alimentar el chip con **VCC (9V)**  
- El uso de capacitores ayuda a estabilizar la señal  
- No es necesario usar las 4 compuertas, se puede partir con una  

`Cuando x vale 0 no hay oscilación`

![operador](./imagenes/operador.heic)

### Oscilación y componentes

- El capacitor **acumula y libera carga**, lo que afecta directamente la frecuencia  
- Mientras mayor sea la capacitancia, más lenta es la oscilación  
- Las resistencias también influyen, funcionando como una especie de “filtro”  

> El capacitor como un “guardia en la puerta” que regula qué tan rápido pasan las cosas.

## En clase

![operador](./imagenes/clase1.png)
![ejemplo](./imagenes/clase.heic)

Armamos un circuito usando una compuerta NAND del 4093 para generar un oscilador. Me encantó que lo logré hacer a la primera! creo que estoy entendiendo mucho mejor los esquemáticos.

![operador](./imagenes/clase2.png)
![ejemplo](./imagenes/clasee.heic)

Después hicimos una variación conectando otra compuerta, lo que generaba una especie de “oscilador que controla otro oscilador”

También vimos referencias como:

- <https://moritzkleininstruments.com> 
- <https://alpaca.markets>  

## Encargo: Schmitt Trigger

El Schmitt Trigger apareció como concepto clave dentro del chip que usamos.

Es un comparador con “memoria” que evita errores cuando la señal es inestable o ruidosa. En vez de tener un solo punto de decisión, trabaja con dos umbrales:

- Uno para cuando la señal sube  
- Otro para cuando baja  

Esto evita que el sistema esté cambiando constantemente de estado cuando la señal está justo en el límite.

Yo lo entendí como:

Si un sistema fuera demasiado sensible, cualquier pequeña variación lo haría cambiar de estado todo el tiempo. El Schmitt Trigger maneja ese espacio entre los estados, haciendo que el cambio sea más estable y menos caótico.
