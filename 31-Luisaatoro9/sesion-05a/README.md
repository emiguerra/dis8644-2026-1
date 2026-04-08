# sesion-05a Martes 07 de Abril del 2026

**Sintetizador Modular y Amplificación**

Hoy trabajamos en la evolución del sintetizador físico, integrando lógica digital y potencia de audio.
1. Los "Cerebros" del Circuito: CD4093 y LM386

* **CD4093 (Oscilador):** Es un chip de 14 patas que contiene 4 compuertas NAND. Lo usamos para generar el sonido.
        Pata 14: Positivo (++).
        Pata 7: Negativo (−−).
<img width="500" height="800" alt="Removed Background-0" src="https://github.com/user-attachments/assets/ed0cb707-4a90-4c0f-b7b1-96a914aafad4" />
<img width="500" height="440" alt="4093_Pinout-white" src="https://github.com/user-attachments/assets/c6e56f57-eb49-4b3e-b2dc-f09cc2aa95d6" />

* **LM386 (Amplificador):** Es el chip que actúa como un megáfono. Toma la señal débil del 4093 y le da fuerza para que el parlante suene fuerte.
<img width="400" height="1440" alt="Removed Background-0(1)" src="https://github.com/user-attachments/assets/bc16ad0f-bad3-4400-a343-bcfa98139792" />
 <img width="450" height="1440" alt="Removed Background-0(1)" src="https://github.com/user-attachments/assets/5e1e53c5-3e31-4e1a-806b-4304bbb466f3" />

# Circuito Sonoro Lab / Construye - Explora - Crea 
Es un proyecto de Chile (creado por Claudia González) que es un referente súper importante. 
En la sesión de hoy exploramos el trabajo de Circuito Sonoro Lab, un espacio de experimentación que se dedica a la creación de dispositivos sonoros electrónicos de forma artesanal.

* **¿Por qué es relevante?:** Su enfoque en el Low-Tech y el uso de chips como el CD4093 (el mismo que estamos usando) demuestra que no se necesita tecnología carísima para crear texturas sonoras complejas.
  🎹 ¿Cómo creas texturas con tu circuito?

¿Qué sifinifica hacer texturas ?

    Al girar RV1 (el tono), cambias el grosor del sonido.
    Al girar RV2 (el ritmo), rompes el sonido en pedazos, creando una textura rítmica.
    Si dejas los cables un poco sueltos o tocas el chip con los dedos, agregas "suciedad" o interferencia, que es otra capa de textura.

* **Aprendizaje Clave:** Nos inspiramos en su estética y en la idea de la modularidad. Ellos ven el circuito no solo como algo técnico, sino como un instrumento musical que se puede "tocar" y modificar.
* **Conexión con mi proyecto:** Al igual que en sus laboratorios, estamos aprendiendo a domar la electricidad para que se convierta en ritmo y ruido, pasando de lo teórico a lo táctil en el protoboard.

  **💡 Dato importante**
Circuito Sonoro Lab es un ejemplo de Arqueología de Medios, porque a veces usan piezas de aparatos viejos (como la radio antigua que ocupé en el encargo anterior 📻) para crear instrumentos nuevos.
<img width="950" height="938" alt="image" src="https://github.com/user-attachments/assets/4a06b911-8346-4c9b-b71d-d05fb89cdc10" />
<img width="350" height="915" alt="image" src="https://github.com/user-attachments/assets/ac8e47cf-7e2c-444d-8ab1-449d20421470" />
<img width="600" height="980" alt="image" src="https://github.com/user-attachments/assets/e93b0617-23b4-4979-8d76-e01d9713c120" />


# VCV Rack (The Eurorack Simulator) Es el software de código abierto que simula sintetizadores modulares bajo el estándar Eurorack.
El profesor recomendó este recurso como la plataforma líder para la simulación de sintetizadores modulares en computadoras (Windows, Mac y Linux).

1. **¿De qué trata?:** Es un software de código abierto que emula el estándar Eurorack (el sistema físico de sintetizadores por módulos).
2. **Funcionalidad:** Permite a los usuarios elegir entre miles de módulos virtuales (osciladores, filtros, amplificadores) y conectarlos mediante cables virtuales para generar sonidos complejos.

   **Observación** Nos sirvio como un laboratorio de experimentación para entender el flujo de la señal (signal flow) y la lógica modular sin necesidad de tener el hardware físico costoso. Es el puente perfecto entre la teoría del sonido y la práctica en el protoboard con el CD4093 y el LM386. **"Entorno de Código Abierto" (Open Source)**

<img width="1681" height="916" alt="image" src="https://github.com/user-attachments/assets/cc086514-5fbc-4b3a-b0b1-cea6e1f2dba8" />
<img width="500" height="983" alt="image" src="https://github.com/user-attachments/assets/cb659005-2638-4e54-8f89-4a5f04c1ca90" />
<img width="500" height="1012" alt="image" src="https://github.com/user-attachments/assets/6f41a645-31e9-4aca-81f6-cad6ecafeebc" />

**💡 Diferencia Clave:** Algo que note es que mientras que en VCV Rack las conexiones son virtuales y los componentes son ideales (sin errores), en nuestro protoboard físico con el CD4093 y el LM386 nos enfrentamos a desafíos reales como el ruido eléctrico, la polaridad de los capacitores y la duración de la batería.


# Ejercicios en clases
Primer ejercicio, para entender bien lo que estamos haciendo, decidí detallar cada punto del circuito uno por uno. Prefiero desglosar el funcionamiento de cada chip y sus componentes porque así se me quedan mejor los conceptos de lógica y flujo de señal.
**Observaciones:** Lo más difícil aquí fue no equivocarse con las patas de los chips y acordarse de que los capacitores tienen lado positivo y negativo. Si los pongo al revés, no suena nada :( tambien no tengo que confundir la de 1k (Marrón-Negro-Rojo) con otras. Si pongo una muy grande en el LED, casi no va a alumbrar. Algo que ahora ya se me quedó grabado es que en el potenciómetro (RV1), la pata que controla el tono es la del medio. Si conecto solo las de los lados, la perilla no va a hacer nada.

 **El sonido:** Usamos una de las cuatro compuertas del chip 4093 (la U2A) para crear la señal sonora. Conectamos un potenciómetro de 100k y un capacitor de 1uF para controlar qué tan rápido "vibra" la señal. Básicamente, si giramos la perilla, el sonido se vuelve más agudo o más grave.
 
 **El indicador visual:** Pusimos un LED con una resistencia de 1k a la salida del chip para ver el ritmo. Si el sonido es muy bajo, se ve el parpadeo; si es alto, el LED se queda prendido fijo.
 
 **Amplificación:** Como la señal del 4093 es muy bajita, la pasamos al chip LM386. Este chip actúa como un megáfono: recibe el pulso débil y le da la fuerza necesaria para que el parlante suene bien.
 
 **Limpieza de señal:** Usamos varios capacitores electrolíticos (los que parecen botellitas) para quitar el ruido de la batería y para que el sonido que llega al parlante sea más estable.
<img width="1275" height="769" alt="miPrimer4093" src="https://github.com/user-attachments/assets/7f316419-24ce-4339-b756-0adad1790156" />


Segundo ejercicio en el cual 
<img width="1275" height="380" alt="miSegundo4093" src="https://github.com/user-attachments/assets/3d0b8aac-fe42-4404-95e5-f6621e6225be" />







3. Modulación: El "Director de Orquesta"

Hicimos una modificación clave conectando dos osciladores en cadena:

1. Oscilador 1 (Ritmo): Usa un capacitor de 10μF10μF (C5). Es más lento. Controla el "pulso" o los "beeps".
2. Oscilador 2 (Tono): Usa un capacitor de 1μF1μF (C3). Es más rápido. Controla si el sonido es agudo o grave.
3. El Puente: Conectamos la salida del primero (Pin 11) a la entrada del segundo (Pin 1). Ahora el ritmo "manda" sobre el sonido.

3. Componentes y Conexiones

1. Potenciómetros (100k100k): Usamos dos. Uno para la velocidad del ritmo (RV2) y otro para la nota musical (RV1).
2. Capacitores Electrolíticos: Aprendimos que tienen polaridad. La pata larga es el positivo (++) y la franja blanca marca el negativo (−−).
3. Resistencias de 1k1k: Identificadas por los colores Marrón-Negro-Rojo. Las usamos para proteger los LEDs y conectar los chips.

4. VCV Rack vs. Protoboard

Aprendimos que el VCV Rack es el simulador (software) donde probamos módulos virtuales, mientras que en el protoboard estamos armando el hardware real con cables y chips.

🔊 Implementación Física vs. Simulación Virtual

En esta sesión comparamos el trabajo en el protoboard (Hardware) con el software VCV Rack (Software):
1. Amplificador Físico: El Chip LM386

A diferencia de los módulos virtuales, el LM386 es un componente electrónico real de 8 patas que instalamos físicamente en el protoboard.

    Función: Actúa como un "megáfono" para el circuito. Toma la señal eléctrica débil generada por el oscilador (CD4093) y le da la potencia necesaria para mover físicamente el cono del parlante.
    Conexión Crítica: La señal entra por el Pin 3 y sale amplificada por el Pin 5 a través de un capacitor de acople de 100μF100μF.

2. VCV Rack: El Laboratorio Virtual

Usamos el software VCV Rack como una herramienta de experimentación modular.

    Simulación: En el programa, los módulos de VCO (osciladores) y VCA (amplificadores) son digitales y se conectan con cables virtuales.
    Utilidad: Nos sirve para entender la ruta de la señal (signal flow) antes de pasar a soldar o armar el hardware real.

Conclusión: Mientras que en VCV Rack solo conectamos funciones, en el protoboard con el LM386 nos enfrentamos a desafíos físicos reales como la polaridad de los componentes, el ruido eléctrico y la gestión de la energía de la batería.

* **VCV Rack (Sintetizador Modular Virtual**) Es el software que nos permite experimentar con el sonido sin necesidad de tener las máquinas físicas. Funciona por "módulos" que se conectan con cables virtuales. Es clave porque nos enseña que el sonido se puede separar en funciones (tono, volumen, timbre) y nosotros decidimos cómo mezclarlas.
