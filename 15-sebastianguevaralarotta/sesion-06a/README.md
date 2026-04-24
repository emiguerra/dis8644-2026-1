# Bitácora de Aprendizaje – OPEN-BEAT KRAFT

Este proyecto no partió como algo completamente claro ni resuelto. La idea de hacer un sintetizador sonaba bien en papel, pero en la práctica fue un proceso mucho más desordenado, lleno de pruebas, errores básicos y momentos donde el circuito simplemente no hacía nada. OPEN-BEAT KRAFT terminó siendo más que un objeto funcional: fue una forma de entender cómo la electrónica realmente se comporta cuando uno deja de verla como teoría y empieza a armarla con las manos. Desde el inicio se propuso trabajar con una lógica modular (reloj, secuenciador, control y sonido), que al principio parecía solo una forma ordenada de avanzar, pero que con el tiempo se volvió clave para no perderse cuando aparecían los errores.

---

## Primer acercamiento: entender antes de conectar

Al comienzo, la intención era seguir el esquema y lograr que todo funcionara rápidamente, pero eso llevó a errores básicos:

* Conectar sin entender completamente
* Asumir que el circuito funcionaría automáticamente
* No revisar funciones de pines

Esto generó momentos donde el circuito estaba armado pero no respondía. A partir de ahí, el proceso cambió: se empezó a analizar cada conexión, entendiendo que el circuito no “funciona solo”, sino que depende de decisiones precisas.

---

## Etapa del reloj (NE555): estabilidad y control del tiempo

El NE555 fue el punto de partida, encargado de generar el pulso (tempo). Los primeros problemas fueron:

* LED que no encendía o quedaba fijo
* Señal inestable
* Ritmo demasiado rápido o demasiado lento

Soluciones aplicadas:

* Uso de capacitor de desacoplo (103)
* Cambio de capacitor de 1uF a 10uF
* Ajuste de resistencia a 1kΩ

Esto permitió estabilizar el circuito. Se entendió que el 555 no solo genera pulsos, sino que traduce componentes físicos en tiempo.

---

## Etapa del secuenciador (CD4017): organización del sistema

Aquí aparecieron errores importantes:

* Orden incorrecto de LEDs
* Secuencia incompleta
* Circuito detenido

Causas y soluciones:

* Pines no están en orden → se mapearon (3, 2, 4, 7)
* Pin 13 mal conectado → se llevó a GND
* Reset mal configurado → pin 15 conectado a pin 10

Esto permitió lograr una secuencia estable de 4 pasos.

---

## Etapa de control (Transistores)

Errores comunes:

* Transistores al revés
* Confusión de patas
* Notas que no se activaban

Solución:

* Identificación correcta (emisor, base, colector)
* Uso de resistencia en base

Se entendió el transistor como interruptor controlado.

---

## Etapa de sonido (CD4093)

Problemas:

* Sonidos iguales
* Frecuencias poco controlables

Soluciones:

* Uso de distintos capacitores
* Ajuste con potenciómetros

Aquí se entendió cómo la electrónica se convierte en sonido.

---

## Etapa de amplificación (LM386)

Problemas:

* Sonido muy bajo
* Ruido

Soluciones:

* Uso de dos amplificadores
* Capacitores de filtrado

Se logró una salida audible clara.

---

## Proceso de construcción con cartón (materialidad)

La carcasa no fue algo secundario, sino parte importante del proceso. Se decidió usar cartón por accesibilidad y porque permitía experimentar sin riesgo.

Proceso:

* Corte manual del cartón para formar la estructura
* Armado tipo caja abierta para facilitar acceso
* Perforación superior para potenciómetros
* Espacios laterales para parlantes

Errores comunes:

* Medidas incorrectas al inicio
* Desalineación de componentes
* Falta de espacio para cables

Ajustes:

* Reforzar estructura
* Redistribuir componentes
* Asegurar fijación de parlantes

El resultado fue una carcasa funcional, liviana y coherente con la idea del proyecto.

<img width="695" height="695" alt="20260424_014223" src="https://github.com/user-attachments/assets/0e8789af-10d0-4c63-9653-0e5322341b2c" />

---

## Distribución de componentes (basado en el montaje real)

La disposición se organizó buscando claridad y funcionalidad:

* Parte superior: potenciómetros (control directo del usuario)
* Centro: protoboard principal (circuito base)
* Parte inferior: LEDs (visualización del sistema)
* Laterales: parlantes (salida de audio)

Esto permitió:

* Separar visualmente las funciones
* Facilitar el acceso y la manipulación
* Evitar cruces innecesarios de cables

El orden físico ayudó directamente al entendimiento del circuito.

<img width="695" height="695" alt="20260424_014353" src="https://github.com/user-attachments/assets/1feb18db-d19f-4df5-9eba-8c70db1621ea" />

---

## Trabajo en equipo en la construcción

El trabajo no fue individual. Durante el proceso:

* Se dividieron tareas (cableado, montaje, prueba)
* Se discutieron errores y soluciones
* Se validaron decisiones entre todos

Situaciones comunes:

* Uno armaba, otro revisaba
* Alguien encontraba errores que otro no veía
* Se probaban distintas soluciones en paralelo

Esto permitió avanzar más rápido y aprender mejor. El circuito no se resolvió por una sola persona, sino por la combinación de miradas.

<img width="825" height="825" alt="20260424_013847" src="https://github.com/user-attachments/assets/ac07f27c-7747-4dfe-9d8d-f4bfea96208a" />

---

## Reflexión final: integración de conocimientos y aprendizaje desde el error

Al revisar todo el proceso del OPEN-BEAT KRAFT, queda claro que el aprendizaje no fue lineal ni limpio, sino más bien acumulativo y, muchas veces, desordenado. Al inicio, los conocimientos estaban fragmentados: se entendía por separado qué era un oscilador, un contador o un amplificador, pero no cómo se relacionaban entre sí dentro de un sistema real. Fue recién en la práctica, al ver que el circuito no funcionaba como se esperaba, donde se empezó a integrar realmente ese conocimiento.

Uno de los puntos más importantes fue darse cuenta de que la electrónica no funciona por partes aisladas, sino como un sistema donde todo depende de todo. Por ejemplo, un problema en el NE555 no solo afectaba el pulso, sino que desordenaba toda la secuencia; un error en el CD4017 hacía que las notas no coincidieran; y una mala conexión en los transistores simplemente bloqueaba el sonido completo. Esto obligó a dejar de pensar en componentes individuales y empezar a entender el circuito como una cadena continua de procesos.

Los errores jugaron un rol clave en este aprendizaje. Muchos de ellos fueron básicos, como conectar mal un transistor, asumir que los pines estaban en orden, o no considerar el ruido en la alimentación. Sin embargo, justamente por ser errores simples, permitieron comprender principios fundamentales:

* No usar un capacitor de desacoplo mostró lo importante que es la estabilidad eléctrica
* Elegir mal un capacitor o resistencia evidenció cómo pequeños cambios afectan todo el comportamiento
* No revisar el datasheet dejó claro que la intuición no siempre es suficiente

A medida que se avanzaba, los errores dejaron de ser solo frustraciones y pasaron a ser parte del método. Cada falla obligaba a revisar, probar y ajustar, generando una comprensión más profunda que simplemente seguir un esquema correcto desde el inicio.

También fue importante integrar lo técnico con lo material. La construcción en cartón y la distribución de los componentes no fueron solo decisiones estéticas, sino que influyeron directamente en el funcionamiento. Un circuito desordenado hacía más difícil encontrar errores, mientras que una buena organización facilitaba tanto el montaje como el análisis. Esto mostró que el “cómo se construye” es tan importante como el “qué se construye”.

El trabajo en equipo aportó a esta integración de conocimientos. Muchas veces, lo que una persona no lograba identificar, otra lo veía rápidamente. Esto permitió contrastar ideas, validar decisiones y avanzar de forma más eficiente. El aprendizaje dejó de ser individual y pasó a ser compartido, enriqueciendo el proceso completo.

En conjunto, el proyecto permitió entender que aprender electrónica no es solo memorizar funciones o seguir instrucciones, sino relacionar conceptos, experimentar con ellos y enfrentarse a sus límites en la práctica. El resultado final —un sintetizador funcional— es importante, pero lo realmente significativo es haber logrado conectar teoría, práctica, error y colaboración en un mismo proceso.

Más que llegar a una solución perfecta, el proyecto enseñó a pensar, probar y corregir, que es finalmente lo que permite construir cualquier sistema electrónico real.

