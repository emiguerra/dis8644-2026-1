# sesion-06a
## Apuntes 14 abr
### Schmitt Trigger
Es un circuito comparador que utiliza histéresis para limpiar señales. Básicamente, es el "filtro de estabilidad" de la electrónica: toma señales analógicas ruidosas, lentas o con interferencias y las convierte en ondas cuadradas digitales perfectas.

**La Histéresis:**

A diferencia de un comparador común que tiene un solo umbral, el Schmitt Trigger tiene dos:
+ Umbral Superior ($V_{cc+}$): La señal de entrada debe subir por encima de este punto para que la salida cambie.
+ Umbral Inferior ($V_{cc-}$): La señal debe bajar de este punto para volver al estado anterior.

**Segun gemini sus aplicaciones principales serian:**
+ Eliminación de rebote (Debouncing): Ideal para botones físicos que, al presionarse, generan múltiples pulsos mecánicos. El Schmitt Trigger asegura que solo se registre un pulso limpio.
+ Conversión de ondas: Transforma ondas senoidales o triangulares en ondas cuadradas perfectas.
+ Osciladores: Es la base de muchos osciladores simples (como los que se usan en síntesis de sonido) cuando se combina con una resistencia y un condensador.Limpieza de datos: Se usa para recuperar señales digitales que se han degradado o llenado de ruido durante su transmisión.

imagen apunte

### Chips
+ **4093** Contiene 4 puertas NAND, pero con una característica especial: cada entrada tiene un Schmitt Trigger.
   + solo oscila si pin 2=V++
     
imagen chip

+ **4017** el secuenciador de pasos. Es el chip que permite que las luces (o los sonidos) se activen uno por uno en orden.
  
imagen chip

### hacemos ruido
En la clase missa nos enseño la coneccion entre el chip 4017 (secuenciador) y el 4093 (sintetizador). que sirve para generar ritmos o melodias sencillas.

imagen pizarra

### En clases 
Realizamos el circuito de todos los chips el 555→4017→4093→385
+ 555 clok
+ 4017 secuenciador
+ 4093 sintetizador
+ 385 salida

imagen circuito

### Bitácora
+ Con mi grupo logramos armar todo el circuito, pero al principio nos llevamos una decepción: no sonaba nada. La primera parte, que es el "reloj" (lo que marca el ritmo) y el secuenciador (el chip 4017 que hace que las luces avancen), funcionaba perfecto. Los LEDs prendían uno tras otro en orden, pero al conectar los pasos para que generaran audio, el parlante seguía mudo.

+ Buscando el error:
Revisamos los cables mil veces para ver si nos habíamos equivocado en alguna conexión, pero todo parecía estar bien puesto. Al final, decidimos probar cambiando el chip 4093. En cuanto pusimos el nuevo, ¡por fin salió sonido! El problema era simplemente que el chip anterior estaba quemado.

+ El problema del sonido:
Aunque ya sonaba, el resultado no era el que esperábamos. El sonido era muy "plano", como un pitido constante que no cambiaba nada. Además, no seguía el ritmo de las luces; en vez de sonar "pun - pun - pun" al ritmo de los LEDs, se escuchaba un ruido eterno que no paraba nunca. No sabíamos cómo hacer para que el sonido se cortara o variara según el paso que estaba encendido.

+ Por discord los profes nos dijeron que habia que hacerle algunas variaciones al circuito para que mejorara el sonido y que en la clase lo ibamos a revisar juntos, nos quedamos mas tranquilos con mi grupo a la espera de la siguente clase.
  
+ Aqui una prueba del sonido que logramos obtener antes de las variaciones.

https://github.com/user-attachments/assets/c6b2f5e4-d381-4418-994f-0781fdd90e9c



