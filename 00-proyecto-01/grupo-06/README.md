# grupo-06

![Título](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/titulo.gif)

**Realizado por:**  
*Paula Fuentes Mena (paulafuentesm)*
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
*Santiago Cifuentes Vélez (santiagocifuvelez)*&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
*Kristel Ladrón de Guevara Jara (kristelagj)*

<br>
 <br>
  <br>
   <br>
   
"Quienes no se mueven no notan sus cadenas"   
*—Rosa Luxemburg*

<br>
 <br>
  <br>
   <br>

Hola! Bienvenidxs a la presentación de nuestro solemne 01.   
Antes de partir, quiero agradecerles a mis compañeras por su esfuerzo y compromiso con el proyecto.  
Hicimos algo mágico.

Comencemos:  

## descripción del sintetizador realizado

**Precarias**, llamado así por las diferentes situaciones inseguras ( errores o la constante broma de que todo iba a explotar) que nos hacía pasar el circuito antes de consolidarse como sintetizador funcional. Un sintetizador construido sobre protoboards e integrado en una carcasa de cartón diseñada bajo criterios de experiencia de usuario (UX). El diseño consiste de una interfaz múltiple: una zona táctil (fotoresistor) y otra con potenciómetros situados en el frente y los lateral izquierdo, teniendo así una experiencia multisensorial. 
El sistema se organiza en cuatro etapas, cada una realizada por un circuito integrado:

+ **Módulo 1:** consta del Clock (555) en modo astable que genera una oscilación constante. Utiliza un potenciómetro para regular carga y descarga, permitiendo un control sobre el ritmo y la actividad del sistema. Además cuenta con un fotoresistor la cual ayuda en la velocidad de la frecuencia. 
+ **Módulo 2:** es el Secuenciador (4017), este componente recibe la señal del clock la cual se presenta en una secuencia de 4/4. Su función es organizar los pulsos en pasos cronometrados (steps) para dar estructura rítmica.
+ **Módulo 3:** Aquí se encuentra el sintetizador (4093), donde le da vida a Precarias. Utiliza compuertas NANDS (Schmitt Trigger) que reciben los pasos del secuenciador; cuenta con 4 potenciómetros y condensadores que ayudan a la frecuencia, en nuestro caso son todos iguales.
+ **Módulo 4:** La etapa final de precarias es la salida (386) donde se encarga de procesar las señales de las zonas anteriores para amplificarlas. A través de este chip, la señal se proyecta hacia el parlante, controlado a través de un potenciómetro.

¿Pero qué distingue a Precarias de otros sintetizadores? Precarias incorpora una diversidad de condensadores, los cuales influyen directamente en la variación de las frecuencias y sonido del sintetizador. Además, el dispositivo cuenta con dos interfaces interactivas múltiple: por un lado, un fotoresistor como control de velocidad, y por otro, potenciómetros, que permiten un control manual más preciso sobre distintos parámetros del sistema.

foto y video 

## proceso y resultados del reloj y secuenciador

### Chips 555

#### Paso 1: Alimentación
El proceso comenzó con la instalación del chip 555 en la protoboard. Se conectan los flujo de energía conectando las energias (cables rojo: positivo y negro: negativo). Luego, se procedió a alimentar el integrado vinculando al pin 1 (tierra) al negativo mediante un cable verde y la pin 8 (VCC) al positivo con un cable café claro.

#### Paso 2: Puentes y Red de Temporización
Para configurar el ciclo del chip, se realizó una interconexión física entre los pins 6 y 2 utilizando un cable café. Desde este nodo, se derivó una conexión hacia un arreglo de resistencias (1k) y un condensador (100 uf), componentes esenciales para definir la frecuencia de la señal. Adicionalmente, la pata 7 se conectó a través de un cable verde a una línea de la protoboard (línea 22), donde se integró a una serie de resistencias para completar la red de descarga.

#### Paso 3: Salida de Señal e Interconexión de Módulos
En la pata 3 (salida) se instaló un cable naranja conectado a un LED rojo con su respectiva resistencia de protección, cerrando el circuito en el polo negativo para visualizar la oscilación. Desde esta misma pata 3, se extendió un cable verde que sirve como puente de interconexión con el siguiente módulo del sistema (4017).

#### Paso 4: Ajustes Finales y Estabilización
Finalmente, se conectó lel pin 5 (control de voltaje) hacia el negativo a través de un condensador sin polaridad. Se aseguró también que el pin 4 (reset) estuviera vinculado al polo positivo para evitar reinicios accidentales, garantizando que el módulo estuviera listo al ver funcionar el LED parpadeando. Por último, Se soldaron la entrada de batería con las entradas dirigidas al negativo y positivo ( cables dupont) , ya que fue la mayor causante de problemas al salir repetidas veces.

![555](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/555.gif)

### Chips 4017

#### 1. Paso 1: Alimentación
 Al igual que en el módulo anterior, el proceso inició estableciendo las conexiones de alimentación. Se vincularon los negativos de la protoboard y  conectar los pines de energía del chip: pin 8 (VSS) se llevó al negativo y la pin 16 (VDD) al positivo para activar el integrado.
 
#### 2. Paso 2:Control de Lógica y Reset 
Para asegurar el funcionamiento del contador, se realizaron las conexiones de control. El pin 15 (Reset) se conectó al pin 10 para determinar el ciclo de conteo. Asimismo, los pins 14 (Clock) y 13 (Clock Inhibit) se conectaron al polo negativo mediante resistencias de 10k uf, garantizando la estabilidad de las señales de entrada.

#### 3. Paso 3:Interconexión de Salidas
Se reservaron las conexiones de los botones (pins 2, 3, 4 y 7) para la etapa final ( sentíamos que era lo más difícil). Con el fin de verificar que el circuito funcionaba correctamente, se instalaron LEDs de prueba. Estos se conectaron desde las cuatro patillas de salida mencionadas hacia las filas 19, 16, 13 y 10 de la protoboard.

#### 4. Paso 4: FUNCIONANDO :)))
Para proteger los componentes, el cátodo de cada LED se conectó al negativo a través de una resistencia de 10k . Esta configuración permite visualizar la secuencia de luces manipulada por el potenciómetro del 555 y confirmar el desplazamiento de la energía para después cambiar los negativos hacia el siguiente módulo 4093.

![4017](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/4017.gif)

incluir texto e imágenes sobre cableado, pruebas, resultados obtenidos.

## proceso y resultados de osciladores y amplificador

### Chips 4093
Secuenciador se transforman en frecuencias audibles mediante el uso de compuertas Schmitt Trigger.

#### Paso 1: Alimentación
Conectamos los pines 14 al positivo (VCC) y 7 al negativo (GND). Se instala un condensador cerámico (100nF) entre ambas líneas, ubicándolo lo más cerca posible de los pines de alimentación del chip.

#### 2. Paso 2: Configuración de Osciladores (Steps) 
Conectamos de las cuatro compuertas NAND del 4093 se configura para recibir un pulso del secuenciador y finalizando cada STEP con la soldadura en el potenciador para poder moverse sin inconvenientes por la carcasa:

+ **STEP 1:** La señal proveniente del pin 3 del 4017 se ingresa a la pin 1. El pin 2 se vincula al potenciómetro RV2 (100k) y el condensador C5 (10uF). La salida resultante (pin 3) se dirige al nodo común MIX tras pasar por una resistencia (1k). Logrando un ruido más grave y con poco volumen por el tamaño del condensador.
.
+ **STEP 2:** La salida del pin 2 del 4017 se conecta a al pin 5. El pin 6 se asocia a su red RC (potenciómetro RV3 de 100k y condensador de 0.47uF). La señal sale por el pin 4, atraviesa la resistencia (1k) y se une al nodo MIX. Logrando un ruido chillón y con un mayor volumen por el tamaño del condensador.
  
+ **STEP 3:** El pulso del pin 4 del 4017 se lleva a el pin 8. El pin 9 se conecta al circuito de control de tono (potenciómetro RV4 y condensador C3). La salida se obtiene en el pin 10, pasando por la resistencia R10 (1k) antes de integrarse al punto de mezcla. Logrando un ruido igual de chillón y con igual volumen que el STEP 2 por el tamaño del condensador.
  
+ **STEP 4:** Finalmente, la señal del pin 7 del 4017 se ingresa al pin 13. el pin 12 se conecta a la última red RC (potenciómetro RV5 y condensador C4). La salida por el pin 11 se conduce al nodo MIX a través de la resistencia R11 (1k). Logrando un ruido igual de chillón y con igual volumen que el STEP 2 por el tamaño del condensador.
  
#### 3. Paso 3: Nodo de Mezcla (MIX) 
Al finalizar este proceso, las cuatro señales rítmicas y tonales convergen en el punto MIX. Este nodo unifica las frecuencias generadas y permite crear diferentes frecuencias de  vibraciones por cómo se mueven los potenciadores conectados a cada STEP, permitiendo que la suma de todos los osciladores sea enviada a la etapa final de amplificación.

### Chips 386

Etapa de Amplificación de Audio (IC LM386)

#### 1. Paso 1: Alimentación
Conectamos el pin 6 a VCC (positivo de la fuente, entre 5V y 9V) y el pin 4 a GND (tierra). Para estabilizar la alimentación, se agrega el capacitor sin polaridad (100nF) entre estas dos líneas. Adicionalmente, se incluye un capacitor (100uF) entre VCC y GND para mejorar el filtrado y reducir ruidos en el sistema.

#### 2. Paso 2: Entrada de Señal y Control de Volumen
La señal proveniente del nodo MIX se dirige a un potenciómetro (100k) para el control del volumen; un extremo se conecta a MIX y el otro a GND. El pin central del potenciómetro entrega la salida ajustada, la cual pasa por el capacitor (100uF) antes de ingresar al pin 3 (entrada de audio) del chip. Por su parte, el pin 2 del LM386 se conecta directamente a GND.

#### 3. Paso 3: Salida hacia el Parlante
La salida de audio se obtiene desde pin 5. Desde este punto, se conecta el capacitor (100uF) en serie, el cual va dirigido hacia el parlante (LS1). Para completar el circuito, el terminal restante del parlante se conecta al nodo de tierra (GND). Finalizando con la soldadora de estas conexiones para poder tener una seguridad de conexión. 

imágenes sobre cableado, pruebas, resultados obtenidos.

## modificaciones realizadas a los circuitos originales

### Esquemático modificado:  
(https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/esquematico-modificado.pdf)

incluir texto, imágenes sobre modificaciones realizadas a los circuitos originales, incluyendo el proceso de diseño, pruebas y resultados obtenidos.

incluir modificaciones en posición, chips, parámetros, valores, etc.

## carcasas de cartón

textos, imágenes

incluir origen de materiales, decisiones de posiciones de los componentes, decisiones estéticas, pruebas, resultados obtenidos.

## interconexión entre módulos

textos, imágenes, diagramas de interconexión

## resultados finales

texto

imagen

video / audio

## aprendizajes y errores

las mejores lecciones aprendidas y los errores más comunes y cómo los resolvieron

## conclusiones

sobre modularidad, materialidad, trabajo en equipo, trabajo electrónico, trabajo maquinal.
