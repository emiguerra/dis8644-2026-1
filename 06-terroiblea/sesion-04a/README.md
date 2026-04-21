# sesion-04a

Martes 31 de Marzo, 2026. 

Nota del día: Único día de taller de la semana porque el viernes es feriado. 

## Referentes (y otras cosas)

- **Anouar Brahem** Es un virtuoso intérprete del oud (laúd árabe) y compositor tunecino. Es ampliamente reconocido por fusionar la música clásica árabe con el jazz contemporáneo y la música de cámara occidental, creando un sonido introspectivo y poético que ha llevado al laúd de vuelta a su estatus como instrumento solista. 
- **Barzakh** álbum debut de Anouar Brahem, lanzado en 1991. El título hace referencia a un concepto filosófico y espiritual en el Islam que describe un "limbo" o lugar intermedio entre dos mundos. Musicalmente, el álbum es una colección de 13 melodías que fusionan la tradición clásica árabe con una estética de producción contemporánea y aireada propia de ECM. A diferencia de trabajos posteriores más cercanos al jazz, este disco se centra profundamente en el sonido del oud solista, evocando paisajes mediterráneos y desérticos. 
- **"the three fives kit"** es un proyecto de electrónica de Evil Mad Scientist Laboratories diseñado por Eric Schlaepfer. Es una réplica funcional a escala "gigante" del circuito integrado 555. En lugar de ser un pequeño chip de silicio, este kit utiliza componentes individuales (discretos) para que puedas ver y entender cómo funciona por dentro. 

## Qué aprendí hoy

### Escalas y unidades electrónicas

Prefijos de alta magnitud (usados en resistencias):

|10⁼| Valor numérico    | Prefijo/nombre | Símbolo | 
|-----| ----------------- | ------- | ------- |
|10¹| 1                 | unidad  | —       |
|10³| 1.000             | kilo    | k (minúscula) |
|10⁶| 1.000.000         | mega    | M (mayúsculas) |
|10⁹| 1.000.000.000     | giga    | G       | 
|10¹²| 1.000.000.000.000 | tera    | T       |

Prefijos de baja magnitud (usados en capacitores):

|10⁼| Valor decimal     | Prefijo/nombre | Símbolo |
|-----| ----------------- | ------- | ------- |
|10⁻¹²| 0,000000000001 | pico    | p       |
|10⁻⁹| 0,000000001     | nano    | n       |
|10⁻⁶| 0,000001         | micro   | µ (mu - se parece a la u) | 
|10⁻³| 0,001             | mili    | m (minúscula) |

Entonces: 

- **resistencias: "R"**

Mega - kilo - Unidad 

- **condensador: "C"**

mili - micro - mano - pico

F = faraday "el uf de los condensadores"
ej: 10.000 picoF = 100 nanoF = 0,1 mF

### Falstad

Página web que sirve para ver como funcionan los circuitos, se puede dibujar/esquematizar y se renderiza mostrando el flujo de energía dentro del circuito
(recordar que para cambiar de modo de funcionamiento hay que apretar escape en el teclado).

Para compartir: archivo - exportar - formato texto (descargar) y después la otra persona lo importa a Falstad. 

![falstad](./imagenes/falstad.gif)

Según gemini (en otras palabras a lo que puse anteriormente) Falstad es un simulador de circuitos electrónicos interactivo y gratuito que funciona directamente en el navegador. Tiene la capacidad para visualizar el flujo de la corriente en tiempo real. 

muestra: 

- Corriente en movimiento: Muestra puntos amarillos que se mueven por los cables para representar la velocidad y dirección de la corriente.
- Colores de voltaje: Los cables cambian de color (verde para positivo, rojo para negativo) según el voltaje.
- Osciloscopio integrado: Puedes ver formas de onda (como la salida de un chip 555) simplemente pasando el ratón sobre un componente.

## Qué hice hoy

Astable -> monostable -> ver como conectarlos entre ellos !
Para "controlar cuanto tiempo esta prendido"

problemas (que vimos como grupo): las baterías funcionan distintas, si se conectan dos circuitos pero no se conectan las baterías no se pueden sincronizar. Hay que conectar los GND o usar solo una batería y conectar entre las photoboard la energía y la GND (de esa forma si se conecta la información y se hace un solo circuito). 

![01](./imagenes/01.png)
![02](./imagenes/02.png)
![03](./imagenes/03.png)

## Proyecto 01

Grupo de trabajo:

- Catalina Catalán. (yo)
- [Nicolás Miranda](https://github.com/disenoUDP/dis8644-2026-1/tree/main/19-Nicolas-Miranda1312)
- [Vania paredes](https://github.com/disenoUDP/dis8644-2026-1/tree/main/25-paredesvania)

Idea: (sin saber que vamos a hacer todavía/ cuál es el proyecto en sí - aspectos formales) Hacer algo parecido a los carrillones de viento (idea de proyecto con motor; motor gira en círculos y va tocando estos "tubos" colgados que generan sonidos). 

## Encargo-04a

Destripar un dispositivo electrónico, documentar con texto e imagen el proceso, distinguir los elementos de la PCB que hemos estudiado como R y C y chips. + documentar las conexiones entre la PCB y los componentes en la carcasa. + escribir un texto de 3 párrafos explicando de forma poética imaginaria el funcionamiento especulativo del dispositivo electrónica, usando metáforas y analogías para describir el flujo de electricidad y la interacción de los componentes. el texto debe ser creativo y evocador, transmitiendo la esencia del dispositivo sin ser técnico, ni tampoco necesariamente real.

### Aparato destripado  

![dvd2](./imagenes/dvd2.png)
![dvd1](./imagenes/dvd1.png)

### Documentación

Quiero partir aclarando que no tenía aparatos para destripar y tampoco me daba el tiempo para ir a la feria a cachurear o algo parecido, así que lo que hice fue utilizar y observar (sin sacar nada) un reproductor DVD que tengo. Ya había visto su interior antes, cuando intenté repararlo en el pasado, así que sentí que me servía para el encargo. Solo le saqué la tapa y observé todo lo que se ve sin tocar nada, ya que tengo la intención de seguir usando el reproductor.

Ahora, a diferencia de la primera vez que lo había abierto, sí pude identificar ciertos componentes (y eso me pone muy feliz, Estuve bastante raro contemplando todo lo que veía más que nada porque hay muchas cosas que siento que si puedo identificar !!). Siento que entiendo cosas que jamás pensé que iba a entender, es muy loco pero me gusta saber. Pude reconocer condensadores y resistencias; identifiqué condensadores de 100 µF y de 220 µF (son gigantes), aunque habían de muchos otros tamaños y valores. Las resistencias estaban más en la sección amarilla (hay un montón, yo diría que mínimo 30 distintas), que es la sección conectada con el cable que se enchufa a la corriente, así que supongo que es la parte que le da alimentación a todo el aparato. Por lo que entiendo en ámbitos generales, es la parte que transforma los voltajes para que todo pueda funcionar, así que tal vez por eso tiene tantas resistencias.

Hay muchos chips, pero a la mayoría no les pude leer el nombre. Eso sí, me sorprendió la cantidad de tamaños distintos que hay: hay unos con muchísimos pines (hay uno que tiene el tamaño del 555 pero tiene 20 patitas ). Los otros elementos supongo que deben ser algo así como el lector de discos y cosas así.

> Agradecimientos a mi inspectora felina (alias mi “choapina”), que ayudó en la verificación de calidad de los componentes y a que no hiciera nada para echar a perder el reproductor. 

### Funcionamiento imaginario

(No sé qué tan poético sea esto porque no me sale serlo, pero sí es una explicación de lo que me imagino que pasa)

Cuando enchufas el aparato, la energía entra de golpe por la zona amarilla. Ahí, unos tubitos altos reciben la corriente, la calman y la guardan un momento para repartirla con cuidado al resto de las piezas. Es como si el tablero despertara y la electricidad empezara a caminar por todos los caminos de cobre, buscando llegar a los bloques negros que controlan todo el movimiento.

En el centro, un disco empieza a girar muy rápido (el dvd) mientras un apartado de vidrio se mueve por debajo. Este apartado lanza una luz roja que rebota en el disco (un niño flotó sobre mí y voló un auto con su rasho laser) y va recogiendo pedacitos de información que contiene el disco externo que se conecta aidcionalmente a todo el circuito. Esos datos viajan por cables planos, como si fueran autopistas (se echan competencias), hacia los procesadores que transforman esos rebotes de luz en las imágenes y los sonidos que vemos en la tele. 

Por todo el camino hay piezas pequeñitas que ayudan a que la energía no corra tan rápido o se desvíe por donde no debe. Todo funciona como una gran cadena donde cada pieza espera su turno para activarse. Cuando apagas el reproductor, la corriente deja de fluir, los motores se detienen y todo el sistema se queda dormido en silencio hasta la próxima vez (eso es todo amigos). 
