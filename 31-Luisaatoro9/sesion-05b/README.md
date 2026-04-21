# sesion-05b: Secuenciadores e Interacción

Viernes 10 de abril del 2026

Esta sesión fue un puente entre la electrónica pura y el diseño de experiencia. Dejamos de pensar solo en "que suene" para empezar a pensar en cómo se organiza el sonido y cómo alguien interactúa con el objeto que estamos construyendo.
### 1. El Secuenciador y la Lógica del 4017

Construimos un secuenciador de pasos usando el chip CD4017. 

* **No genera sonido por sí mismo;** lo que hace es "contar" pulsos de reloj (que le manda un chip 555) y activar una salida a la vez, del 0 al 9.
* **El rol del Schmitt Trigger:**  Para que el 4017 no se equivoque al contar (por el ruido eléctrico o interferencias), necesitamos un Schmitt Trigger. Este componente limpia la señal, asegurando que el pulso sea un "cuadrado" perfecto. Sin esto, la secuencia se saltaría pasos de forma errática. Además, al observar el diagrama técnico del CD4093, identifiqué el símbolo de histéresis dentro de las compuertas. Esto confirma que el chip posee un Schmitt Trigger integrado, lo cual es fundamental para nuestra cadena de señal: el 4093 genera un pulso cuadrado 'limpio' que el secuenciador 4017 puede contar sin errores de lectura por ruido eléctrico.

### 2. Referentes: El Instrumento como Interfaz 
* **Ergonomía y St. Vincent:** Ella diseñó su guitarra pensando en el cuerpo femenino y en la comodidad al tocar. Esto me hizo clic con nuestro proyecto: meter el circuito en una caja de cartón no es solo para esconder los cables, sino para crear una interfaz que invite a ser tocada.
* **David Byrne y la libertad inalámbrica:** En su show American Utopia, Byrne eliminó los cables y los "pedalboards" fijos del suelo. Esto le permitió moverse libremente. Es un referente de cómo la tecnología puede liberar la expresión artística.
* **Banda Marinero:** Ver cómo este dúo chileno aplica estas ideas y usa instrumentos diseñados bajo estos conceptos (como la guitarra de St. Vincent) aterriza toda la teoría a algo real y local.

### Libro Push Turn Move

Entendí que el diseño de un instrumento no es solo estética, sino funcionalidad cognitiva. El libro plantea que existen tres formas básicas de interactuar con el sonido:

1. Push (Pulsar): Acciones momentáneas, como disparar un ritmo o una nota (lo que hacemos con el pulso del 4017).
2. Turn (Girar): Control gradual de parámetros, como el tono o el tempo (lo que hacemos con nuestros potenciómetros).
3. Move (Mover): Relación entre el cuerpo y el espacio (lo que menciona David Byrne al sacar los cables del escenario).

* **Affordance (Invitación al uso):** El diseño de mi instrumento debe decirle al usuario qué hacer sin manuales. Una perilla invita a girar (turn) y un botón a presionar (push).
* **Feedback (Retroalimentación):** El usuario necesita saber que su acción tuvo un efecto. En nuestro circuito, los LEDs son el feedback visual del ritmo que marca el 4017.
* **Memoria Háptica:** Al meter todo en una caja de cartón, buscamos que el usuario aprenda por el tacto dónde están los controles, igual que un músico toca sin mirar.

Esto me hizo click con mi protoboard. Antes veía los potenciómetros como simples resistencias, pero ahora los veo como la interfaz que permite al usuario "dialogar" con el chip. No leí el libro completo aún pero si pude comprender que si el usuario no sabe qué perilla girar, mi diseño de interacción falló, aunque el circuito sea perfecto.

### 3. Reflexión 

Me quedo con la idea de la belleza contextual. No necesitamos materiales caros; estamos transformando cartón y chips básicos en algo complejo. La clave está en cómo gestionamos el voltaje para que se convierta en ritmo y en cómo diseñamos la interacción para que el usuario no necesite un manual para "jugar" con el instrumento.

### Bibliografía

* All About Circuits. (s.f.). *Logic signal voltage levels*. https://www.allaboutcircuits.com/textbook/digital/chpt-3/logic-signal-voltage-levels/
* Bjørn, K. (s.f.). *Push Turn Move: The new book on electronic music instruments*. https://matthewess.com/push-turn-move-the-new-book-on-electronic-music-instruments-by-kim-bjorn/
* Byrne, D. (2010). *How architecture helped music evolve* [Charla]. TED. https://www.ted.com/talks/david_byrne_how_architecture_helped_music_evolve
* CA-RA. (s.f.). *Básicos del Schmitt Trigger: cómo funciona el Schmitt Trigger*. https://ca-ra.org/es/b%C3%A1sicos-del-schmitt-trigger-c%C3%B3mo-funciona-el-schmitt-trigger/
* INCB. (s.f.). *Cómo funciona el 4017*. https://incb.com.mx/index.php/articulos/53-como-funcionan/8859-como-funciona-el-4017-art812s
* Música Popular. (s.f.). *Marineros*. https://www.musicapopular.cl/grupo/marineros/
* Music Man. (s.f.). *St. Vincent 2016*. https://www.music-man.com/instruments/guitars/st-vincent-2016
* Sound On Sound. (s.f.). *Introduction to frequency modulation*. https://www.soundonsound.com/techniques/introduction-frequency-modulation
