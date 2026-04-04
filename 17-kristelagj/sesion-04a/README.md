# sesion-04a
## Clase310326

### pre-clase (teloneo Aaron)

Comenzamos la clase hablando sobre lo que sucedió y opinamos sobre sokio y el trabajo de misaa, además se leyeron todos los feedbacks sobre cómo nos sentíamos e íbamos durante marzo (hoy termino marzo)

Se nos mencionó que tenemos 1 semana para poder rellenar después de dados los encargos

### clase

- Misaa

A Partir de las sugerencias, vimos algunas cosas un poco más lento como el circuito astable y monoestable que hemos visto (falta el biestable)  

(foto)

Misaa nos comentó que el ejercicio que vimos la semana pasada era poco académico porque las probabilidades de que fallara eran muy altas, entonces ahora hicimos una variante de esta y nos funcionó (atari punk console)

(hacer tabla de notación científica de resistencias y condensadores)

Para los condensadores no polarizados el último dígito es equivalente a 0; Por ejemplo, 104 equivale a 10.000 pF

- https://www.falstad.com/circuit/
- axidraw
- evil mad scientist
- meneología
- Aniquilar 555

Si el pin 4 del 555 está conectado a tierra nunca va a tener reseteo 

(foto)

### imagenes de proceso

### post-clase

https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard/all

**Diferencia entre condesadores y resistencias:** las resistencias limitan el flujo de corriente disipando energía en calor, por eso son de carbón, ya que el flujo de electrones no es rapido, mientras que los condensadores almacenan energía temporalmente en un campo eléctrico y la liberan.

### tarea

En mi caso estoy desmantelando un equipo que me prestó mi papá, me enseo sus equipos de audio, sus conexiones y de esa conversación él me enseñó el equipo que tengo en mis manos (a la hora de escribir esto no he investigado aún que es para poder hacer un análisis sin ninguna percepción y cuando termine, investigare y dejaré registro)

Este se llama “Active line drive ALD-1”, el cual tiene un ruido que aún no han podido arreglar para poder escuchar música. 

![active line](imagenes/mccormak-ald1-dna1.jpg)

![Active line drive ALD-1](imagenes/active_line_drive_adl1.jpeg)

Es muy fácil de desarmar, solo tenia 8 tornillos de cruz y listo (es hermoso poder reconocer cosas que antes no tenia pensado en saber. Este ramo me ha ayudado a poder hablar más con mi papá)

-------------------------

Dividi en 4 secciones la PCBA:

- Zona 1

![zona 1](imagenes/zona-1.jpeg)

Resistencias:

| # | Banda 1 | Banda 2 | Banda 3 | Banda 4 | Banda 5 | Banda 6 |
|---|--------|--------|--------|--------|--------|--------|
| 1 | rojo   | café   | dorado | negro  | negro  | café   |
| 2 | rojo   | café   | café   | café   | rojo   | rojo   |
| 3 | rojo   | café   | naranja| negro  | negro  | café   |
| 4 | rojo   | café   | dorado | verde  | violeta| amarillo |

Condensadores:

| # | Capacitancia | Voltaje |
|---|-------------|--------|
| 1 | 2200 µF     | 50 V   |
| 2 | 100 µF      | 35 V   |
| 3 | 220 µF      | 63 V   |

Los demás componentes:

| Símbolo | Tipo de componente        | Descripción / Modelo        |
|--------|--------------------------|----------------------------|
| E      | Entradas                 | modelo                     |
| SW     | Interruptor              | Witoft 205 9305            |
| Q      | Transistores             | 5, 6, d                    |
| Q      | Transistores             | K214 Z K5                  |
| Q      | Transistores             | J77 3 H5                   |
| D      | Diodos                   | Z5IN 93J                   |
| D      | Diodos                   | 4935 8026                  |
| D      | Diodos                   | 30B 402                    |
| D      | Diodos                   | J2 30B                     |
| C      | Capacitores              | MKS 4                      |
| C      | Capacitores              | 1.0 µF / 63 V              |
| C      | Capacitores no polarizados | 502                      |
| R      | Resistencias             | 25R 3                      |
| R      | Resistencias             | a 20% 9402          |

-------------------------

- Zona 2

![zona 2](imagenes/zona-2.jpeg)

Resistencias:

| # | Banda 1 | Banda 2 | Banda 3 | Banda 4 | Banda 5 | Banda 6 |
|---|--------|--------|--------|--------|--------|--------|
| 1 | rojo   | café   | café   | amarillo | amarillo | rojo   |
| 2 | rojo   | café   | negro  | blanco   | amarillo | rojo   |
| 3 | rojo   | café   | café   | rojo     | negro    | amarillo |
| 4 | rojo   | café   | café   | amarillo | verde    | café   |
| 5 | rojo   | café   | negro  | celeste  | celeste  | gris   |
| 6 | rojo   | café   | negro  | celeste  | celeste  | celeste|
| 7 | rojo   | café   | café   | café     | rojo     | rojo   |
| 8 | rojo   | café   | café   | amarillo | morado   | rojo   |

Condensadores:

| # | Capacitancia | Voltaje |
|---|-------------|--------|
| 1 | 1000 µF     | 35 V   |
| 2 | 10 µF       | 63 V   |
| 3 | 100 µF      | 35 V   |
| 4 | 100 µF      | 16 V   |

Los demás componentes

| Símbolo | Tipo de componente   | Descripción / Modelo                              |
|--------|----------------------|--------------------------------------------------|
|    -    | Transformador        | Toroidal                                         |
| J      | Jumper               | Puente / conexión interna o selección            |
| D      | Diodos               |-----                          |
| U      | Circuito integrado   | LM317                                            |
| TP     | Punto de prueba      | Punto de prueba                                  |
| Q      | Transistores         | (≈6 patitas, no dice nada)                         |
| XLR    | Conector             | Tipo XLR (audio profesional)                     |

-------------------------

- Zona 3

![zona 3](imagenes/zona-3.jpeg)

Resistencias:

| # | Banda 1 | Banda 2 | Banda 3 | Banda 4 | Banda 5 | Banda 6 |
|---|--------|--------|--------|--------|--------|--------|
| 1 | rojo   | café   | dorado | negro  | verde  | naranja |
| 2 | rojo   | café   | rojo   | negro  | negro  | café   |
| 3 | rojo   | café   | negro  | café   | rojo   | rojo   |
| 4 | rojo   | café   | dorado | café   | rojo   | rojo   |
| 5 | rojo   | café   | negro  | blanco | amarillo | rojo |
| 6 | rojo   | café   | naranja| blanco | blanco | amarillo |

Condensadores:

| # | Capacitancia | Voltaje |
|---|-------------|--------|
| 1 | 100 µF      | 35 V   |

-------------------------

- Zona 4

![zona 4](imagenes/zona-4.jpeg)

Resistencias:

| # | Banda 1 | Banda 2 | Banda 3 | Banda 4 | Banda 5 | Banda 6 |
|---|--------|--------|--------|--------|--------|--------|
| 1 | rojo   | café   | naranja | blanco  | blanco  |  amarillo        |
| 2 | rojo   | café   | dorado  | café    | rojo    | rojo   |

Condensadores:

No hay

-------------------------

- Carcasa (parte delantera)

SW1 → lee si es CD, tuner, video,
tape 1, aux / phono.

SW2 → lee si es tape 1, source, tape 2

PCBA demarca hace conexión con zona 4 lo cual te dirige a la conexión salida con cables. Además lleva a "tape defeat", donde si está encendido,mutear, además del regulador derecha o izquierda.

SW3 → ve si es normal o directo.

R124 → No sé qué es (supondre que es para subir volumen ya que no dice nada)

- Carcasa (parte tracera)

J29, J27, J28, J30 dirigen el transformador toroidal al encendido o apagado además del cable de 230VAC - T315 mA

(Todo lo de adelante se refleja en otros con cables)

J23, J24 (LEFT), J25, J26 (RIGTH) (balancean el output)

desde J1 a J20 siguen conectados previamente hasta CD con L y R.

-------------------------

1. En zonas 2 y 3 hay circuitos integrados de 65448
2. Los GND y TP estan por todas las zonas y tienen un alambre soldado
3. Las E solo estan soladadas
4. El equipo tiene otra PCBA pero esta en vertical la cual sus LED estan hacia afuera. Logro apreciar que tiene condenzadores no polarizados, LED, circuitos integrados de 8 pins, 14 pins y resistencias.
5. Me gusta el diseño de los sectores, muy microdesign
6. Hay una entrada de cable que tienen una conexión con la placa de cables que es GND

(HACER DIBUJOS)



