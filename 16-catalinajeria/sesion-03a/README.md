# sesion-03a

## Clase 24-03-2026

### Apuntes de la clase

En esta clase comenzamos a trabajar con sonido a partir de circuitos electrónicos, entendiendo cómo la oscilación y la frecuencia permiten generar distintos tonos utilizando el chip 555.

Se retomó el circuito de la clase anterior y se explicó que el 555 funciona generando una señal que oscila entre 0V y 9V, cargando y descargando un capacitor constantemente. Esto genera un encendido y apagado continuo, formando una señal periódica.

### Frecuencia y oscilación

La frecuencia corresponde a la cantidad de veces que una señal se repite en un segundo.

- Mientras más rápida es la oscilación → mayor frecuencia → sonido más agudo  
- Mientras más lenta es la oscilación → menor frecuencia → sonido más grave  

También se explicó que:

F = 1 / T  

Donde:
- F es la frecuencia  
- T es el período (tiempo que tarda en repetirse un ciclo)  

El capacitor influye directamente en esto:
- Mayor valor en µF → oscilación más lenta  
- Menor valor en µF → oscilación más rápida  

### Circuito con parlante

Se incorporó un parlante al circuito para transformar la señal eléctrica en sonido.

El funcionamiento es:
- El chip genera una señal eléctrica  
- Esta señal mueve los imanes del parlante  
- Se transforma en vibración (sonido)  

Se recomendó usar un capacitor de 100 µF para el parlante, ya que ayuda a suavizar la señal.

### Estructura del circuito

Se explicó que el circuito se puede dividir en tres partes:

- Input (entrada): donde se controla la señal (ej: fotoresistor, potenciómetro)  
- Proceso: el chip 555 (caja negra)  
- Output (salida): LED o parlante  

Este tipo de circuito se llama **astable**, porque no tiene un estado fijo, sino que está cambiando constantemente (oscilando).

### Componentes utilizados

**Potenciómetro:**
- Permite controlar manualmente la frecuencia  
- Cambia el tono del sonido  

**Fotoresistor (LDR):**
- No tiene polaridad  
- Cambia su resistencia según la luz  
- Permite modificar el sonido automáticamente  

**Botón (switch):**
- Funciona como interruptor momentáneo  
- Solo deja pasar la señal mientras se mantiene presionado  
- Tiene 4 patas, pero se conectan en diagonal  
- Se debe colocar con el lado plano hacia abajo en la protoboard  

### Conceptos importantes

- VCC: voltaje positivo  
- GND: tierra o negativo  
- Siempre desconectar la batería antes de modificar el circuito  
- La distribución en la protoboard es importante para que funcione correctamente  

También se mencionó que con resistencias y capacitores se pueden filtrar señales, modificando el comportamiento del circuito.

### Actividad realizada

Se trabajó en un circuito tipo “toy organ”, donde se agregaron botones para generar distintos sonidos.

La idea fue:
- Mantener el circuito base  
- Agregar switches  
- Modificar la frecuencia para obtener distintos tonos  

También se hicieron pruebas en simuladores como Tinkercad antes de armar el circuito físico.

### Conclusión

En esta clase se entendió cómo la oscilación y la frecuencia están directamente relacionadas con el sonido en los circuitos electrónicos. Fue importante ver cómo el chip 555 puede generar señales que luego se transforman en audio mediante un parlante.

Además, el uso de componentes como el potenciómetro, el fotoresistor y los botones permitió hacer el circuito más interactivo y experimentar con distintos sonidos.
