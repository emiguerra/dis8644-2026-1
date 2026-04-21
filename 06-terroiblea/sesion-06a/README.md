# sesion-06a

Martes 14 de Abril, 2026. 

Nota del día: full en proyecto. 

## Referentes (y otras cosas)

- **Nate Gentile** (hace computadores) (nombre real José Ignacio Gentile Meriggi) es un ingeniero de software, emprendedor y creador de contenido (youtuber) uruguayo con más de tres millones de suscriptores en su canal homónimo dedicado a la informática doméstica, especialmente al análisis y montaje de potentes equipos y componentes. <https://www.youtube.com/channel/UC36xmz34q02JYaZYKrMwXng>
- **Pandoc** (transformar documentos de markdown a otro formato) es un conversor de documentos libre y de código abierto, mayormente usado como una herramienta de escritura (especialmente por académicos), y es una base para la publicación de flujos de trabajo. Fue creado originalmente por John MacFarlane, un profesor de Filosofía en la Universidad de California, Berkeley.
- **LaTex** es un sistema de composición tipográfica de alta calidad. Incluye características especialmente diseñadas para la producción de documentación científica y técnica. (pronunciado habitualmente como "lay-tek") A diferencia de los procesadores de texto tradicionales como Word (donde lo que ves es lo que obtienes), en LaTeX escribes código de marcado que luego se "compila" para generar un archivo final, normalmente un PDF. Es el estándar de facto en el mundo académico para escribir tesis, artículos de investigación y libros de matemáticas o física.
- **Leslie Lamport** es un matemático y científico de la computación estadounidense. Es especialmente conocido por sus trabajos en sistemas distribuidos y por ser el desarrollador inicial del sistema de formateo de textos LaTeX, y de BibTeX.​ 
- **Mauricio Loyola** (arquitectura con mención en computación) Es docente, investigador y consultor en tecnologías digitales para el diseño, arquitectura y construcción. Sus áreas de trabajo incluyen análitica del diseño, ciencias de datos, internet de las cosas, electrónica y computación física. 
- **Jorge Gómez Mir** es un ingeniero civil electrónico e investigador chileno, especializado en dispositivos semiconductores y nanoelectrónica de baja potencia. 
Actualmente, se desempeña como Profesor Asistente en la Facultad de Ingeniería y Ciencias Aplicadas de la Universidad de los Andes en Chile, donde imparte cátedras sobre Arquitectura de Computadores y Sistemas Embebidos.

## Qué aprendí hoy

### Schmitt trigger 

Es un tipo de comparador electrónico que utiliza la retroalimentación positiva para convertir una señal de entrada analógica "ruidosa" en una señal de salida digital limpia y definida. A diferencia de un comparador estándar, que tiene un solo nivel de umbral, el Schmitt Trigger utiliza dos niveles de voltaje distintos (histéresis) para decidir cuándo cambiar su estado. 

La característica clave es la histéresis, que evita que pequeñas variaciones de ruido causen múltiples cambios rápidos e indeseados en la salida. 

- **Umbral Superior (UTP):** La salida cambia de "bajo" a "alto" solo cuando la entrada supera este valor.
- **Umbral Inferior (LTP):** La salida cambia de "alto" a "bajo" solo cuando la entrada cae por debajo de este valor.
- **Zona Muerta:** Entre estos dos umbrales, el circuito mantiene su estado actual, ignorando pequeñas fluctuaciones. 

Explicado de forma simple y con ejemplo:

Imagina que estás en un tobogán:

- Para que la luz se prenda, tienes que llegar hasta arriba del todo.
- Una vez que se prende, aunque bajes un escalón, la luz sigue prendida. No se apaga por cualquier cosita.
- Solo se va a apagar cuando llegues hasta abajo del todo, al suelo.

### Histéresis 

Es como decir que algo tiene "memoria" o que su estado actual depende de lo que pasó justo antes.

Normalmente, si pulsas un botón al 50%, esperarías que pasara algo. Pero en un sistema con histéresis, el resultado depende de si venías del 0% o del 100%.

- **En la subida:** Necesitas un empujón fuerte para activar algo (un umbral alto).
- **En la bajada:** Una vez activado, no se apaga inmediatamente; necesitas bajar mucho más para que se desactive (un umbral bajo).

Esa "distancia" o diferencia entre los dos puntos es lo que llamamos histéresis.

Ejemplos en la vida real:

- El termostato de una casa: Si se programa a 20°C y no tuviera histéresis, la calefacción se prendería y apagaría cada segundo si la temperatura oscila entre 19.9 y 20.1. Con histéresis see prende a los 19°C y no se apaga hasta llegar a los 21°C. Así descansa el motor.
- Las luces automáticas de un auto: Se encienden cuando se entra a un túnel (está muy oscuro). No se apagan apenas ves un poquito de luz, sino cuando el sol brilla de verdad afuera. Así no parpadean con la sombra de un árbol.
- Un elástico: Cuando se estira un elástico y luego lo se suelta, a veces no vuelve exactamente a su forma original de inmediato. El material "recuerda" que fue estirado.

### List of 4000 series integrated circuits 

La familia 4000 es una serie estándar de circuitos integrados (CI) de lógica CMOS introducida originalmente por RCA en 1968. Estos componentes son conocidos por su amplio rango de voltaje de operación (típicamente de 3V a 18V) y su bajísimo consumo de energía en estado estático, lo que los hace ideales para aplicaciones alimentadas por baterías. 

En la página estan ordenados por tipos y se pueden encontrar la mayoría de los circuitos integrados (chips) que hemos visto hasta la fecha. 

<https://en.wikipedia.org/wiki/List_of_4000-series_integrated_circuits>

## Sobre proyecto 01

Puntos a evaluar (cada ámbito vale 1.0 puntos + el punto base da el 7.0)
los primeros 3 son grupales, los siguientes 3 son individuales:

1. factura del sintetizador: orden del circuito, limpieza, organización, factura.
2. documentación textual del sintetizador: diagrama de bloques, esquemático, dibujos, textos, explicación de cada parte, de cada chip.
3. modificaciones del sintetizador: mejoras, decisiones de diseño, afinaciones, parámetros, experiencia de usuario.
4. bitácoras marzo.
5. bitácoras abril.
6. presentación oral.

Considerar:

- caja de cartón para la carcasa.
- Uso de chip 4017, 4093, 555, LM386 (mezcla/unión de todo lo que hemos visto hasta le fecha) + salida a audio. 
- Jorge Gómez Mir va venir a ver la entrega del proyecto 01 !! (invitado).

seguir como base (sí o sí) el siguiente esquemático/circuito: (En base a esta base, cada grupo debe hacer las modificaciones para generar sonidos únicos de cada uno.

- Paso 1: Clock.
- Paso 2: Secuenciador. 
- Paso 3: Sintetizador. 
- Paso 4: Salida (audio).

![circuito](./imagenes/circuito.png)

## Qué hice hoy !!

Trabajo grupal

- Armamos todo y lo unimos.

Tuvimos un problema de conexión entre el paso 2 (secuenciador) y el paso 3 (sintetizador), así que lo que hicimos fue seguir un código de color para cada “step” (step 1 azul, step 2 verde, step 3 amarillo, step 4 rojo) y ordenamos mejor las conexiones para que estuvieran más distribuidas. Por ejemplo, movimos algunas resistencias para hacer más espacio en el paso 2. En base a esto, aprovechamos de revisar todas las conexiones para verificar que estuvieran bien puestas y conectadas.

Después de confirmar que todo estuviera correcto, nos dimos cuenta de otros problemas que surgieron. Por ejemplo, cuando ponemos el potenciómetro del paso 4 al máximo no suena; de hecho, solo suena en un punto exacto (más o menos al medio), por lo que no hay que mover mucho el potenciómetro. Nos pasaba lo mismo al manipular los potenciómetros del paso 3. Para esto, revisamos distintas opciones para ver si tal vez había algo mal conectado o algún componente en mal estado, pero todo se veía bien, así que no entendíamos qué era lo que estaba fallando.

También intentamos conectar el paso 1 directo al paso 4 (salida), saltándonos el paso 3 (sintetizador). En ese caso sí sonó, pero finalmente no nos servía mucho para la entrega final.

![desarrollo](./imagenes/desarrollo.png)

