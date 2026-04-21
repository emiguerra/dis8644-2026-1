# sesion-05a
Clase 7 de Abril

## Apuntes

<p>La clase empezo con los profesores explicandonos sobre el VCV Rack, la cual es una aplicación de web que es una sintesis modular, la cual esta inspirado en los sintetizadores analógicos físicos. Básicamente es una plataforma para crear sonidos desde cero, en donde cada modulo cumple una función especifica y uno decide cómo se conectaran mediante cables o al menos la imitacion de cables como si fuera un sistema de conexión real o físico. 
No hay una única forma de uso, es totalmente experimental, además de gratuito y permitiendo entender de manera mucho más práctica como funciona la sintesís de sonido. Es utilizado para musica electrónica como para musica más experimental. Se podria considerar el VCV Rack como un **Laboratorio digital** para construir sus propios sintetizadores.</p>

![VCVrack](./imagenes/vcvrack.png)

*imagen referencial de un VCV rack*

<p>Luego en siguiente parte de la clase y que es en lo que más nos enfocamos, nos enseñaron sobre el circuito integrado 4093, el cual contiene 4 compuestos NAND. 
Aqui es importante aclarar algo antes de explicar el 4093, los compuestos operadores (AND, OR, NOT, etc.) son las bases de las compuestas lógicas, son las que evalúan las condiciones y entregan un resultado binario, es decir, verdadero (1) o falso (0).</p>

- **AND**: solo da 1 cuando ambas entradas son 1  
- **OR**: da 1 si al menos una entrada es 1  
- **NOT**: invierte el valor (1 pasa a 0 y viceversa)  
- **XOR**: da 1 solo si las entradas son distintas

## Chip 4093

![chip4093](./imagenes/chip4093.png)

Puntos importantes a considerar sobre el 4093:

- Siempre se alimenta con el **VCC (9V)**
- El uso de capacitadores ayuda bastante a estabilizar la señal
- No es necesario usar las 4 compuertas, podemos partir con solo una
