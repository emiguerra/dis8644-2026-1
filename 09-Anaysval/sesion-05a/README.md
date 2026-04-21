
# sesion-05a

Las señales binarias son la forma más básica de representar información en electrónica digital.

Solo utilizan dos estados:

- 0 → sin voltaje (conectado a tierra)
- 1 → con voltaje (por ejemplo, 9V)
  
En lugar de valores continuos, todo se reduce a encendido o apagado.

Cuando este cambio entre 0 y 1 ocurre muchas veces por segundo, se genera una señal repetitiva. Si el cambio es brusco, se forma una onda cuadrada, que en algunos casos puede transformarse en sonido.

---

### VCV RACK

Es un programa para armar sintetizadores virtuales, basado en módulos que se conectan entre sí. (<https://vcvrack.com/>)
 

- Las conexiones de entrada y salida están marcadas visualmente
- El gate actúa como un interruptor que deja pasar o corta la señal

### Conceptos importantes:

- VC: algo que se controla mediante voltaje
- VCO: genera las ondas (sonido)
- LFO: modifica parámetros lentamente (no se escucha como tono principal)
- VCA: regula la intensidad del sonido
- VCF: cambia el color o carácter del sonido

---

### Formas de onda

- Seno: Es la forma más simple y suave. No tiene cambios bruscos, por eso suena muy limpia, casi como un tono puro sin “textura”. Se percibe más tranquila y estable que las demás.
- Cuadrada: Pasa de un valor a otro de forma instantánea, sin transición. Eso hace que suene más fuerte y artificial, muy asociada a sonidos electrónicos o de videojuegos antiguos.
- Triángulo: Tiene cambios más progresivos que la cuadrada, formando líneas rectas. Suena más suave, pero con un poco más de cuerpo que la senoidal, quedando en un punto intermedio.
- Sierra: Aumenta de forma continua y luego cae de golpe. Esto genera un sonido más intenso y cargado, con mayor riqueza, por lo que se usa para lograr timbres más complejos.

![foto](./imagenes/ondas.png)

---

### Operadores y compuertas lógicas

Las compuertas lógicas permiten tomar decisiones dentro de un circuito usando valores binarios (0 y 1).

- AND → solo entrega 1 si ambas entradas están en 1
- OR → entrega 1 si al menos una entrada es 1
- NOT → cambia el valor (de 1 a 0 o de 0 a 1)
- XOR → da 1 cuando las entradas no coinciden
- NAND → es lo opuesto a AND (solo da 0 cuando ambas son 1)

![foto](./imagenes/compuertas.png)

--- 

### Chip 4093

El 4093 es un circuito integrado usado en electrónica digital. Contiene 4 compuertas NAND en un solo chip.

![foto](./imagenes/chip.png)

### Características principales

- Funciona con lógica binaria (0 y 1)
- Cada compuerta es del tipo NAND
  
Incluye Schmitt Trigger, lo que ayuda a:
- Limpiar señales inestables
- Evitar errores cuando la señal no es totalmente clara

### Alimentación

- Pin 14 → VCC (voltaje, por ejemplo 9V o 5V)
- Pin 7 → GND (tierra)

### Cada compuerta tiene 2 entradas y 1 salida:

### Compuerta 1
Pin 1 → Entrada A

Pin 2 → Entrada B

Pin 3 → Salida

### Compuerta 2

Pin 5 → Entrada A

Pin 6 → Entrada B

Pin 4 → Salida

### Compuerta 3

Pin 8 → Entrada A

Pin 9 → Entrada B

Pin 10 → Salida

### Compuerta 4

Pin 12 → Entrada A

Pin 13 → Entrada B

Pin 11 → Salida

### Ejercicio en clases, Chip 4093 y LM386

(El LM386 es un chip que sirve para amplificar sonido)

1.

![foto](./imagenes/1ejercicio.png)

https://github.com/user-attachments/assets/7972a218-3298-45f0-bc73-7c43239d7af1

2.

![foto](./imagenes/2ejercicio.png)

https://github.com/user-attachments/assets/e290eba7-55d4-4366-a099-6e7fa46869db

Video extra porque el sonido que emitía nos recordaba a Poker Face de Lady Gaga ヾ(´〇`)ﾉ🎙️✮⋆˙

https://github.com/user-attachments/assets/f3506c61-66a7-4dbe-b8a6-f8025571b7f6
