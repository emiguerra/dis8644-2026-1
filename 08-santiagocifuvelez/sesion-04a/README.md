# sesion-04a  
31 de marzo del 2026

Hola profe(s) Aron, Misa y Emi. Espero estén teniendo un bonito día, y tengan una sonrisa hoy en sus rostros.

El día de hoy vamos a ver en estas letras lo siguiente:

1. la notación científica usada para describir resistencias y condensadores.
2. profundización del circuitos astable y monostable con el chip 555, interconectando ambos en cascada.
3. El encargo 04, respectivo a esta unidad.

## 1. La notación científica usada para describir resistencias y condensadores.  
La notación científica se usa porque los valores en electrónica pueden ser muy grandes o muy pequeños, y escribirlos completos sería poco práctico.
Se basa en potencias de 10.

Para eso debemos entender que:  
![notación cientifica](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-04a/imagenes/img1.png)

**Resistencias** 
Las resistencias suelen tener valores grandes, así que usan exponentes positivos.  
Prefijos más usados:  
Prefijo	Símbolo	Equivalencia  
kilo	kΩ

mega	MΩ  	

**Condensadores (F)**  
Los condensadores trabajan con valores muy pequeños, así que usan exponentes negativos.  
Prefijos más usados:  
Prefijo	Símbolo	Equivalencia  
micro	µF	10−610^{-6}10−6  
nano	nF	10−910^{-9}10−9  
pico	pF	10−1210^{-12}10−12  

(10^3, 10^6) - Resistencia (números grandes)  
(10^{-6}, 10^{-9}) - Condensador (números pequeños)  
µ, n, p	- Siempre condensadores  
k, M	- Siempre resistencias  


## 2. Profundización del circuitos astable y monostable con el chip 555, interconectando ambos en cascada.
![cascada](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-04a/imagenes/imgastableymonostable.jpg)

<a href="https://drive.google.com/file/d/1s-TS1Z9ULEbuu8Uzo-hDDFqpuyOHnLCE/view?usp=drive_link">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRPUdY8tZ3k6NU9tu5oLw3sdZMID-MxhRJpRQ&s" width="200">
</a>

## 3. El encargo 04, respectivo a esta unidad.

El dispositivo que voy a desarmar para hacer mi respectivo análisis, es un control remoto de tv antiguo, perteneciente a VTR.com

1.	Así se ve en su estado natural, sin intervención alguna.  
![fto1](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-04a/imagenes/control.jpeg)

2.	Ahora vamos a ver, su esqueleto.
   
![fto2](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-04a/imagenes/control2.jpeg)

![fto3](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-04a/imagenes/control3.jpeg)

3.	La parte que ahora nos interesa más, es la placa verde y la placa de acetato transparente, la cual estoy muy seguro que tiene alguna función por sus pedacitos de metal que existe en ella.

![fto4](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-04a/imagenes/control4.jpeg)

5.	Ahora que ya seleccionamos esas dos partes del cuerpo del control remoto, vamos a ver los elementos que encontramos en la placa, quizá algunos conocidos, otros no, como:  

Parte trasera/marrón:  
Un condensador de 100uf (10v), una luz LED azul, un globito naranja llamado: TT4.OM, y las marcas donde se ponen las baterías que le dan energía al circuito.

Parte delantera/verde:  
