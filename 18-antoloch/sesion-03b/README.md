# sesion-03b
# Apuntes de Clase
##  Resistencia Equivalente (Req)
La **resistencia equivalente** es el valor único que reemplaza varias resistencias en un circuito, manteniendo el mismo efecto eléctrico.

- **Serie:**  
  La corriente es la misma en todas las resistencias, por lo que se suman directamente:  
  \[
  R_{eq} = R_1 + R_2 + R_3 + \dots
  \]

- **Paralelo:**  
  El voltaje es común, y se calcula con la suma de los recíprocos:  
  \[
  \frac{1}{R_{eq}} = \frac{1}{R_1} + \frac{1}{R_2} + \frac{1}{R_3} + \dots
  \]

- **Caso especial (dos resistencias en paralelo):**  
  \[
  R_{eq} = \frac{R_1 \cdot R_2}{R_1 + R_2}
  \]

- **Posibilidades de cambios en el circuito:**  
  - Variar resistencias o capacitores para modificar tiempos o frecuencias.  
  - Usar potenciómetros para tener control ajustable.  
  - Incorporar diodos para diferenciar la carga y descarga del condensador.  

---

## Circuito Monoestable con 555
- **Realizamos un circuito monoestable** con el temporizador 555.  
- Tiene un solo estado estable (reposo).  
- Al recibir un pulso externo, genera un único pulso cuya duración depende de la resistencia y el condensador.  
- En la práctica, el LED se encendía unos segundos y luego se apagaba.  
- Al inicio fue difícil, incluso un chip se dañó, pero finalmente logramos hacerlo funcionar.

---

##  Diferencia con el Astable
- **Astable:** no tiene estado estable, oscila continuamente y produce una señal periódica (onda cuadrada).  
- **Monoestable:** necesita un disparo externo y solo genera un pulso.  

-mais simple:
- El **monoestable** es como un cronómetro que se activa solo cuando lo disparas.  
- El **astable** es como un metrónomo que nunca se detiene.  

---

##  Atari Punk Console
- También **armamos el circuito Atari Punk Console**, basado en el temporizador 556.  
- Lo hicimos en pareja, y al principio **no resultó bien** porque habíamos conectado mal algunos cables.  
- Tras corregir el error y reemplazar el chip, el circuito funcionó correctamente.  
- Pudimos experimentar sonidos retro controlando el tono con el potenciómetro y la luz con el LDR.  

---

## Forrest Mims y RadioShack
- Forrest Mims fue un divulgador de electrónica en los años 70.  
- Sus manuales, vendidos en **RadioShack**, enseñaban a construir circuitos simples y accesibles.  
- Uno de sus diseños con el 556 fue redescubierto y bautizado como **Atari Punk Console**, por su sonido retro y estilo DIY.  

---
##  Conclusión
En esta clase **realizamos circuitos** con resistencias equivalentes, el 555 en modo monoestable y el Atari Punk Console.  
Aunque hubo errores de conexión y un chip quemado pipipi , logramos corregirlos y experimentar con el funcionamiento real de ambos diseños.




