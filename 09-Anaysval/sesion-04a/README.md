# sesion-04a

Volvimos a ver los circuitos astable y monoestable pero invirtiendo el orden de los circuitos.

Atari Punk: Astable → Monoestable

Circuito de hoy: Monoestable → Astable

### Ejercicio en clases

![foto](./imagenes/ejercicioo.jpg)

Trabajé junto a Benjamín, armamos el circuito astable y el monoestable por separado, y ambos funcionaron bien.

### Monoestable

https://github.com/user-attachments/assets/60ec7024-7705-43bf-8d23-72c9b8d586da

### Astable

https://github.com/user-attachments/assets/13f52108-e097-4fbc-bc21-7281ebec68b6

Luego los unimos, pero no funcionó, nos dimos cuenta de que faltaba conectar el positivo y el negativo de las protoboards entre sí.

Conectamos los cables faltantes y funcionó :)

https://github.com/user-attachments/assets/e5e9a725-d0ca-49ae-ae0c-552b8f488e00

Agregamos un potenciometro

https://github.com/user-attachments/assets/2c9f7b53-fa45-42c1-a891-21f487c01d55

---

### Tabla de potencias de 10

![foto](./imagenes/tabla.png)

---

También nos mostraron Falstad que sirve para armar circuitos virtuales (como con protoboard) y ver cómo funcionan en tiempo real: puedes poner resistencias, capacitores, chips, LEDs, etc., y observar cómo circula la corriente o cómo cambian las señales.

https://www.falstad.com/circuit/

---

### Pinout chip 555

![foto](./imagenes/555timer.jpg)

- Pin 1 (GND/Tierra): Tierra o negativo de la alimentación.
- Pin 2 (Trigger/Disparo): Inicia la temporización cuando el voltaje cae por debajo de un tercio del voltaje de alimentación.
- Pin 3 (Output/Salida): Entrega la señal de salida (alto o bajo), puede alimentar LEDs o pequeños dispositivos.
- Pin 4 (Reset/Reinicio): Reinicia el temporizador; si va a negativo se detiene, por eso se conecta a VCC para uso normal.
- Pin 5 (Control Voltage/Voltaje de control): Permite ajustar los niveles internos; normalmente se conecta a tierra con un condensador para evitar ruido.
- Pin 6 (Threshold/Umbral): Detiene la temporización cuando el voltaje supera dos tercios del voltaje de alimentación.
- Pin 7 (Discharge/Descarga): Descarga el condensador para reiniciar el ciclo.
- Pin 8 (VCC/Alimentación): Alimentación positiva (aprox. 4.5V a 15V).

---
### Encargo

- Destripar un dispositvo electrónico, documentar con texto e imagen el proceso, distinguir los elementos de la PCB que hemos estudiado como R y C y chips.
- Documentar las conexiones entre la PCB y los componentes en la carcasa.
- Escribir un texto de 3 párrafos explicando de forma poética imaginaria el funcionamiento especulativo del dispositivo electrónica, usando metáforas y analogías para describir el flujo de electricidad y la interacción de los componentes. el texto debe ser creativo y evocador, transmitiendo la esencia del dispositivo sin ser técnico, ni tampoco necesariamente real.
