# grupo-08

## integrantes

- Antonella Aguilar / antokiaraa
- Catalina Oyanedel / catalinaoyanedel-01
- Yaira Ruiz / yairaruiz

## descripción del sintetizador realizado

Nuestro proyecto se basa en la construcción de un sintetizador modular, compuesto por los chips 555, 4017, 4093 y LM386. Para lograr que nuestro sintetizador pueda funcionar, se requiere seguir el paso a paso de nuestros chips: Primero, el chip 555 genera el pulso base (clock), que luego este pasa al 4017 el cual distribuye la señal en 4 distintos pasos, funcionando como secuenciador. A partir de ahí la señal se conecta al 4093 donde se genera el sonido mediante oscilación y finalmente el LM386 amplifica la señal para que pueda escucharse a través del parlante. En este sentido el sintetizador funciona de forma modular donde cada parte del circuito se puede entender por separado, pero en realidad solo tiene sentido cuando todo está conectado. Cada módulo cumple una función distinta y la conexión entre ellos es lo que finalmente permite generar sonido.

Mantuvimos el circuito con el esquemático que nos entregaron, realizando modificaciones mínimas que no cambiaron el sonido del sintetizador, ya que al probar con distintos condensadores, por ejemplo, no nos terminaban de convencer los cambios de estos sonidos. Partiendo por lo básico, el proyecto cuenta con distintas perillas (potenciómetros) que permiten modificar el sonido en tiempo real: la del 555 controla la frecuencia del pulso base, las cuatro perillas del 4093 generan variaciones en el tono y la textura del sonido, y la del LM386 regula el volumen del parlante. Esto hace que el sonido no sea fijo, sino que es variable según cómo se manipule y se pueden ir experimentando diferentes combinaciones.

En base a que no profundizamos en los cambios de sonidos, quisimos diseñar de mejor manera la experiencia al manipularlo, es por eso que le dimos el título de “Naturalezas Interconectadas”. Este título simboliza que somos distintos tipos de naturalezas interactuando la una con la otra, en nuestro caso, personas, interactuando con este circuito a través del sonido y las luces. Así, quisimos integrar dentro del diseño de la carcasa las luces como parte del sintetizador, haciendo que al interactuar no solo se le diera protagonismo al sonido, sino también a las reacciones lumínicas.

imagen del sintetizador en su contexto

audio o video del sintetizador en acción

## proceso y resultados del reloj y secuenciador

con chips 555 y 4017

incluir texto e imágenes sobre cableado, pruebas, resultados obtenidos.

## proceso y resultados de osciladores y amplificador

con chips 4093 y 386

incluir texto e imágenes sobre cableado, pruebas, resultados obtenidos.

## modificaciones realizadas a los circuitos originales

Durante el desarrollo del proyecto tuvimos que realizar algunas modificaciones tanto por problemas de funcionamiento como por la integración del sintetizador en la carcasa. Al tener 4 LEDs funcionando el circuito no lograba soportarlo, lo que generaba interferencias en la señal y hacía que no se emitiera sonido, Misa nos comentó que para evitar esto debíamos quitar alguno de los LEDs, o en nuestro caso lo que hicimos fue quitar solamente la resistencia de este para que empezara a sonar, por lo que el circuito final tiene los 4 LEDs pero solo 3 de ellos se encienden, también notamos que según el LED que desactivaramos, el sonido cambiaba, en el resultado final sería el Step 2 el que está desactivado.

También probamos modificar los valores de los condensadores para explorar cómo afectaban el sonido. En el caso del 4093, cambiamos los condensadores de 1uF por otros de 10uF y 100uF en los potenciómetros, pero el resultado no nos convenció, el sonido se volvía más grave y menos variable al mover las perillas. Por esto, decidimos mantener los condensadores de 1uF, ya que permitían un mayor rango de variación y un comportamiento más interesante del sonido.

Otra modificación fue la conexión de 2 de los potenciómetros, el del 555 y el del LM386, que para que pudiesen quedar cómodamente funcionales en la carcasa los sacamos de la protoboard mediante cables dupont M-H (macho-hembra).

## carcasas de cartón

textos, imágenes

incluir origen de materiales, decisiones de posiciones de los componentes, decisiones estéticas, pruebas, resultados obtenidos.

## interconexión entre módulos

textos, imágenes, diagramas de interconexión

## resultados finales

Resultado final de nuestro proyecto “Naturalezas Interconectadas”  

Se logró un montaje final funcional, donde organizamos el circuito dentro de la carcasa y los componentes quedaron correctamente distribuidos y las perillas accesibles, agregando pequeñas piezas en resina impresas en 3D para 4 de los potenciómetros que corresponden al chip 4093 permitiendo su manipulación sin interferir en el funcionamiento del sistema. El circuito responde a las variaciones de los potenciómetros generando cambios en la frecuencia, modulación y amplitud de la señal. 

*fotos y videos*

## aprendizajes y errores

las mejores lecciones aprendidas y los errores más comunes y cómo los resolvieron

## conclusiones

sobre modularidad, materialidad, trabajo en equipo, trabajo electrónico, trabajo maquinal.

## bibliografía
