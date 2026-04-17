# Sesion-04a Martes 31 de Marzo 2026

Temas: Configuración NE555P, Atenuación por Potenciómetro y Notación Científica.

# Análisis de Sistemas en Cascada y Gestión de Errores

En electrónica, un sistema en cascada es cuando conectas varios bloques (circuitos) uno tras otro, de modo que la salida del primero es la entrada del segundo. 🌊

Sí lo imagino, como una fila de fichas de dominó: la primera tiene que caer para que la segunda se mueva.

En nuestra clase, lo usamos así con los dos chips 555:
1. El Flujo de Señal

    * **Bloque A (Monostable):** Presióno un botón y este chip genera un pulso de energía que dura, por ejemplo, 5 segundos.
    * **Bloque B (Astable):** Este chip está "dormido". Solo se despierta y empieza a parpadear el LED cuando recibe la energía que viene del Bloque A.
    * **Resultado:** El LED parpadea solo durante esos 5 segundos y luego todo se apaga.

2. ¿Por qué se llama así?

Se usa la metáfora de la cascada (waterfall/Cascada) porque el flujo de información o electricidad cae de un nivel al siguiente. Si el primer bloque falla o no se activa, el segundo nunca se entera de que tiene que trabajar.

❗ojo con esto (error común/misconception):

Mucha gente cree que en un sistema de cascada los dos chips funcionan al mismo tiempo. pero no. la señal "cae" de uno al otro en orden. si el primer chip (monostable) no dispara el pulso, el segundo (astable) ni se entera y se queda muerto. es una cadena, no un trabajo en equipo en paralelo.


📝Ejemplo

Un sistema de alarma:

    El sensor de movimiento (Bloque 1) detecta algo y manda una señal.
    Esa señal activa un temporizador (Bloque 2) que espera 30 segundos.
    Si no pones la clave, ese tiempo activa la sirena (Bloque 3).

Cada etapa depende de la anterior. Eso es cascada.


**🚀 En el protoboard que armamos, la "cascada" es ese cable que sale de la pata 3 del primer chip y va hacia el segundo para darle la orden de empezar.** 

1. **El condensador (Pico):** Trabajamos con prefijos como pico (10−1210−12), que es una millonésima de millonésima parte de un Faradio. Es algo casi invisible de lo pequeño que es.
2. **La Zipbomb (Yotta):** El profe o alguien mencionó el caso de las "bombas de compresión". Existe una teórica que pesa 55.4 Yottabytes (10241024). El prefijo Yotta es el más grande que reconoce el Sistema Internacional oficialmente.

**La matemática no miente: Si vas desde el −12−12 (pico) hasta el +24+24 (yotta), tienes que saltar 36 espacios en la línea numérica.**

💡Diferencia Abismal

Para tener una idea, una diferencia de 36 órdenes de magnitud es como comparar el tamaño de un protón con el tamaño de toda la Vía Láctea... ¡y todavía sobraría espacio!

🧐 ¿Qué tan grande es esa diferencia?

Sí me lo imagino, sería algo como: si el Pico fuera del tamaño de una hormiga...

    1 orden (x10): Una hormiga de 10 cm.
    6 órdenes (x1.000.000): Una hormiga del tamaño de un estadio de fútbol.
    15 órdenes: Una hormiga que llega de la Tierra al Sol.
    36 órdenes: ... ¡Ni siquiera el Universo entero alcanza para que quepa esa hormiga! 🌌🐜

**💠 Notación Científica y Escalado de Unidades**

Para no quemar nada, el profe profundizó en los órdenes de magnitud. Es crítico no marearse con los ceros en electrónica de precisión:
| abreviación | prefijo | número real | potencia | aplicación típica |
| --- | --- | --- | --- | --- |
| M | Mega | 1.000.000 | 10^6| Resistencias de alta impedancia |
| k | Kilo | 1.000 | 10^3 | Resistencias estándar (1k,10k)|
| - | unidad | 1 | 10^0| Voltios / Amperios |
| m | mili | 0,001 | 10^-3| Consumo de corriente / Tiempo |
| μ | micro | 0,000001 | 10^-6| Capacitancia electrolítica |
| n | nano | 0,000000001 | 10^-9| Capacitancia de poliéster |
| p | pico | 0,000000000001 | 10^-12| Capacitancia cerámica |


Hoy la sesión se puso intensa con la implementación de una arquitectura en cascada. El objetivo era que un chip le "hablara" al otro, pero me costó un mundo que funcionara a la primera. Saqué varias fotos del protoboard porque el caos de cables era real y necesitaba documentar cada paso.

**El ejercicio en cuestión :)**

<img src="https://github.com/user-attachments/assets/595692f6-4ad2-4309-aada-597866ac5971" width="1000%"> 

🤝 Tierra Común: El Punto de Referencia

Este es el concepto más importante para que cualquier sistema de múltiples chips funcione. En el pizarrón, la línea roja que une las partes bajas de los dos 555 se llama Tierra Común (GND).

    El Problema: Si cada chip tuviera su propia "tierra" separada, el segundo chip no entendería la señal que le manda el primero. Sería como si dos personas trataran de medirse la altura, pero una estuviera parada en el suelo y la otra arriba de una mesa; el resultado no tendría sentido.
    La Solución: Al unir todos los negativos del circuito a un solo punto (la línea azul del protoboard), establecemos un voltaje cero real para todo el sistema. Así, el pulso de salida del chip 1 tiene un camino claro para "caer" hacia la entrada del chip 2.


**Mi proceso**

<img src="https://github.com/user-attachments/assets/db77bac7-da80-43a5-8d4f-2b5c63f404e7" width="33%"> 
<img src="https://github.com/user-attachments/assets/771fcf3e-1416-4f8a-b3b8-ce6a588d4e6e" width="33%"> 
<img src="https://github.com/user-attachments/assets/7510303b-3288-426e-9c39-52c54aaf0877" width="33%"> 


 **🛠️ Desarrollo Experimental y Debugging (Mi pelea con el hardware)**

La clave fue interconectar dos bloques del Chip NE555P para que el estado lógico de uno condicionara al siguiente. Aquí anoté mi proceso de resolución de problemas:

1. **Estado de Reset Permanente (El error del cable negro):** En mis primeras pruebas (se ve en la foto 1), el circuito no hacía nada. Me di cuenta que leí mal el esquemático y conecté el Pin 4 (Reset) a GND. Como el reset es activo en bajo, el chip estaba inhibido permanentemente. Tuve que puentear el Pin 4 a VCC para habilitar la lógica interna.
2. **Desviación de Frecuencia (Confusión de resistencias):** Me mareé con el código de colores y puse una resistencia de 100 ΩΩ (marrón-negro-marrón) donde el circuito requería una de 10k ΩΩ (marrón-negro-naranja). Esto hizo que la frecuencia de oscilación fuera superior al umbral de percepción visual (>60Hz>60Hz), por lo que el LED azul parecía prendido fijo. Lo recalibré usando los valores correctos y ahí recién empezó a parpadear. 🚨
3. **Integridad de Conexiones:** En las fotos se ve el desorden de cables. Aprendí por las malas que si en el simulador Falstad ves puntos rojos, es porque hay nodos abiertos. En el protoboard real me pasó lo mismo: un par de cables no hacían contacto y por eso el lazo de corriente no cerraba.
4. **Atenuación de Salida:** Añadimos un potenciómetro de salida para que actuara como un divisor de tensión variable. Esto nos permitió controlar el volumen de la señal antes de la etapa de salida (parlante).


# Auto ayuda para aprenderme los valores de las resistencias 
| Valor | Colores | Cómo leerlo rápido |
| --- | --- | --- |
| 220 Ω\\OmegaΩ | Rojo - Rojo - Marrón | 2 - 2 + un cero (220220220) |
| 1k Ω\\OmegaΩ | Marrón - Negro - Rojo | 1 - 0 + dos ceros (1.0001.0001.000) |
| 10k Ω\\OmegaΩ | Marrón - Negro - Naranja | 1 - 0 + tres ceros (10.00010.00010.000) |
| 100k Ω\\OmegaΩ | Marrón - Negro - Amarillo | 1 - 0 + cuatro ceros (100.000100.000100.000) |

📝 Ejemplo: Si ves Rojo - Rojo - Marrón:

    Rojo = 2
    Rojo = 2
    Marrón = un 0 Resultado: 220 Ohmios.


1. Si la 3ª es Marrón: La resistencia es de cientos (ej: 220, 330, 470).
2. Si la 3ª es Rojo: La resistencia es de miles (ej: 1k, 2.2k, 4.7k).
3. Si la 3ª es Naranja: La resistencia es de diez miles (ej: 10k, 22k, 47k).

# 🕵️‍♀️ Encargo 04a: Desarmando una Radio Vieja

1. **El proceso de "destripado"** Abrir esta radio fue un lío porque los tornillos estaban súper apretados. Al final logré separarla y me encontré con la placa café llena de piezas. Pude reconocer al tiro las resistencias por los colores que vimos en clase y los capacitores que parecen mini tanques negros. También hay un chip negro con hartas patas que está justo al medio de todo el circuito y al lado del chip también hay un LED verde chiquitito que supongo que es el que avisa cuando la radio está encendida y recibiendo energía.

<img src="https://github.com/user-attachments/assets/da6026a3-6c3d-4d5d-86eb-3f1218a4f812" width="33%"> 
<img src="https://github.com/user-attachments/assets/c0b0085f-a2ec-4b4f-b633-d9e8cd4ff834" width="33%"> 
<img src="https://github.com/user-attachments/assets/14f510c7-e3b8-4809-af5e-79cf4266aff6" width="33%"> 

2. **Conexiones con la carcasa** La placa está conectada a la carcasa por varios cables de colores (amarillo y verde) que van directo al parlante, que es esa pieza redonda gigante. También están las ruedas de plástico que uno mueve por fuera para buscar la música; esas ruedas mueven unas piezas que están soldadas a la placa para que la radio pesque la señal.
<img src="https://github.com/user-attachments/assets/77057278-6939-489c-832a-ff6f3e921591" width="23%"> 
<img src="https://github.com/user-attachments/assets/bd3dfcd5-7611-46ae-887c-f563c3f668e8" width="38%"> 
<img src="https://github.com/user-attachments/assets/e4167c48-f2b2-49b5-b65e-4946ebd48988" width="38%"> 

3. Funcionamiento imaginario: "La red que atrapa el viento"

Para mí, esta radio es como una telaraña de cobre gigante escondida en una caja de plástico. La antena, con todos esos hilos enrollados, no es solo metal; es una trampa para cazar los susurros que viajan por el aire. Me imagino que las canciones son como pájaros invisibles que se quedan enredados en el cobre y bajan disparados por los cables amarillos hacia la placa café, que es el suelo de este mundo mecánico.

En ese suelo, los capacitores negros parecen pequeños silos de agua donde la electricidad se queda quieta un rato para recuperar el aliento. Las resistencias, con sus anillos de colores, son como túneles estrechos que obligan a la energía a ir más lento para no inundar el resto de la ciudad. Todo ese desorden de piezas está ahí para que el chip central, que parece un insecto negro pegado a la placa, pueda traducir los choques eléctricos en palabras que nosotros entendamos.

Al final, el parlante es como el tambor de un chamán que empieza a vibrar cuando la electricidad lo golpea. Los cables verdes y amarillos son las venas que llevan la sangre eléctrica hasta ese tambor de metal y cartón. Cuando el imán de atrás empuja el aire, esos susurros que la antena cazó al principio por fin escapan de la radio convertidos en música, saliendo por los hoyitos de la carcasa como si fueran el último aliento de una máquina que nunca duerme.
<img src="https://github.com/user-attachments/assets/6ea51125-a183-45d1-ade2-92912f5274e0" width="800%"> 

Nota Personal: Esta radio es una verdadera guerrera. Acompaño a mi abuela en los terremotos más fuertes aquí en Chile, y a pesar de todos los golpes que tiene, sigue funcionando impecable. Comparada con los equipos actuales, que son mucho más sofisticados y compactos, esta radio tiene una electrónica más robusta y simple que la hace legendaria. Esta joya está hecha para durar y no morir nunca, sin importar cuántas veces se caiga.
