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

**Precarias**, llamado así por las diferentes situaciones inseguras (errores o la constante broma de que todo iba a explotar) que nos hacía pasar el circuito antes de consolidarse como sintetizador funcional. Este sintetizador esta construido sobre protoboards e integrado a una carcasa de cartón diseñada bajo criterios de experiencia de usuario (UX). El diseño consiste de una interfaz múltiple: una zona táctil (fotoresistor) y otra con potenciómetros situados en el frente y los lateral izquierdo, teniendo así una experiencia con un movimiento combinado (girar-precionar)
El sistema se organiza en cuatro etapas, cada una realizada por un circuito integrado:

+ **Módulo 1:** consta del Clock (555) en modo astable que genera una oscilación constante. Utiliza un potenciómetro para regular carga y descarga, permitiendo un control sobre el ritmo y la actividad del sistema. Además cuenta con un fotoresistor la cual ayuda en la velocidad de la frecuencia.
  
+ **Módulo 2:** es el Secuenciador (4017), este componente recibe la señal del clock la cual se presenta en una secuencia de 4/4. Su función es organizar los pulsos en pasos cronometrados (steps) para dar estructura rítmica.
  
+ **Módulo 3:** Aquí se encuentra el sintetizador (4093), donde le da vida a Precarias. Utiliza compuertas NANDS (Schmitt Trigger) que reciben los pasos del secuenciador; cuenta con 4 potenciómetros y condensadores que ayudan a la frecuencia, en nuestro caso son todos iguales.
  
+ **Módulo 4:** La etapa final de precarias es la salida (386) donde se encarga de procesar las señales de las zonas anteriores para amplificarlas. A través de este chip, la señal se proyecta hacia el parlante, controlado a través de un potenciómetro.

¿Pero qué distingue a Precarias de otros sintetizadores? Precarias consta de dos interfaces interactivas: por un lado, un fotoresistor como control de velocidad, y por otro, potenciómetros, que permiten un control manual más preciso sobre distintos parámetros del sistema.

![final](imagenes/final-sinte.jpg)

Video 1: https://youtube.com/shorts/EZvZhcw6Tzs?feature=share

Video 2: https://youtube.com/shorts/NSwSG6KaihU?feature=share

## proceso y resultados del reloj y secuenciador

### Chips 555

#### Paso 1: Alimentación
El proceso comenzó con la instalación del chip 555 en la protoboard. Se conectan los flujo de energía conectando las energias (cables rojo: positivo y negro: negativo). Luego, se procedió a alimentar el integrado vinculando al pin 1 (tierra) al negativo mediante un cable verde y la pin 8 (VCC) al positivo con un cable café claro.

#### Paso 2: Puentes y Red de Temporización
Para configurar el ciclo del chip, se realizó una interconexión física entre los pins 6 y 2 utilizando un cable café. Desde este nodo, se derivó una conexión hacia un arreglo de resistencias (1k) y un condensador (100 µF), componentes esenciales para definir la frecuencia de la señal. Adicionalmente, la pin 7 se conectó a través de un cable verde a una línea de la protoboard (línea 22), donde se integró a una serie de resistencias para completar la red de descarga.

#### Paso 3: Salida de Señal e Interconexión de Módulos
En la pin 3 (salida) se instaló un cable naranja conectado a un LED rojo con su respectiva resistencia de protección, cerrando el circuito en el polo negativo para visualizar la oscilación. Desde esta misma pata 3, se extendió un cable verde que sirve como puente de interconexión con el siguiente módulo del sistema (4017).

#### Paso 4: Ajustes Finales y Estabilización
Finalmente, se conectó LED pin 5 (control de voltaje) hacia el negativo a través de un condensador sin polaridad. Se aseguró también que el pin 4 (reset) estuviera vinculado al polo positivo para evitar reinicios accidentales, garantizando que el módulo estuviera listo al ver funcionar el LED parpadeando. Por último, Se soldaron la entrada de batería con las entradas dirigidas al negativo y positivo (cables dupont), ya que fue la mayor causante de problemas al salir repetidas veces.

![555](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/555.gif)

### Chips 4017

#### 1. Paso 1: Alimentación
 Al igual que en el módulo anterior, el proceso inició estableciendo las conexiones de alimentación. Se vincularon los negativos de la protoboard y  conectar los pines de energía del chip: pin 8 (VSS) se llevó al negativo y la pin 16 (VDD) al positivo para activar el integrado.
 
#### 2. Paso 2:Control de Lógica y Reset 
Para asegurar el funcionamiento del contador, se realizaron las conexiones de control. El pin 15 (Reset) se conectó al pin 10 para determinar el ciclo de conteo. Asimismo, los pins 14 (Clock) y 13 (Clock Inhibit) se conectaron al polo negativo mediante resistencias de 10k µF, garantizando la estabilidad de las señales de entrada.

#### 3. Paso 3:Interconexión de Salidas
Se reservaron las conexiones de los botones (pins 2, 3, 4 y 7) para la etapa final (sentíamos que era lo más difícil). Con el fin de verificar que el circuito funcionaba correctamente, se instalaron LEDs de prueba. Estos se conectaron desde las cuatro patillas de salida mencionadas hacia las filas 19, 16, 13 y 10 de la protoboard.

#### 4. Paso 4: FUNCIONANDO :)))
Para proteger los componentes, el cátodo de cada LED se conectó al negativo a través de una resistencia de 10k. Esta configuración permite visualizar la secuencia de luces manipulada por el potenciómetro del 555 y confirmar el desplazamiento de la energía para después cambiar los negativos hacia el siguiente módulo 4093.

![4017](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/4017.gif)

![prueba](imagenes/proceso/secuenciador-as-an-img.jpeg)

## proceso y resultados de osciladores y amplificador

### Chips 4093 y Chips 386

![4093 y 386](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/4093-y-386.jpg)

Secuenciador se transforman en frecuencias audibles mediante el uso de compuertas Schmitt Trigger.

#### Paso 1: Alimentación
Conectamos el pin 14 al positivo (VCC) y 7 al negativo (GND). Se instala un condensador cerámico/no polarizado (100nF) entre ambas líneas, ubicándolo lo más cerca posible de los pines de alimentación del chip.

#### 2. Paso 2: Configuración de Osciladores (Steps) 
Conectamos de las cuatro compuertas NAND del 4093 que se configura para recibir un pulso del secuenciador y finalizando con cada STEP doldandolo en el su potenciometro correspondiente para así poder moverse sin inconvenientes en la carcasa:

+ **STEP 1:** la señal proveniente del pin 3 del 4017 que se ingresa a la pin 1. El pin 2 se vincula al potenciómetro RV2 (100k) y condensador de 0.47µF. La salida resultante (pin 3) se dirige al nodo común MIX tras pasar por una resistencia (1k). Logrando una alta frecuncia.
.
+ **STEP 2:** La salida del pin 2 del 4017 se conecta a al pin 5. El pin 6 se asocia a su red RC (potenciómetro RV3 de 100k y condensador de 0.47µF). La señal sale por el pin 4, atraviesa la resistencia (1k) y se une al nodo MIX. Logrando una alta frecuncia.
  
+ **STEP 3:** El pulso del pin 4 del 4017 se lleva a el pin 8. El pin 9 se conecta al circuito de control de tono (potenciómetro RV4 y condensador de 0.47µF). La salida se obtiene en el pin 10, pasando por la resistencia R10 (1k) antes de integrarse al punto de mezcla. Logrando una alta frecuncia.
  
+ **STEP 4:** Finalmente, la señal del pin 7 del 4017 se ingresa al pin 13. el pin 12 se conecta a la última red RC (potenciómetro RV5 y condensador de 0.47µF). La salida por el pin 11 se conduce al nodo MIX a través de la resistencia R11 (1k). Logrando una alta frecuncia.
  
#### 3. Paso 3: Nodo de Mezcla (MIX) 
Al finalizar este proceso, las cuatro señales rítmicas y tonales convergen en el punto MIX. Este nodo unifica las frecuencias generadas y permite crear diferentes vibraciones por cómo se mueven los potenciadores conectados a cada STEP, permitiendo que la suma de todos los osciladores sea enviada a la etapa final de amplificación.

### Chips 386

#### 1. Paso 1: Alimentación
Conectamos el pin 6 a VCC (positivo de la fuente, entre 5V y 9V) y el pin 4 a GND (tierra). Para estabilizar la alimentación, se agrega el capacitor sin polaridad (100nF) entre estas dos líneas. Adicionalmente, se incluye un capacitor (100µF) entre VCC y GND para mejorar el filtrado y reducir ruidos en el sistema.

#### 2. Paso 2: Entrada de Señal y Control de Volumen
La señal proveniente del nodo MIX se dirige a un potenciómetro (100k) para el control del volumen; un extremo se conecta a MIX y el otro a GND. El pin central del potenciómetro entrega la salida ajustada, la cual pasa por el capacitor (100µF) antes de ingresar al pin 3 (entrada de audio) del chip. Por su parte, el pin 2 del LM386 se conecta directamente a GND.

#### 3. Paso 3: Salida hacia el Parlante
La salida del sonido se obtiene gracias al pin 5. Desde este punto, se conecta el capacitor (100µF) en serie, el cual va dirigido hacia el parlante (LS1). Para completar el circuito, el terminal restante del parlante se conecta al nodo de tierra (GND). Finalmenmte soldamos estas conexiones para poder tener seguridad de la conexión. 

![proceso](imagenes/proceso/proceso_1.jpeg)
## modificaciones realizadas a los circuitos originales

### Proceso:

Al iniciar el proceso, implementamos el circuito original entregado y modificado por Misaa con el fin de validar su funcionamiento base y asegurar que la instalación fuera correcta antes de experimentar. A pesar de enfrentar complicaciones técnicas, como errores de conexión y resistencias quemadas, logramos completar el circuito con el íbamos a trabajar.

video de santi: https://youtube.com/shorts/FAeN6yMwqWY?feature=share

Una vez lista la etapa anterior, procedimos a intervenir el circuito del chip 386 para maximizar la potencia y el tono de la salida de audio. Basándonos en la premisa de que valores menores de capacidad alteran la respuesta en frecuencia, sustituimos los condensadores de 100 µF por unos de 0,47 µF en la etapa de amplificación. Con este ajuste, no funcionaba bien el sistema, así que volvimos a poner el anterior condensador.

Posteriormente, probamos realizar cambios en los condensadores vinculados a los potenciómetros. Al utilizar inicialmente valores elevados (10µF), el volumen no alcanzaba la intensidad deseada y buscábamos una mayor variedad tonal, por lo que decidimos sustituirlos por condensadores de 0,47 µF. Este ajuste resultó satisfactorio, ya que proporcionó un sonido notablemente más agudo y potente. Sin embargo, al querer una diversidad de texturas dentro del mismo sistema, decidimos conservar el primer condensador (de izquierda a derecha) con su valor original de 10 µF, logrando así un contraste dinámico entre los diferentes tonos del sintetizador.

Videos del mut: 

![proceso](imagenes/proceso/mut.jpeg)

1: https://youtube.com/shorts/5PpWNb0iPO0?feature=share

2: https://youtube.com/shorts/UJPJm3hy5Yk?feature=share

3: https://youtube.com/shorts/5tdJ-7rMd7w?feature=share

Tras completar el ajuste de los condensadores, el siguiente paso fue sustituir el potenciómetro por un fotorreceptor (sensor de luz) del primer módulo para experimentar nuevas formas de interacción. Este cambio nos intereso para el proyecto, ya que permitía una modulación dinámica del sistema: al aumentar la intensidad lumínica, el dispositivo generaba un sonido más rápido, mientras que en condiciones de oscuridad la velocidad disminuye. 

Al día siguiente, ocurrieron problemas en el circuito, por lo que volvió a armar y se decidió dejar el sensor en vez de el potenciador en el chip 555, y seguir con los mismos elementos que el dia anterior, solo modulando los colores y identificarlos en un dibujo esquemáticos de cada protoboard para identificarse.

### Final:
Al aprender cómo soldar, logramos proponer una nueva versión de carcasa por la mayor seguridad de que no se iban a desconectar ni mover nada, permitiéndonos así soldar los potenciómetros y el parlante de forma fija, eliminando así el riesgo de que los cables chocaran entre si, ya que nos desconectaba el circuito. Además de cambiar a todos los potenciadores de que están conectadas al chip 4093 por condensadores de 0,47 como decisión grupal por gustos de sonido y se notaban la diferencia de sonido independiente de los condenzadores. 

En cuanto a la carcasa, decidimos mantener los potenciómetros y el fotosensor seleccionados previamente, ya que preferíamos que nos permitía controlar la velocidad. Ubicamos el sensor en la parte superior de la carcasa para facilitar su interacción con la luz, mientras que los botones de los potenciómetros se instalaron en el frente y el control de volumen se situó en el lateral izquierdo y también para saber si esta encendido, colocamos en el frente la luz del 555. 
Finalmente, para solucionar el problema recurrente de desconexión entre la batería y las líneas de alimentación, optamos por soldar los terminales directamente a la protoboard donde se encuentra el chip 555. Esto garantizó la estabilidad del flujo eléctrico, dejando la batería accesible por fuera del sistema para que solo tuviera que conectarse al momento de la solemne.


### Esquemático modificado:  

![4017](https://github.com/paulafuentesm/dis8644-2026-1/blob/1e93ee50ea62ca7833c6da25062508df6a0819f1/00-proyecto-01/grupo-06/imagenes/esquematico-modificado-img.jpg)

PDF: (https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/esquematico-modificado.pdf)

![esquemático precarias](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/00-proyecto-01/grupo-06/imagenes/precarias-esquemaatica.jpg)

video: https://youtube.com/shorts/y3wmMXkBmb8?feature=share

video 2: https://youtube.com/shorts/o5TqyCJIAiU?feature=share

## carcasa de cartón

Como grupo decidimos que las interfaces estuvieran distribuidas por paneles para optimizar el uso. En el frente se ubican los cuatro potenciómetros que modifican el sonido, mientras que en un costado izquierdo, a la misma altura, se instaló el potenciómetro encargado de modular el volumen general de Precarias.

Finalmente, en la parte superior, la sección que representó el mayor desafío técnico,ya que, los cables chocaban entre tornados al interior o la carcasa del parlante retumbaba al tener algún scotch, por lo que lo insertamos en el cartón y pegamos a los contados interior el sobrante de cables, se posicionaron el parlante y el fotorreceptor. Esta ubicación estratégica permite que el dispositivo interactúa directamente con los cambios de iluminación ambiental, logrando que el sintetizador se sincronice dinámicamente al captar una luz externa o al percibir el encendido y apagado de las luces de la sala.

## interconexión entre módulos

La interconexión técnica fue un desafío, ya que era un constantemente se nos quemaban las piezas o ver que los pasos realizados fueran correctos, especialmente en la aplicación de soldadura, esto no hizo crear una metodología de colores para el cableado. Este sistema de organización fue clave para guiarnos como equipo, permitiéndonos identificar rápidamente qué cables correspondían a los potenciómetros (pines 2 y 3) y establecer con claridad qué componentes debían ir soldados para asegurar la estructura del diseño.

El primer componente en ser intervenido fue el parlante, utilizando cables rojos y negros para garantizar una conexión sólida y un sonido estable. 

Para después seguir con los condensadores de 0,47 uf  asociados a los potenciómetros, estandarizando el uso de cables específicos para los pines 2 y 3, siendo estos el mismo color diferente en cada potenciador. Para optimizar el tiempo, dividimos las tareas: mientras unos pelaban los cables de colores y negros, otros aplicaban pasta de soldar y realizaban las uniones. Antes de la instalación final en la protoboard, verificamos cada terminal con un medidor de potencia para asegurar que estuviera bien.

Sin embargo, al finalizar los cuatro potenciómetros, detectamos un fallo en el primero de ellos; aunque las mediciones iniciales eran correctas, no lograba modular la frecuencia en el circuito. Tras realizar pruebas cruzadas con resistencias y baterías, notamos que el potenciómetro estaba defectuoso, por lo que procedimos a reemplazarlo y soldar nuevamente hasta que todo el conjunto estuvo operativo.
Al final, notamos que teníamos un constante problema con los cables de la batería, los cuales se soltaban con facilidad y generaban que viéramos todo de nuevo al no notar la principio que volvían a soltarse. Decidimos soldar los conectores de la batería directamente al circuito y así tener la seguridad de que estuvieran conectados el día de la solemne.

## resultados finales

Evidencia de las diferentes fases que paso el proyecto hasta llega a ser “Precarias”:


![resultado](imagenes/proceso/proceso-1.jpg)
![resultado](imagenes/proceso/proceso-3.jpg)
![resultado](imagenes/proceso/proceso-2.jpg)
![resultado](imagenes/proceso/proceso-2.jpeg)

video: https://youtube.com/shorts/MB089a_Y4Zo?feature=share

## aprendizajes y errores

### Aprendizaje: 

Uno de los mayores logros de este semestre fue el fortalecimiento del trabajo en equipo y la capacidad de pedir ayuda. Al reconocer que no éramos expertos, logramos combinar los conocimientos individuales de cada integrante para crear una fuente colectiva de ayuda mutua en el grupo, nadie era experto y todos estábamos aprendiendo, cuando ya pudimos superar la barrera de la frustración y entender esto, pudimos seguir adelante. Esta sinergia fue la que nos permitió llevar a buen puerto el proyecto del sintetizador, también considerando la buena disposición de los integrantes para invertir tiempo fuera de clases para entender y darnos nuestro tiempo para hacer los circuitos.

En cuanto al avance técnico, nuestra evolución fue notable: pasamos de no saber que era y cuál era el uso de una protoboard a manipular con diferentes chips en módulos para hacer sonido, aprendiendo desde el inicio de un 555 y como funcionaban en diferentes contextos. Logramos dominar el flujo de energía, desde lo más básico como encender un LED, hasta procesos más complejos como controlar la sensibilidad de los botones para alterar el sonido con salida a un parlante. Entendimos que no nacemos sabiendo, el ahora poder encontrar un error que antes no podíamos ver, era un aprendizaje, poder entender que un error cometido era un aprendizaje para un futuro. 

### Errores:

En cuanto a los errores, fueron demasiados, tantos que no había clase que no cometieron al menos 3 errores (conexión, ubicación de cable, error de chip) pero eso al menos hacía que tuviéramos más cuidado en esos puntos en la siguiente clase. El principal fue la constante falta de precisión en el montaje de cables y la conexión de los componentes. Al inicio cometimos fallas sistemáticas al confundir los orificios de la protoboard, conectando cables en pines incorrectos, lo que provocó que quedáramos múltiples chips 555 (tuvimos que ir a comprar más durante las semanas), resistencias y LEDs. Estos errores de conexión eran tan recurrentes que nos obligaban a repetir los módulos, desarmar todo y volverlo desde 0,  hasta tres veces por clase. Se nos olvidaba conectar el paso de energía entre protoboard, lo que hacía que los circuitos no funcionaran al no circular la energía.

Además, sufrimos de una grave falta de estandarización y orden colectivo en el manejo de los módulos. No establecimos un código de colores grupal para los cables lo que nos hacía estresarnos y estar minutos viendo uno por uno cuál era el error en una ensalada de cables, lo que generaba confusión y pérdida de tiempo cada vez que un integrante distinto tomaba el circuito. La fragilidad de nuestras conexiones fue un error persistente hasta la última clase; los cables se soltaban y no sabíamos dónde iban  o se ubicaban mal por la falta de un sistema de trabajo. Este desorden en la conducción colectiva del sistema nos hacía volver a hacer el sistema por algún cable que no sabíamos dónde iba.

## conclusiones

Fue un trabajo complejo, como mencionamos en el punto anterior, el cual tomó mucho tiempo, dedicación y odio-cariño. Poder estar sumergidos en el “estrés” y sentirlo por estar aprendiendo algo nuevo y si, es una frase que seguiremos repitiendo porque de esto hace un mes no sabíamos nada pero ahora sabemos un 1% y estamos orgullosos de ese pequeño paso, quedan varios o ya está el punto de partida para nosotros en el futuro si deseamos seguir explorando. Es por esto que hay muchos puntos que podemos tocar en esta primer entrega:

En cuanto a la modularidad, comprendimos la importancia de los diferentes chip, destacando el que mas sufrió, el chip 555. Al ser el componente más básico y versátil, todos logramos dominar su configuración. Sin embargo, aprendimos por experiencia propia que su aparente sencillez no lo hace menos delicado: es sumamente fácil de quemar si no se manipula con el cuidado necesario, una lección técnica que quedó grabada en nuestro flujo de trabajo.

Respecto al trabajo en equipo, el desempeño fue excelente. Logramos una dinámica equitativa donde cada integrante aportó de manera significativa, manteniendo siempre la disposición para trabajar fuera del horario de clases. La ausencia de conflictos y la capacidad de llegar a consensos de forma ágil y rápida nos consolidó como un grupo cohesionado y eficiente, lo cual fue vital para sacar adelante el sintetizador.
Sobre el manejo eléctrico y la distribución, implementamos una metodología propia en la protoboard. Establecimos un código de colores específico para los elementos comunes y estandarizamos la comunicación interna para que todos supiéramos qué cables correspondían a cada sección. Esto facilitó el entendimiento del flujo de energía, ayudándonos a prevenir cortocircuitos y asegurando que la conexión entre las distintas placas fuera efectiva.

Originalmente, decidimos asignar un chip por cada protoboard para mantener el orden, aunque tuvimos que adaptar este plan a último minuto tras el fallo de una de las placas. Optamos por usar una placa de mayor tamaño para los últimos dos módulos, pero manteniendo la mecánica de trabajo previa. Este sistema nos permitió mover componentes y comunicarnos con mayor comodidad, demostrando nuestra capacidad de adaptación técnica ante imprevistos.

Tras superar los múltiples problemas técnicos que nos obligaron a cranearnos la cabeza constantemente, simplificamos el diseño de la carcasa. Elegimos cartón corrugado para realizar un corte láser preciso, lo que nos permitió integrar los botones impresos en 3D de manera óptima. Esta decisión final no solo cerró el proceso de fabricación, sino que garantizó una mejor experiencia de uso  para nuestro sintetizador.

Finalmente queremos agradecer como grupo a Nicolás, Vania y Anto por ayudarnos en todo nuestro proceso. A cami por siempre estar dispuesta a todo y realizarnos luestras perillas para condenzadores. 
