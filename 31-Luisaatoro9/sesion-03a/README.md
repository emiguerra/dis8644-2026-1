# sesion-03a 
## Martes 24 de marzo 2026  
### Experimentación Sonora con el Chip 555

En esta sesión dimos un salto de lo visual a lo sonoro. Usamos el circuito integrado 555 en configuración **astable** para generar una oscilación que pudiéramos escuchar. Lo más interesante fue ver cómo componentes tan pequeños cambian por completo el tono del sonido.

---
### Ejercicios 
<img width="1000" height="623" alt="Captura_de_pantalla_2026-03-24_a_las_09 47 56" src="https://github.com/user-attachments/assets/d9670b95-d872-4522-ba14-73a5231b4f03" />
<img width="1000" height="688" alt="Captura_de_pantalla_2026-03-24_a_las_12 08 10" src="https://github.com/user-attachments/assets/2daf1ee7-da9e-44bb-b219-aa2ceb1548b3" />
<img width="1000" height="517" alt="Captura_de_pantalla_2026-03-24_a_las_12 14 58" src="https://github.com/user-attachments/assets/e483a5c5-3280-4889-804b-11374d3348e0" />
<img width="500" height="915" alt="24_03_taller" src="https://github.com/user-attachments/assets/3ac963b1-56db-43f2-bb36-609af208effb" />

### Conexiones y el "Puente" de Salida

Para que el sonido llegara al parlante, fue clave entender el rol del **pin 3** del chip 555. Este pin actúa como un puente de salida que entrega una **señal cuadrada** (pulsos de encendido y apagado).

Al conectar el parlante aquí (pasando por un capacitor para protegerlo), esos pulsos eléctricos se convierten en la vibración mecánica que escuchamos.

---

### Lo que aprendí en el protoboard

- **Frecuencia:**  
  Al mover el potenciómetro, cambiamos la resistencia y, por ende, la velocidad de los pulsos.  
  Más pulsos por segundo = sonido más agudo.

- **Capacitores:**  
  Usamos uno de **100 μF** a la salida.  
  Aprendí que estos componentes almacenan y liberan energía, definiendo qué tan rápido o lento es el ciclo de carga del oscilador.
---
   ### Reflexión: El Sonido como Información
<img width="280" height="1024" alt="Jose Vicente Asuar" src="https://github.com/user-attachments/assets/facab515-c803-4dbd-a765-3b44ac517696" />
<img width="700" height="420" alt="jcr-content-5" src="https://github.com/user-attachments/assets/44ac7422-15a7-4cc5-9fb7-a3df61d3aabb" />

Al ver el documental de José Vicente Asuar, me cambió la forma de entender el sonido. Normalmente uno piensa en la música como algo puramente artístico, pero Asuar lo plantea como una forma de información compleja que se puede codificar, interpretar y visualizar.

Me impactó ver cómo en Chile, con las limitaciones de esa época, se logró integrar la música con los primeros computadores. No es algo que se enseñe mucho, pero es una parte clave de nuestra historia técnica. Me hace reflexionar sobre cómo hoy tenemos toda la tecnología al alcance y la normalizamos, pero en el fondo, que un computador funcione y procese datos para crear arte es algo increíble que nació de la pura exploración.

Conexión técnica con el taller: Lo que más me resonó fue la idea de construir desde la experimentación. Asuar trabajaba con "prueba y error", ajustando componentes electrónicos para encontrar nuevos timbres. Eso conecta directamente con lo que hacemos en clase:

1. Ajuste de parámetros: Al igual que Asuar configuraba sus sintetizadores, nosotros ajustamos resistencias y capacitores para cambiar la frecuencia.
2. Límites del hardware: Él usaba las limitaciones de las máquinas para crear; nosotros estamos entendiendo cómo el pin 3 del 555 entrega una señal cuadrada que, aunque es "digital" (encendido/apagado), se convierte en algo orgánico que escuchamos.

### Bibliografía y Referentes

* Arreguín Ponce, E. I. (2020). *Oscilador 555 (astable y monostable)* [Video]. YouTube. https://www.youtube.com/watch?v=sJ9EZWBZee8

* Astra AI. (s.f.). *Chat sobre informática*. Recuperado de https://app.astra-ai.co/?subject=informatics&chatId=Ep_4i7X749zaKNEgPQ5tn

* Electronics Tutorials. (s.f.). *555 Oscillator Tutorial*. Recuperado de https://www.electronics-tutorials.ws/waveforms/555_oscillator.html

* El Mostrador. (2023, marzo 28). *José Vicente Asuar: el legado del padre de la música electroacústica en Chile*. Recuperado de https://www.elmostrador.cl/cultura/2023/03/28/jose-vicente-asuar-el-legado-del-padre-de-la-musica-electroacustica-en-chile/

* 555 Timer Circuits. (s.f.). *Toy Organ using 555 Timer*. Recuperado de https://www.555-timer-circuits.com/toy-organ.html#google_vignette
