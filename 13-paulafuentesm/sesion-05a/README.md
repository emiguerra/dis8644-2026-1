# sesion-05a

# **Sintetizadores Modulares**

**vcv-rack**

+ Plataforma de sintetizador modular virtual que simula módulos Eurorack, además de módulos.
+ CHIP CD4039: tiene diferentes nand con diferentes funciones que dependen a cual se conecta relacionado con el sistema de modulos.

## Apuntes

| Modulos | Abreviatura | Descripción |
| :--- | :--- | :--- |
| VC | Controlado por Voltaje | Circuitos electrónicos cuyo comportamiento (como ganancia, frecuencia o corriente) es ajustado por un voltaje de entrada variable o señales electricas.
| VCO | Oscilador controlado por voltaje | Circuito electrónico que genera una señal periódica cuya frecuencia de oscilación según el voltaje de entrada.
| LFO | Oscilador de Baja Frecuencia | Frecuencia muy baja ( sonido bajo ), utilizadas para modular automáticamente parámetros como el tono, volumen o filtro.

![moduladores-1](https://github.com/paulafuentesm/dis8644-2026-1/blob/cef8875e95f5c528a399e51fd273babaf368a526/13-paulafuentesm/sesion-05a/imagenes/moduladores-1.jpg)
Imagen: sistema de ondas en VCO y vistaso a Algebra Boole.

**Algebra Boole.** : valores binarios (0 y 1)
+ 1 : ( verdad ) se utiliza si es qu ela enegia puede pasar por el circuito.
+ 0 : ( falso ) no hay un camino y no llega energia.

| Algebra Boole | Descripción |
| :--- | :--- |
| OR  | Una de las entradas es verdadera ( 1 ) o tiene 2 o x caminos independientes. ( mostrado ejemplo en: imagen arriba "tabla de verdad" )
| NOT | Invierte el valor de entrada: 0 pasa a ser 1 , y 1 pasa a ser 0. ( ej imagen abajo " 1 camino" )
| AND | verdadero (1) solo si todas sus entradas son verdaderas. ( ej imagen abajo )

![amoduladores-2](https://github.com/paulafuentesm/dis8644-2026-1/blob/cef8875e95f5c528a399e51fd273babaf368a526/13-paulafuentesm/sesion-05a/imagenes/amoduladores-2.jpg)

------

## **Ejercicio en clases:**

**Ejercicio 01:**

![miprimer4093](https://github.com/paulafuentesm/dis8644-2026-1/blob/cef8875e95f5c528a399e51fd273babaf368a526/13-paulafuentesm/sesion-05a/imagenes/ejercicio/miprimer4093.png)
Autor: Misa

**Ejecuciòn**

![chip4093-1](https://github.com/paulafuentesm/dis8644-2026-1/blob/cef8875e95f5c528a399e51fd273babaf368a526/13-paulafuentesm/sesion-05a/imagenes/ejercicio/chip4093-1.jpg)

Observaciones: 
Sonido electrónica donde un LED pulsa al ritmo de una señal y un parlante reproduce un pitido cuyo tono cambia con el potenciómetro.

+ La luz empieza  parpadear según las ondas que recibe junto con el pitido que se meite del parlante
  
+ CD4093: genera pulsos eléctricos repetitivos (onda cuadrada) y eso hace parpadear la luz del LED.

**Ejercicio 02:**
Se le agrega otro Nand utilizando patitas 11- 12-13 ( màs otro Potenciometro)

![misegundo4093](https://github.com/paulafuentesm/dis8644-2026-1/blob/cef8875e95f5c528a399e51fd273babaf368a526/13-paulafuentesm/sesion-05a/imagenes/ejercicio/misegundo4093.png)
Autor: Misa

*Ejecuciòn*

![chip4093-2](https://github.com/paulafuentesm/dis8644-2026-1/blob/cef8875e95f5c528a399e51fd273babaf368a526/13-paulafuentesm/sesion-05a/imagenes/ejercicio/chip4093-2.jpg)

Observaciones: 
Los potenciómetros permite modificar de manera independiente tanto la frecuencia del tono principal como la velocidad de modulación

+ las ondas de sonido puente ir en diferentes modulaciones por q+lo que crean sonidos diferentes y se pueden modificar por separado, creando 2 melodías diferentes 
+ Los led se ocupan para ver si el circuito está funcionando 




