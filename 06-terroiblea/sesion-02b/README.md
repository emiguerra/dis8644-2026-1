# sesion-02b

Viernes 20 de Marzo, 2026.

Nota del día: sinceramente no sé qué tiene esta clase contra mí, pero editando el GitHub se me borró todo más de tres veces (╥_╥). Ni siquiera alcanzaba a guardar y pasaban cosas que hacían que perdiera todo lo que llevaba. Después de tantas veces que se borró, quiero aclarar que esta clase ya no tiene tanta información como la que tenía anotada la primera vez. :(

## Referentes (y otras cosas)

- **Cocoquantus** (instrumento musical) es un sintetizador y procesador de efectos artesanal diseñado por Peter Blasser para la marca Ciat-Lonbarde. Es conocido por su estética de madera, su flujo de trabajo esotérico y su sonido lofi y experimental.
- **Peter Blasser**
- **Ángel Abusleme** es _"ingeniero civil electricista y magíster en ciencias de la ingeniería por la Pontificia Universidad Católica de Chile. Además, es MSc y PhD en ingeniería eléctrica por la Universidad de Stanford, donde se especializó en diseño de circuitos integrados de señales mixtas. Actualmente, se desempeña como director y académico del Departamento de Ingeniería Eléctrica de la Pontificia Universidad Católica de Chile. Sus líneas de investigación son el desarrollo de instrumentos para experimentos de física de partículas y el diseño de circuitos integrados analógicos y de señales mixtas"_. - Profesor Asociado especializado en Diseño electrónico, microelectrónica, microcontroladores, sistemas embebidos.
- **Bob widlar** fue un ingeniero electrónico estadounidense pionero en el diseño de circuitos integrados (CI) lineales. Es ampliamente reconocido como el "padre" de los amplificadores operacionales modernos y una de las figuras más brillantes y excéntricas de la historia de Silicon Valley. 

## Qué aprendí hoy

### Ley de Ohm

(para más información revisar clase/sesión anterior)

- V (voltaje): se mide en volts (V).
- I (corriente): se mide en amperes (A).
- R (resistencia): se mide en ohmios (Ω).

Voltaje (V): La fuerza que impulsa a los electrones.

- V = I x R 

Un ejemplo seria: 9 V = I x 220 Ω

- Para aislar I, dividimos 9/220
- El resultado sería I = 0.04090909

Para expresar este valor en miliamperios, se multiplica el resultado por 1000

- 0.0409090 x 1000 = 40.91 mA
- O simplificado sería 0.04 A x 1000 mA = 40 mA.

### Circuitos

- circuito en **Serie**: los componentes se conectan uno tras otro (ejemplo: B–C en serie).  
- circuito en **Paralelo**: los componentes comparten los mismos nodos de conexión (ejemplo: BC // DE).  
- **Caja negra**: se analizan entradas y salidas sin importar el funcionamiento interno.
- **Grafos**: representación visual de conexiones entre puntos. (o) 
- **Grafos topológicos**: representación visual de un sistema que utiliza nodos y aristas para mostrar relaciones y componentes.

Según gemini, Los grafos en circuitos eléctricos son representaciones topológicas que simplifican redes complejas mediante nodos (vértices) y ramas (aristas), ignorando la naturaleza de los componentes para enfocarse en su conexión. Esta herramienta facilita la aplicación de las leyes de Kirchhoff para analizar corrientes y voltajes.

- En el caso de las clases se usa un esquema con conexiones cuadradas que terminan en tierra y empiezan por la alimentacion.
- Se podrían también hacer conexiones circulares y seguiría cumpliendo su propósito de simplificación y haciendo más fácil el entendimiento del camino de los circuitos.

### Componentes (parte 02)

- Cable dupont.
- Protoboard.
- Pila.
- Resistencias.
- Led (Diodo Emisor de Luz)
- Pulsador.
- Potenciometro. (hasta este punto revisar [sesion-01b](https://github.com/terroiblea/dis8644-2026-1/tree/main/06-terroiblea/sesion-01b) para más información)
- **Capacitor/condensador** es un componente electrónico pasivo que almacena energía eléctrica en un campo electrostático. Consiste en dos placas conductoras separadas por un material aislante (dieléctrico). A diferencia de las baterías, cargan y descargan energía rápidamente, siendo esenciales para filtrar, bloquear corriente continua y acoplar señales en circuitos.
  - **Electrolíticos:** polarizados (patita corta - negativo - GND), medidos en µF, con límite de voltaje. Es un dispositivo pasivo (no genera energía por sí mismo) que almacena energía en un campo eléctrico. Consiste en dos placas conductoras separadas por un material dieléctrico. Este diseño permite acumular carga eléctrica en las placas, creando así una diferencia de potencial. Hay de 1, 10, 100 μF
  - **Cerámicos:** no polarizados (no importa hacía que lado se pone), pequeños y versátiles. Son de valor fijo hechos de material cerámico como dieléctrico. Está formado por dos o más capas de cerámica y una capa de metal que actúan como electrodos. El comportamiento eléctrico y, por lo tanto, las aplicaciones de los materiales cerámicos están determinados por la composición del material cerámico. Los cerámicos son compuestos inorgánicos, no metálicos, de óxido cristalino, nitruro o carburo, como el carbono y el silicio. Tenemos de 104, osea 100.000 pF 
- **Chip / Circuito integrado 555**: 8 patas, numeradas en sentido antihorario desde la muesca. Es un temporizador versátil utilizado para generar pulsos, oscilaciones y retardos de tiempo. Sus modos principales son astable (oscilador libre) y monoestable (temporizador de un solo pulso).   
- **Fotoresistor**, también conocido como LDR (Light Dependent Resistor), es un componente electrónico pasivo cuya resistencia óhmica varía inversamente a la cantidad de luz recibida. Su resistencia disminuye cuando aumenta la intensidad de la luz (baja a cientos de ohmios) y aumenta en la oscuridad (sube a megaohmios). En otras palabras: su resistencia depende de la luz; más luz es igual a menor resistencia lo que genera que parpadeé más rápido.

![componentes02](./imagenes/componentes02.png)

## Qué hice hoy

Vimos el uso del chip 555.

En primera instancia, se conecta siguiendo el esquema "normal" (sale en la foto anterior). La salida la conectamos a un LED; el chip ocasiona que este "parpadee". Este parpadeo depende de las resistencias y capacitadores que tiene el circuito. Para ver distintas variaciones, comenzamos a realizar cambios para ver qué resultaba.

Probar distintos capacitores:

- 1 µF = parpadeo muy rápido. (Va tan rápido que da la sensación de que la luz vibra; solo grabando desde el celular se logra realmente apreciar cuando la luz se apaga y se vuelve a prender).
- 10 µF = parpadeo rápido, pero visible.
- 100 µF = parpadeo lento.
  
1. Sustituir una resistencia por un potenciómetro para variar/controlar la velocidad del parpadeo.

En uno de los extremos (hacia la izquierda), la luz se queda apagada; a medida que se va moviendo hacia la derecha, comienza a aumentar el nivel de parpadeo de la luz hasta llegar al otro extremo, que ocasiona que la luz se mantenga encendida en todo momento.

2. Usar un fotoresistor para que la luz controle la frecuencia del parpadeo.

El sensor funciona con luz, así que, en primera instancia, con la luz ambiental parpadeaba ligeramente rápido. Después, con mi grupo utilizamos la linterna del celular y las distintas potencias que esta tiene; en la más baja, el parpadeo era más lento y, con la potencia más grande, el parpadeo era muy rápido. 

![cambios](./imagenes/cambiosc.png)

(queda pendiente subir los gifts de los cambios realizados) 

## Encargo-02b

Practicar cualquiera de las materias que se hayan visto en clase, dejar ese registro en la bitácora. Ademas, escribir en la bitácora al menos 10 preguntas para la próxima sesión, sobre cualquier tema que hayamos revisado o mencionado. pueden ser preguntas técnicas, conceptuales, de diseño, etc.

### Practica 

(más bien fue un repaso para entender bien algunos contenidos)

Primero me enfoque en los tipos de circuitos pasados en clase (básico, en serie y en paralelo) porque no creo haberlo entendido tan bien, con el objetivo de entender cómo funcionan, en qué se diferencian y qué efectos generan en el comportamiento de la corriente.

En primera instancia, revisé el **circuito básico**, que es la forma más simple de un circuito. Este está compuesto por una fuente (pila), conductores (cables), la resistencia y un receptor (LED). Para que funcione, debe ser un sistema cerrado; es decir, la corriente debe poder salir de la fuente y volver a ella. Si el circuito se abre en cualquier punto, deja de funcionar completamente.

En el **circuito en serie**: En este tipo de circuito, los componentes están conectados uno tras otro en una sola línea, por lo que la corriente tiene un único camino para circular. Según lo que busque la corriente que pasa por cada componente es la misma, pero el voltaje se reparte entre ellos lo que ocasiona que, si se agregan más componentes (por ejemplo, más LEDs), cada uno reciba menos energía, por lo que su intensidad disminuye. Además, si uno de los componentes falla o se desconecta, todo el circuito deja de funcionar.

En el **circuito en paralelo:** Los componentes se conectan en distintas ramas, compartiendo los mismos puntos de entrada y salida. Según lo que busque la corriente se divide entre las ramas, pero cada componente recibe el voltaje completo de la fuente. Esto ocasiona que los dispositivos funcionen de manera independiente: si uno falla, los demás siguen funcionando. A diferencia del circuito en serie, aquí la intensidad de cada componente se mantiene más constante.

Entonces: 

- La principal diferencia está en cómo se distribuyen la corriente y el voltaje.
- El circuito en serie es más simple, pero menos eficiente y más vulnerable a fallas.
- El circuito en paralelo es más estable y confiable, por eso se utiliza en instalaciones reales (como en casas).
- El comportamiento del circuito (intensidad de luz, funcionamiento, fallas) depende directamente de cómo están conectados sus componentes.

| Tipo de circuito         | Cómo es                                | Qué pasa con la corriente         | Qué pasa con el voltaje             | ¿Qué pasa si un elemento falla? | Ejemplo simple                    |
| ------------------------ | -------------------------------------- | --------------------------------- | ----------------------------------- | ------------------------------- | --------------------------------- |
| **Circuito en serie**    | Todo en una sola línea (uno tras otro) | La misma corriente pasa por todos | El voltaje se reparte               |  Se apaga todo                | Luces de navidad antiguas         |
| **Circuito en paralelo** | Varias ramas (caminos separados)       | La corriente se divide            | El voltaje es el mismo en cada rama | Los demás siguen funcionando | Instalación eléctrica de una casa |

Después, pase a revisar nuevamente la ley de OHM. Le pedí a ChatGPT que me lo explicara como si fuera un niño de diez años y me sorprendió porque me dio un ejemplo muy parecido al que dio Misaa en la clase (el de regar la flor), pero debo admitir que esta vez sí logré entender mejor todo. 

Entonces: Imagina que la electricidad es como agua que viaja por una manguera. 

- El **voltaje (V)** es como la fuerza con la que empujas el agua.
- La **corriente/Intensidad (I)** es cuánta agua está pasando.
- La **resistencia (R)** es qué tan apretada o estrecha está la manguera.

La **Ley de Ohm** dice algo muy simple:

- Si empujas más fuerte (más voltaje), pasa más agua (más corriente).
- Si la manguera es muy estrecha (más resistencia), pasa menos agua.
- Si la manguera es ancha (menos resistencia), pasa más agua fácilmente.

Ejemplo fácil:

- Una pajita delgada: cuesta que pase el jugo (alta resistencia).
- Un tubo grande: pasa mucho jugo rápido (baja resistencia).

Entonces, la idea es:

La electricidad depende de cuánto empujas y qué tan difícil es pasar.

Ahora, Para saber el “empuje” (**Voltaje**, V): 

- se usa la formula: **V = I × R**
- ¿Cuándo sirve?: Cuando se sabe cuánta electricidad está pasando (corriente) y qué tan difícil es el camino (resistencia). 
- Ejemplo: Si pasa mucha electricidad por algo difícil = necesitas mucho “empuje”.
- “¿Qué tan fuerte tengo que empujar el agua?”
- ¿Para qué sirve?: Para saber si un aparato tiene suficiente “fuerza” para funcionar.
- Ej: pilas, enchufes, cargadores
- Se mide en - Unidad: **Voltios (V)**

Para saber cuánta electricidad pasa (Corriente/**Intensidad**, I):

- se usa la formula: **I = V / R**
- ¿Cuándo sirve?: Cuando se sabe cuánto empujas (voltaje) y qué tan apretado está el camino (resistencia).
- Ejemplo: Si empujas mucho pero la manguera es muy apretada = pasa poco.
- “¿Cuánta agua logra pasar?”
- ¿Para qué sirve?: Para saber cuánta energía está circulando, muy importante porque demasiada corriente puede quemar cosas
- Se mide en - Unidad: **Amperios (A)**

Para saber qué tan difícil es el camino (**Resistencia**, R)

- se usa la formula: **R = V / I**
- ¿Cuándo sirve?: Cuando se sabe cuánto empujas y cuánta electricidad realmente pasa.
- Ejemplo: Si empujas fuerte pero pasa poca agua = algo está muy apretado.
- “¿Qué tan tapada está la manguera?”
- ¿Para qué sirve?: Para controlar la electricidad, evitar que pase demasiada corriente y proteger circuitos.
- Se mide en - Unidad: **Ohmios (Ω)**

En resumen (simplificado):

| Magnitud        | Unidad       | Qué representa        | Ejemplo simple         |
| --------------- | ------------ | --------------------- | ---------------------- |
| Voltaje (V)     | Voltios (V)  | Empuje                | Qué tan fuerte empujas |
| Corriente (I)   | Amperios (A) | Cuánto fluye          | Cuánta agua pasa       |
| Resistencia (R) | Ohmios (Ω)   | Dificultad para pasar | Qué tan apretado está  |

### Preguntas

- ¿Cómo elegir correctamente el valor de una resistencia? Hasta el momento solo nos dicen exactamente qué usar, pero quisiera saber cómo uno ve que necesita si quiere hacer un circuito. 
- ¿Por qué algunos componentes funcionan con corriente continua (CC) y otros con corriente alterna (CA)?
- ¿Qué errores comunes pueden dañar una PCB al momento de diseñarla o fabricarla? (en qué hay que tener mayor precaución)
- ¿Cuál es la principal diferencia en rendimiento entre THT y SMT más allá del tamaño?
- ¿Cómo funciona internamente un LED para emitir luz y por qué hace poco comenzaron a hacerlos de color azul? ¿Por qué estos ocupan más voltajes (los azules) y que hace que cada color de led funcione con distintos voltajes?
- ¿Qué tan preciso es el código de colores de las resistencias comparado con medirlas con un multímetro?
- ¿Cómo influye el diseño de una PCB en el funcionamiento general del circuito? (ej: disposición de pistas)
- ¿Cómo se calcula el tiempo exacto de parpadeo con el chip 555?
- ¿Cómo hacer que el circuito tenga distintos ritmos y no solo uno?
- algo más general que no tiene que ver directamente con el contenido de la clase de forma bruta: ¿qué se considera "música"? o ¿qué hace que algo sea llamado música y no solo sonidos aleatorios o sonidos en general? (¿será la intención que se le da?). 

Si bien la actividad es dejar las preguntas para la próxima clase, aquí está la respuesta de algunas de las preguntas: 

- **¿Por qué algunos componentes funcionan con corriente continua (CC) y otros con corriente alterna (CA)?**

Para empezar aquí hay una tabla resumen entre corriente continua y corriente alterna: 

| Tipo de corriente           | Cómo se mueve la electricidad | Dirección                     | Forma              | Fuente común     | Ejemplo simple    |
| --------------------------- | ----------------------------- | ----------------------------- | ------------------ | ---------------- | ----------------- |
| **Corriente Continua (CC)** | Fluye de manera constante     | Siempre en un solo sentido | Línea recta        | Pilas, baterías  | Linterna, celular |
| **Corriente Alterna (CA)**  | Va cambiando constantemente   | Cambia de sentido        | Onda (sube y baja) | Enchufes de casa | Refrigerador, TV  |

- Corriente continua (CC)

Se usa porque es estable y no cambia.

Entonces: Los componentes como chips, microcontroladores, celulares necesitan CC porque trabajan con señales precisas y constantes. “Necesitan que la electricidad sea tranquila y ordenada”

- Corriente alterna (CA)

Se usa porque es más eficiente para transportar energía.

Entonces: Se usa en casas, motores, electrodomésticos porque puede viajar largas distancias sin perder tanta energía. “Es mejor para llevar electricidad lejos y mover cosas”

CC = precisión (electrónica).

CA = potencia y transporte (energía).

- **¿Cuál es la principal diferencia en rendimiento entre THT y SMT más allá del tamaño?**

Para empezar aquí hay una tabla resumen entre THT y SMT: 

| Tipo    | Nombre completo          | Cómo se montan                  | Tamaño       | Facilidad           | Uso común             |
| ------- | ------------------------ | ------------------------------- | ------------ | ------------------- | --------------------- |
| **THT** | Through-Hole Technology  | Las patas atraviesan la placa   | Grandes      | Más fácil de soldar | Proyectos, prototipos |
| **SMT** | Surface-Mount Technology | Van pegados sobre la superficie | Muy pequeños | Más difícil         | Electrónica moderna   |

THT (Through-Hole)

Rendimiento:

- Más resistente mecánicamente (no se sueltan fácil).
- Mejor para altas corrientes o potencia.
- Peor en altas frecuencias (más interferencias).

Es ideal para: Fuentes de poder, equipos industriales, prototipos. 

SMT (Surface-Mount)

Rendimiento:

- Mejor en alta velocidad y alta frecuencia.
- Menos ruido eléctrico (mejor señal).
- Puede disipar calor distinto (depende del diseño).
- Permite muchos más componentes en poco espacio. 

Es ideal para: Computadores, celulares, electrónica moderna. 

THT = resistente y potencia.

SMT = velocidad y eficiencia electrónica.

- **¿Cómo funciona internamente un LED para emitir luz y por qué hace poco comenzaron a hacerlos de color azul? ¿Por qué estos ocupan más voltajes (los azules) y que hace que cada color de led funcione con distintos voltajes?**
  
Un LED (diodo emisor de luz) es un semiconductor con una unión p-n.

Cuando se le aplicas corriente continua (CC):

- Los electrones (carga negativa) se mueven hacia la unión.
- Se encuentran con “huecos” (cargas positivas).
- Al juntarse, pierden energía.
- Esa energía se libera como luz (fotones).

Es decir, “Cuando las cargas se juntan, sueltan energía en forma de luz”.

¿Por qué los LED pueden tener un color distinto?

- El color depende de un concepto clave: la banda prohibida (o band gap) que es la energía que necesita el electrón para poder moverse y luego liberar luz.

Ejemplo: 

- Banda pequeña = menos energía = luz roja.
- Banda grande = más energía = luz azul.

El color depende del material del LED

- Rojo = Arseniuro de galio (GaAs) y/o Arseniuro-fosfuro de galio (GaAsP) =  menos energía (bajo voltaje (~1.8 – 2.0 V))
- Verde o amarillo = Fosfuro de galio (GaP) y/o variantes como GaAsP = energía media (voltaje medio (~2.0 – 2.5 V))
- Azul = Nitruro de galio (GaN) y/o Nitruro de galio-indio (InGaN) = mucha energía (mayor voltaje (~3.0 – 3.5 V))

¿Por qué los LED azules aparecieron mucho después?

Porque son mucho más difíciles de fabricar ya que para lograr luz azul se necesitas materiales con alta energía y estructuras cristalinas muy precisas. Durante años, los científicos no lograban hacerlo bien hasta que en los 90 se desarrolló el material adecuado (como el nitruro de galio). (Este avance fue tan importante que llevó al Premio Nobel de Física 2014).

> El Premio Nobel de Física 2014 fue otorgado a Isamu Akasaki, Hiroshi Amano y Shuji Nakamura por la invención de los diodos emisores de luz (LED) azules eficientes. Este avance permitió la creación de fuentes de luz blanca brillantes y de bajo consumo, revolucionando la iluminación moderna.

Entonces, ¿Por qué los LED azules usan más voltaje?

- Porque necesitan más energía para encenderse. (más voltaje necesario)

| Color       | Material principal | Voltaje típico (V) | Costo típico |
| ----------- | ------------------ | ------------------ | ------------ |
| 🔴 Rojo     | GaAs / GaAsP       | **1.8 – 2.0 V**    | Muy barato   |
| 🟡 Amarillo | GaP / GaAsP        | **2.0 – 2.2 V**    | Muy barato   |
| 🟢 Verde    | GaP / GaAsP        | **2.2 – 3.0 V**    | Muy barato   |
| 🔵 Azul     | GaN / InGaN        | **3.0 – 3.5 V**    | Barato  (pero más complejo) |
| ⚪ Blanco    | GaN + fósforo      | **3.0 – 3.5 V**    | Barato       |

El material del semiconductor define: El color, el voltaje necesario y el costo. Por eso los LEDs simples de electrónica básica usan materiales más antiguos y baratos (rojo, verde) y los modernos (azul/blanco) usan materiales más avanzados. 

### Bibliografía 

- Ammitech. (s.f.). Diferencias entre montaje SMT vs montaje THT. <https://ammitechnologies.com/diferencias-montaje-smt-tht/>
- Cursos MCI Electronics. (2022). Diferencia entre circuito serie y paralelo. <https://cursos.mcielectronics.cl/2022/08/09/diferencia-entre-circuito-serie-y-paralelo/>
- DigiKey. (s.f.). Cómo aplicar la ley de Ohm a circuitos en serie y en paralelo. <https://www.digikey.es/es/blog/how-to-apply-ohms-law-to-series-and-parallel-circuits>
- Fluke Corporation. (s.f.). La Ley de Ohm: Qué es y cómo calcularla. <https://www.fluke.com/es-mx/informacion/blog/electrica/que-es-la-ley-de-ohm>
- Universidad de Granada. (s.f.). Los diodos LED. <https://www.ugr.es/~juanki/LED.htm>
- Wikipedia. (s.f.). LED. <https://es.wikipedia.org/wiki/Led>
- Wikipedia. (s.f.). Ley de Ohm. <https://es.wikipedia.org/wiki/Ley_de_Ohm>
