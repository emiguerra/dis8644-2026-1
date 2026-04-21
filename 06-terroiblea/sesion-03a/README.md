# sesion-03a

Martes 24 de Marzo, 2026.

Nota del día: eee. 

## Referentes (y otras cosas)

- **Electricidad en chile**, _La situación actual del consumo de electricidad en Chile refleja una apuesta significativa por fuentes de energía baja en carbono, con más del 70% de la electricidad generada a partir de estas fuentes_. <https://lowcarbonpower.org/es/region/chile> 
- proyecto misaa: **strangeTrigger** - <https://github.com/misaaaaaa/strangeTrigger>
- **Tutupá** _"es una drum machine que controla baquetas físicas, creada con la intención de generar ritmos programados con los objetos del entorno. El primer prototipo fue desarrollado por Bárbara Molina y Matías Serrano a través del programa de becas de verano de StgoMakerSpace y estrenado el 5 de abril de 2016. Está programado en Arduino y consta de un controlador basado en una matriz de luces led y las baquetas son movidas por servomotores.Pensado con fines artísticos, musicales y educativos, busca promover nuevas relaciones con los objetos a través de la escucha y proponer problemáticas en torno al desarrollo de la tecnología y nuestra relación con ella."_ - <https://vimeo.com/164729084>
- **Gordon matta clark** fue un artista estadounidense de ascendencia chilena que exploró diferentes modos de intervención arquitectónica. Se le reconoce principalmente por sus «building cuts» o «cortes de edificios».
- **David Eugene Tudor** fue un pianista y compositor estadounidense de música experimental. Estudió piano con Stefan Wolpe y al tiempo ganó fama como uno de los principales intérpretes de la música de vanguardia para piano. En la década de 1950, Tudor era el intérprete favorito de compositores como John Cage, Karlheinz Stockhausen y Pierre Boulez. Se hizo famoso por resolver partituras gráficas y complejas: Tenía una capacidad intelectual única para interpretar notaciones que otros consideraban imposibles. Fue el principal intérprete de las obras de Cage que utilizaban objetos (tornillos, gomas) dentro del piano para alterar su sonido. Fue quien estrenó la famosa obra "silenciosa" de Cage en 1952, sentándose frente al piano sin tocar una sola tecla. A mediados de los años 60, Tudor abandonó casi por completo el piano para dedicarse a la electrónica en vivo. Su enfoque no era usar sintetizadores comerciales (como los de Moog o Buchla), sino construir sus propios circuitos.
- **John Cage** según gemini fue un influyente compositor, filósofo y artista estadounidense, reconocido como una de las figuras más importantes de la vanguardia del siglo XX. Su trabajo desafió las definiciones tradicionales de la música, integrando el silencio, el azar y el uso de instrumentos no convencionales. "el silencio no existe"
- **4′33″** obra de John Cage realizada por Davir Tudor, _el debut de la obra tuvo lugar el 29 de agosto de 1952 en el Maverick Concert Hall de Woodstock, Nueva York. Aunque la pieza se asocia con el "silencio", Tudor utilizó métodos precisos para ejecutarla: se sentó al piano con un cronómetro para medir exactamente los tres movimientos de la obra. Para indicar el inicio y el fin de cada sección sin tocar una sola nota, Tudor cerraba y abría la tapa del teclado del piano. En esa primera interpretación, los movimientos duraron 30 segundos, 2 minutos y 23 segundos, y 1 minuto y 40 segundos respectivamente. La intención de Cage, transmitida a través de la interpretación de Tudor, no era el silencio absoluto (que Cage consideraba inexistente), sino redirigir la atención del oyente hacia los sonidos ambientales. Durante el estreno, los asistentes pudieron escuchar el viento entre los árboles, la lluvia sobre el techo y los ruidos de incomodidad del propio público (tosidos y susurros) como parte de la música. Tudor, quien era un virtuoso del piano y colaborador cercano de Cage, ayudó a legitimar esta obra vanguardista que inicialmente provocó desconcierto e irritación en gran parte de la audiencia._
- **Merce Cunningham** fue un coreógrafo y bailarín estadounidense, considerado una de las figuras más revolucionarias e influyentes de la danza del siglo XX. Su trabajo marcó la transición definitiva de la danza moderna a la danza contemporánea, al romper con la narrativa emocional y la dependencia de la música. Propuso que la danza y la música debían coexistir de forma autónoma en el mismo tiempo y espacio, sin que una dictara el ritmo de la otra. Junto a su pareja y colaborador habitual, el compositor John Cage, utilizó métodos aleatorios (como el lanzamiento de monedas o dados) para determinar secuencias de movimiento, eliminando el control consciente del coreógrafo.
- **The Moog Ladder Filter** de Moog music <https://youtu.be/5sAq0FjRUI4>

Avisos de la clase: (eventos opcionales)

- De sokio **"Splitting / Absence"** en el gam a (opera/obra) _"As part of their HISTORIAS initiative, The Clemente Center and New Latin Wave present a special workshop preview of Splitting / Absence, Section: New York, part of Sokio’s new opera about Gordon Matta-Clark"._
- De club sonoro deportivo **“Nada como una metáfora”** (tomar deporte y convertirlo en sonido) _"La presentación propone un encuentro entre deporte y arte sonoro, y constituye uno de los resultados públicos del proyecto Aproximaciones subacuáticas, financiado por el Fondo Nacional de Desarrollo Cultural y las Artes. Este proyecto releva la investigación artística en diálogo con otros campos del conocimiento, a través de un trabajo colaborativo entre el Club Sonoro Deportivo, integrado por Fernanda Fábrega Rubio, Matías Serrano Acevedo y Santiago Corvalán Garretón, junto a la Vicerrectoría de Asuntos Estudiantiles y Comunitarios (VAEC), la Dirección de Deportes y Actividad Física (DDAF) y el Magíster en Artes Mediales de la Universidad de Chile"._ - <https://www.instagram.com/clubsonorodeportivo/> / <https://www.instagram.com/p/DWUFR7djvy4/>

## Qué aprendí hoy

### Chip NE555 timer (circuito integrado)

El NE555 es un circuito integrado usado en electrónica para generar señales eléctricas repetitivas. 

Inventor: Fue diseñado en 1971 por el ingeniero suizo Hans Camenzind; quien trabajaba como consultor para la empresa Signetics. Se dice que la idea fue inicialmente rechazada por el departamento de ingeniería de la empresa, pero él pasó un año perfeccionando el diseño a mano.

A pesar de su "sencillez" externa (y la verdad es que es bien tiernito), su interior es un sistema híbrido complejo que contiene: 23 transistores, 16 resistencias y 2 diodos. Tres resistencias iguales que establecen voltajes de referencia de 1/3 y 2/3 de Vcc. Dos comparadores que detectan cuándo el voltaje de entrada cruza esos niveles de referencia. Un flip-flop RS que es un interruptor digital interno que memoriza el estado de la salida y un transistor de descarga que esta encargado de vaciar capacitores externos para reiniciar ciclos de tiempo. 

¿Por qué sigue siendo importante?

A pesar de la existencia de microcontroladores modernos como Arduino, el 555 sigue siendo fundamental porque: Es extremadamente económico, no requiere programación, solo un par de resistencias y capacitores externos y es muy versatil al punto que puede generar tiempos desde microsegundos hasta horas con gran precisión. 

El **Circuito integrado 555** tiene 8 patas, numeradas en sentido antihorario desde la muesca. Es un **temporizador** utilizado para generar **pulsos, oscilaciones y retardos de tiempo.**

> Aunque se cree que el nombre "555" proviene de sus tres resistencias internas de 5 kΩ, el propio Camenzind mencionó en entrevistas que el número fue elegido por Signetics simplemente porque "sonaba bien".

![555](./imagenes/555.gif)

Modos de operación principales: 

#### Astables: 

Es un oscilador que conmuta continuamente entre dos estados inestables (alto y bajo), produciendo una onda cuadrada sin necesidad de señal externa. (A diferencia de los monoestables o biestables, el astable nunca descansa en un estado fijo.)

- Circuito que NO tiene estados estables ya que cambia continuamente entre alto y bajo (nunca se detiene).
- Pasa de alto (1 / encendido / 9V) a bajo (0 / apagado / 0V). (ej: 1 a 0 a 1 a 0 a 1 y así siempre que tenga energía)
- Genera una onda cuadrada constante o un pulso constante (representación).
- Oscila continuamente mientras reciba alimentación.
- Produce: parpadeo (LED) o sonido continuo (parlante, suena como un latido)
- Depende de las resistencias y condensadores (controlan la frecuencia, que tán rápido cambia entre un estado y el otro).
- Es ideal para luces intermitentes, relojes lógicos o alarmas.

#### Monostables: 

En el modo monoestable el 555 realiza una temporización cuando se presiona un pulsador. Al activarlo, la salida pasa a estado alto mientras se contabiliza el tiempo programado, tras lo cual la salida vuelve a estado bajo a la espera de una nueva activación del pulsador.

- Circuito con 1 estado estable y 1 estado temporal. 
- Necesita un gatillo (botón/señal). Al activarse cambia de estado y luego vuelve automáticamente a su estado 0.
- Genera un solo pulso.
- Está quieto hasta que algo lo activa, luego “dispara” y vuelve. 
- Ejemplo: temporizador, luz que se apaga sola, timbre. 
- Depende principalmente del condensador y resistencia (tiempo del pulso). 

![modosoperación](./imagenes/modos.png)

información sacada de: El circuito integrado 555 <https://electroclinica.org/2024/03/02/el-circuito-integrado-555/> 

Otras consideraciones: 

#### Oscilación

- ir y venir.
- subir y bajar.
- cambiar constantemente.

En electrónica: pasar de alto a bajo (1 <-> 0, encendido <-> apagado)

En el caso del **modo astable**: 

- salto de bajo a alto.
- salto de alto a bajo.

Un ciclo completo = una oscilación. 

- El circuito nunca se queda quieto.
- Cambia continuamente entre 9V y 0V.
- Esa variación genera la señal y reacción (Ejemplo: en el caso de un Led con 0V se apaga y en 9V se enciende, esto se va repetir continuamente mientras tenga energía). En otras palabras: Lo que se ve representando en el sonido o lo que se escucha es el cambio de 9V a 0v (el sonido ocurre en la transición, no en los extremos).

#### Frecuencia y Período

- **Período (T)**: tiempo de un ciclo completo.
- **Frecuencia (f)**: cantidad de ciclos por segundo.
- F = 1/T
- Se mide en Hertz (Hz)

La frecuencia depende de: **resistencias y condensadores** (esto es lo que determina qué tan rápido parpadea un LED, qué tan agudo o grave suena un parlante).

En el caso del condensador se carga (sube voltaje) y se descarga (baja voltaje), esto crea el ritmo del circuito. Cumple con “suavizar” la señal, eliminar lo constante y deja pasar el cambio. Por eso actúa como un filtro permitiendo que el sonido exista (cambio)

- **condensador grande** = más lento = sonido grave.
- **condensador pequeño** = más rápido = sonido agudo.

Ejemplo:

- cambiar de 10 µF a 1 µF = sonido más rápido/agudo. 

En el caso de las resistencias, estas controlan la velocidad de carga/descarga del condensador afectando directamente la frecuencia (utilizar siempre mayores a 1 kΩ). Por otra parte, por ejemplo el potenciómetro es una resistencia variable que permite ajustar la frecuencia manualmente (como cambiar la velocidad del parpadeo o el tono del sonido). 

#### Transducciónes 

Es la transformación de un tipo de señal, energía o material genético en otro de distinta naturaleza. En el caso de la electrónica y específicamente de lo que estamos desarrollando sería: el proceso de convertir energía eléctrica a sonido. 

- El parlante transforma la señal del 555 en sonido audible. 

#### Interruptores (Switch)

Es un componente pasivo que permite o interrumpe el paso de la corriente eléctrica en un circuito, o bien desvía la señal hacia diferentes caminos.

Su función es controlar el paso de corriente:

- encender / apagar
- abrir / cerrar circuito

Tipos:

- momentáneos (ej: timbre)
- estables (ej: interruptor de luz)

A diferencia de los interruptores de pared, los que utilizamos suelen ser mucho más pequeños y están diseñados para soldarse en placas de circuito impreso (PCB).

Clasificación por Configuración (Polos y Vías): (Se definen por cuántos circuitos controlan y cuántas posiciones de salida tienen).

- SPST (Single Pole Single Throw): El más simple (encendido/apagado). Solo dos terminales.
- SPDT (Single Pole Double Throw): Un común y dos salidas. Selecciona entre dos caminos (A o B).
- DPST / DPDT (Double Pole): Controlan dos circuitos aislados al mismo tiempo con un solo movimiento.

#### Conceptos clave resumidos: 

- **Oscilar:** cambiar constantemente entre dos estados.
- **Astable:** nunca se queda fijo.
- **Frecuencia:** qué tan rápido ocurre el cambio.
- **Condensador:** marca el ritmo (carga/descarga).
- **Resistencias:** regulan la velocidad.
- **Salida:** se ve (LED) o se escucha (parlante).

## Qué hice hoy

Hoy trabajamos con la salida del circuito astable del 555, que era originalmente un LED con un resistor, después reemplazamos el LED y resistor, por un capacitor y un parlante. Para hacer las conexiones usamos cables caimán/alligator clip (como no habían tantos caimanes en la clase lo realizamos grupal, al final la vania y el nico de mi grupo tuvieron la oportunidad de hacerlo sonar mientras yo los ayudaba). 

Después vimos los efectos de cambiar una resistencia y un capacitor en el circuito, y cómo afecta la frecuencia de oscilación del circuito.

(las fotos del proceso están junto a las fotos del circuito del encargo!!)

## Encargo-03a

Expandir el circuito usado, agregando más interruptores para crear el circuito toy organ disponible en <https://www.555-timer-circuits.com/toy-organ.html>. otra versión del circuito se incluye a continuación, diagramada por misaa hoy. documentar todos los aciertos y errores en la bitácora + ver documental variaciones espectrales sobre la vida de josé vicente asuar, disponible en <https://www.youtube.com/watch?v=sJ9EZWBZee8> 

### Circuito toy organ 

![encargo01_diagrama](./imagenes/encargo01.png)

![encargo](./imagenes/encargo.png)

A mi todavía me cuesta un poco seguir los esquemas, más bien es mi grupo de trabajo el que siempre me enseña o ayuda a realizar estas partes del trabajo. En este caso, la vania y el nico me ayudaron a seguir el esquema y me prestaron también sus botones para poder tener una mayor cantidad. Más que nada me siguen confundiendo ciertas conexiones (cuando van cosas juntas en más de un pin por ejemplo, cuando se conectan los circulitos y cosas así). 

### Variaciones espectrales 

Documental inspirado en la vida y obra del músico e ingeniero chileno José Vicente Asuar, destacado a nivel mundial por su trabajo en el desarrollo de la música electroacústica y creador del COMDASUAR, el primer computador musical en Latino américa, hoy abandonado en una parcela. El reencuentro de Asuar con este artefacto descubre un relato perdido, revelando la historia de un personaje esencial en la biografía sonora chilena. 

![josevicenteasuar](./imagenes/jose.png)

#### José Vicente Asuar

José Vicente Jesús Asuar Puiggrós (Santiago de Chile, 20 de julio de 1933-11 de enero de 2017) fue un compositor, ingeniero e investigador chileno, uno de los pioneros de la música electroacústica a nivel nacional; además es considerado ser uno de los primeros compositores de música electrónica a nivel latinoamericano y ser el creador del primer laboratorio de música electrónica en América Latina.

Algunos hitos importantes de su vida/carrera:

- En 1958 crea uno de los primeros laboratorios de música electrónica en Latinoamérica.
- Compone Variaciones espectrales (1959), considerada la primera obra electrónica chilena.
- Trabaja y desarrolla investigación en Chile, Alemania y Venezuela.
- Influye en generaciones de músicos experimentales.

Su enfoque era adelantado a su tiempo ya que no veía la tecnología como una herramienta secundaria, sino como parte del proceso creativo mismo. 

#### COMDASUAR

El COMDASUAR (Computador Musical Digital-Analógico Asuar) fue  creado en 1978, es el primer computador musical de Latinoamérica diseñado específicamente para componer e interpretar música. 

Algunos datos relevantes: 

- Usaba un teclado tipo QWERTY.
- Funcionaba con un lenguaje de programación musical.
- Permitía generar sonidos electrónicos directamente.

Algo interesante es que no era solo una máquina sino que era una extensión del compositor. De hecho, estudios lo describen como un ejemplo de “cognición extendida”, donde el artista y la tecnología funcionan como un solo sistema creativo

#### Reflexión

El documental me deja dando vuelta una frase que vi anteriormente: “El progreso no siempre se pierde por falta de talento, sino por falta de memoria”. Y eso me hizo mucho sentido con un CFG que tuve el semestre pasado, donde veíamos cómo la memoria y el archivo son clave para conservar el pasado. Porque al final, lo que pasa con José Vicente Asuar es exactamente eso, no es que faltara talento (todo lo contrario), sino que faltó registro, difusión y valoración (sobre todo esta última parte). Chile tuvo a un pionero mundial en música computacional y, aun así, quedó medio perdido en la historia (y siendo honestos, todavía lo está, porque lamentablemente no es una figura tan conocida). Creo que bajo este contexto el COMDASUAR abandonado termina siendo casi una metáfora, ya que no solo es una máquina olvidada, es el reflejo de cómo se puede dejar botado todo un legado si no hay una cultura de memoria que lo sostenga (y lo valore/respete!). Esto se refuerza aún más con el contraste que muestra el documental, mientras en el extranjero a Jose se le reconoce como innovador y participó en espacios importantes, en Chile su obra está poco difundida y su figura queda relegada a nichos (e incluso buscando información sobre él no hay tanta como debería ser).

PPor otro lado, considero que en el documental se deja claro una lectura más profunda y súper actual ya que Asuar no veía la tecnología como un reemplazo del artista, sino como una herramienta para potenciar la creatividad. Eso conecta mucho con las discusiones actuales sobre inteligencia artificial, donde muchas veces se plantea como una amenaza, cuando en realidad podría entenderse como un apoyo. Personalmente, siento que la IA no debería reemplazar al artista o al diseñador (que es algo que se ve mucho), sino facilitar ciertos procesos y abrir nuevas posibilidades creativas, tal como lo hacía Asuar con sus propias herramientas.

### Bibliografía

- Archive of Digital Art. (s.f.). JOSE VICENTE ASUAR (Chile, 1933-2017). <http://archive.olats.org/pionniers/pp/asuar/asuar.php>
- Discoteca Nacional de Chile. (2019, noviembre). José Vicente Asuar: Así habló el computador. CMDA-1. 1979. Chile. <https://discotecanacionalchile.blogspot.com/2019/11/jose-vicente-asuar-asi-hablo-el.html>
- The Clinic. (2010, octubre 24). José Vicente Asuar (1933): compositor pionero de la música electrónica “El piano o el violín son tan artificiales como un computador”. <https://www.theclinic.cl/2010/10/24/jose-vicente-asuar-1933-compositor-pionero-de-la-musica-electronica-%E2%80%9Cel-piano-o-el-violin-son-tan-artificiales-como-un-computador%E2%80%9D/>
- Wikipedia. (s.f.). José Vicente Asuar. <https://es.wikipedia.org/wiki/Jos%C3%A9_Vicente_Asuar>
