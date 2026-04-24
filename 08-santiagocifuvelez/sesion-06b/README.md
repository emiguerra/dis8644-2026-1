# sesion-06b

17 de abril del 2026 

¡Hola!, no sé si ya están cansadxs de que siempre los salude…, pero lxs voy a cansar hasta que se termine el semestre. (jiji).  
Espero que se encuentren muy bien equipo docente de Taller de maquinas electrónicas. 

Hoy vamos a ver lo siguiente:

1.	Tipos de fuentes de energía para alimentar la proto.
2.	Modificaciones realizadas por el profesor Misa para un mejor funcionamiento del instrumento. 
3.	Trabajo en solemne 01 
4.	Trabajo de solemne 01 (Precarias), en el MUT.
   
Comencemos c:

## 1.	Tipos de fuentes de energía para alimentar la proto.

**9V:** *La cual usamos regularmente, obtenida de una batería recargable.*  
**12V:** *Baterías de autos y paneles solares.*  
**5V:** *Un cable “USB-A” que se pude conectar a una cabeza de energía y transitarla hasta la proto.*  

## 2.	Modificaciones realizadas por el profesor Misa para un mejor funcionamiento del instrumento. 

Lo que se realizó aquí fue:  
Agregar condensadores no polarizados (lentejitas), para estabilizar circuito. También, quitamos luces LED y resistencias del chip “4017”, ya que la energía llegaba cansada al chip “4093” al pasar por estas, y esto hacía que sonara distorsionado y cansado. 

Esquemático de realización de que se necesitaba estabilizar el circuito:  
![condensadores agregados](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/esquema-modificado.jpeg)

Esquemático formalizado:  
![Esquemático corregido por el profe misa](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/esquematico4pasosnuevo.png)

## 3.	Trabajo en solemne 01 

En clase, estuvimos revisando que sucedía con el circuito, ya que la bocina sonaba muy distorsionada, y teníamos un problema en el chip 4093 y 386. Estuvimos toda la clase intentando solucionar ese problema, hasta que el equipo de la reina Vania, nos ayudó a organizar mejor los componentes en la protoboard, y claro: Nos dimos cuenta de que no estaban mal, si no que por el orden que tenían en la protoboard, había resistencias tocándose (las patitas metálicas), y había condensadores muy altos para el ejercicio, los cuales habíamos agregado porque queríamos al comienzo, diversos tonos en el sonido.

También en el 386, la organización nos estaba afectando. Así que lección aprendida. Ser más dinámicos y precavidos con la organización de las protoboards.

## 4.	Trabajo de solemne 01 (Precarias), en el MUT.

Antes de partir al MUT (re hermoso, por cierto), estuve en casa intentando arreglar el circuito, y gracias al profesor Aaron, lo logré…, pues todo funcionaba, pero el sonido emitido por la energía se seguía escuchando re cansado y muy sucio, así que el profesor Arón, con una calculadora de oscilaciones, me recomendó usar condensadores de menos de 1uf.   
Así que use condensadores de 0.47uf. 

Period.

![yo en casa antes de pedir ayuda](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/yo-en-casa.jpeg)  

Video de mi pidiendo ayuda:  
https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/video-pidiendo-ayuda.mp4   

![SOS respondido por el profe aaron](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/ayuda-profe-aaron.jpeg)

Luego, al MUT para planear, mostrar y enseñar a mi grupo lo realizado en casa: 

![yo en el metro con precarias en la mano](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/subway-mut.jpeg)
![proceso de trabajo en el cc](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/working-in-the-mut.jpeg)
![Cuando terminamos, y todo estaba bien](https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/precarias-funciono.jpeg)

**She's alive:**

Video de precarias viva:  
https://github.com/santiagocifuvelez/dis8644-2026-1/blob/main/08-santiagocifuvelez/sesion-06b/imagenes/precarias-con-vida.mp4
