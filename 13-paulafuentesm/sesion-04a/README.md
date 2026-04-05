# sesion-04a
**Apuntes:**

![apuntes](https://github.com/paulafuentesm/dis8644-2026-1/blob/fb6c6fd84c073d6bb9bf61dc91bd68943d7f3a42/13-paulafuentesm/sesion-04a/imagenes/apunte1.jpg)

![apuntes02](https://github.com/paulafuentesm/dis8644-2026-1/blob/fb6c6fd84c073d6bb9bf61dc91bd68943d7f3a42/13-paulafuentesm/sesion-04a/imagenes/apunte2.jpg)

Chip 555:

| N patita | Nombre | Funciòn |
| :---         |     :---:      | :---           |
| 1   | Tierra (GND)     | negativo    |
| 2     | Disparo (Trigger)       |  ciclo de temporización (unido a 6)      |
| 3     | Salida (Output)       | señal de salida del circuito      |
| 4     | Reinicio (Reset)       | reinicia (la salida va a 0)      |
| 5     | Control de Voltaje       | no es necesario conectar      |
| 6     | Umbral (Threshold)       | Finaliza el ciclo de temporización  (unido a 2)    |
| 7     | Descarga (Discharge)       | descargar el capacitor      |
| 8     | Voltaje de alimentación       | positivo      |
| ------------- | ------------- |

-----

***Ejercicio:***

Conectar Circuitos MS a AS

+ Verde: Monoastable
  
+ Naranjo: Astable
  
![ejercicio](https://github.com/paulafuentesm/dis8644-2026-1/blob/c8e0f15690830b4e5794ca5f498205d97fc2d3f1/13-paulafuentesm/sesion-04a/imagenes/ejercicio_clase/ejercicio.jpg)
Imagen: Usuario Cifuv

![aplicacion](https://github.com/paulafuentesm/dis8644-2026-1/blob/fb6c6fd84c073d6bb9bf61dc91bd68943d7f3a42/13-paulafuentesm/sesion-04a/imagenes/ejercicio_clase/aplicacion.jpg)

![aplicacion02](https://github.com/paulafuentesm/dis8644-2026-1/blob/fb6c6fd84c073d6bb9bf61dc91bd68943d7f3a42/13-paulafuentesm/sesion-04a/imagenes/ejercicio_clase/aplicacion02.jpg)

***Observación:***

+ verificar que todo funcionara correctamente, se comprobó que los LED conectados a cada circuito se encendieran.

Los circuitos se conectan mediante un cable que va desde la pata 3 hacia la pata 2 o 6, utilizando como fuente la batería conectada al circuito astable. Al funcionar el sistema, el parlante emite un sonido agudo y fuerte, cuya intensidad o tono puede regularse mediante el potenciómetro.

-------
***Aparato Electrico***

+ Raton de computadora
  
![raton](https://github.com/paulafuentesm/dis8644-2026-1/blob/c8e0f15690830b4e5794ca5f498205d97fc2d3f1/13-paulafuentesm/sesion-04a/imagenes/aparato_electrico/raton.jpg)

![ratonpcb](https://github.com/paulafuentesm/dis8644-2026-1/blob/c8e0f15690830b4e5794ca5f498205d97fc2d3f1/13-paulafuentesm/sesion-04a/imagenes/aparato_electrico/ratonpcb.jpg)

Componentes:

+ LED rojo:Ilumina la superficie donde se mueve el mouse. La luz rebota en la mesa o alfombrilla.
+ Chip 3510: cómo se movió el mouse y conecta con el PC.
+ R1 – 68R: Limita la corriente que pasa por el LED.
+ C1 – condensador electrolítico (filtra la alimentación).
+ CE2 – 10 µF – condensador electrolítico para estabilizar el voltaje.
+ C2 – 104 (100 nF)
+ Botones: clic izquierdo y derecho

Explicaciòn:

Al abrir el dispositivo parece un pequeño raton. No corre por túneles de tierra, sino por caminos de cobre donde la electricidad avanza como si fueran sus patas diminutas. El chip es el cerebro del animal, tratando de entender hacia dónde moverse, mientras la corriente eléctrica va y viene como si fueran pequeños impulsos nerviosos que le dicen “avanza”, “detente” o “mira hacia otro lado” para poder sobrevivir.

Los condensadores, pequeños depósitos de energía, donde guarda un poco de electricidad igual que un ratón guarda comida. Cuando hace falta energía, la sueltan lentamente para que todo siga funcionando, mientras que la resiencias lo mantien vivo. 

El LED rojo siendo los ojos del ratón, iluminando el suelo mientras explora. Tal vez ese pequeño ratón eléctrico va observando el mundo debajo de él y, cada vez que se mueve, le cuenta al computador hacia dónde corrió. Moviéndose por sus caminos de cobre mientras explora todo lo que hay bajo su luz. 








