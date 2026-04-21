# sesion-05b

Apuntes de la clase del viernes 10 de Abril, 2026.

El día de hoy la clase fue un poco más cortita, comenzamos a las 11 AM.

- Trabajamos en base a un nuevo chip: el 4017

Es un circuito integrado CMOS de 16 pines que actúa como contador Johnson de 10 décadas, dicho más simple puede contar del 0 al 9 de forma secuencial.

+ Recibe pulsos: Acepta una señal de reloj (clock) en su pin 14.
+ Activa salidas en orden: Cada vez que recibe un pulso, apaga la salida actual y enciende la siguiente.Si la salida 0 está encendida y llega un pulso, se apaga la 0 y se enciende la 1.
+ Reinicio: Al llegar a la última salida (la 9), el siguiente pulso hace que el conteo regrese automáticamente a la salida 0.

Debíamos realizar una conexión con un timer.
Ya hemos visto 2 hasta el momento.
+ 555
+ 4097

Intenté con el 4097 porque a comparación del 555 lo hemos visto solo una vez si es que mal no recuerdo.

Me di cuenta que me costó y me demoré más en realizar este circuito. Porque además elegí el que utilizaba más compuertas. Por lógica tendría más margen de error y exactamente, no funcionó.

Probé con otro esquemático más simple.
Funcionó a medias, logré el timer, más no me funcionó al momento de conectarlo con el 4017.
Parecía que prendía una pura vez apenas le conectaba la batería, duraba unos segundos y se apagaba. Por tiempo no logramos hacer la conexión con ninguno en mi grupo.

---

El fin de semana después del trabajo estuve intentando probar nuevamente el circuito para ver si funcionaba. 
Compré un cargador de batería porque me hacía más sentido que esta estaba descargada y por eso me fallaba el circuito. Supuse, cargué la batería y me puse a probar.

Esta vez hice el timer con el 555, me fui por la vieja confiable.
Hice la conexión con el 4017.

Sucedió lo mismo que la vez anterior. Prendía unos segundos, y se apagaba, aunque le moviera el potenciómetro, le ajustara los cables, revisé si es que era problema de los LEDS y no era nada de eso!!

Quedé un poco frustrada porque tampoco pude identificar si es que era algún problema con el chip (no tenía repuesto). Así que espero resolverlo en la proxima sesión, preguntar, revisar en conjunto y ver qué es en lo que me pude haber equivocado :)
