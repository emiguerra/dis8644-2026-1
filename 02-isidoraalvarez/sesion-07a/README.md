# sesion-07a

manual nasa para aprender a soldar
internet archive
claudia gonzalez godoy 
kicad:software 
kicad source code
10.0.1 descargar esta version 

jlcpcb:empresa china 
se le manda el diseño en archivo cad 
realible FR4 pcbs 
pcb lampda:smt/ through-hole 

media lab mx
Si se pone capacitores en Paralelo (Uno al lado del otro) se suma tienes más almacenamiento.
Voltaje: Se mantiene igual al del capacitor más débil. esto se hace para aumentar la potencia o el filtrado, y hace que tenga energia estable.

Y si se coloca los capacitores en Serie (Uno tras otro) se reduce el total es menor que el capacitor más chico. Soportan más tensión sin quemarse. y se suele usar para trabajar con voltajes altos.
tambien se usa para acople 
Como la capacidad total baja, el capacitor actúa como un filtro "pasa-altos". Bloquea los graves y solo deja pasar los agudos.

**proceso en clase**
transistores:tiene polaridad cara plana a uno
izq-------.colector
derecha. imiter o emisor
al medio base controla la corriente 
**Extras**
CD 555 intentanmos cambiarle un capacitador de 10uf a 100 uf
*No funciono con el de 100 uf*
usar capacitadores de 10 uf si o si para el CD 555

**Modificaciones**
Capacitor due cambiado en el 4093 para una mayor frecuencia de 10 a 1 

CD 555 intentanmos cambiarle un capacitador de 10uf a 100 uf
*No funciono con el de 100 uf*
usar capacitadores de 10 uf si o si para el CD 555

intentamos hacer la prueba de ponerle leds al chip 4017 y no resulto pero prabaremos una vez mas, le pedimos auyada a otro grupo y esperamos que esta vez funciones 
[Imagen]
todo el circuito funcionaba bien no se tuvo que corregir mucho 
En el CD 4091 fuimos probando ponerle distintos capacitadores de 10 uf y de 100uf en paralelo y empezo a sonar muy bien.( fue la mejor decicion ir poniendole capacitadores en paralelo  




**cosas por hacer**

Hacaer informe 

Afinacion del sonido

corte laser de las cajas 

impresion 3d 

**Trabajo en la semana**

durante la semana el circuito nos funciono muy bien solo faltaba definir la afinacion.
Cortamos en laser las ultimas modificaciones que le hicimos a la carcasa
seguimos una logica de colores
por ej: 4093-recistencias-cafe-pin
            -capacitor-amarillo-pin

identificamos posibles variables al momento que empezo a fallar algunas partes del circuito 
*entre estas variables estuvo el problema de las conexiones y en el chip 386 un condesador fue a negativo por error
teniamos una pinza conectada a un capacitor,funcionaba a ratos

**conectamos**
en el 555teniamos un condesador de 1uf para hacer ¨resureccion¨  mas rapido, pero a lo mejor la capacidad del 555 era demasiado rapida 

**Etapa final**

Al momento de intentar conectar todos los circuitos para ponerlos en sus resprectivas carcasas y ninguno de los chips funciono 

-Cambiamos el 555 y ahora se prende el led pero no oscila por lo tanto cambiamos el condesador de de 100 uf por  uno de 1 uf 

-por segunda vez se cambia el 555 y se termina por cambiar el potenciometro.

-se cambio otras 3 veces mas el chip 

-habia un potenciometro mal sodado 

**2da falla**

El parlante no sonaba

555 si funcionaba, oscila,parpadea
vamos probando conexiones con el 4017, empezamos a brobar con leds y solo dos parpadeaban cambiamos como dos veces el chip, para descubrir que al final el clock estaba mal conectado 
en general habian malas conexiones.
problemas de soldadura del potenciometro logaritmico

*se uso esta logica para variar el sonido*
(la frecuencia especifica)

-cuando se dispone los capafitores en serie se restan 

- en paralelo se suman

- entre mayor valor de los capacitadores-mayor es la frecuencia


**FINAL**


LOGRAMOS HACER QUE SUENE

empezamos a jugar con los capacitadores para ver bien la afinacion del sonido
