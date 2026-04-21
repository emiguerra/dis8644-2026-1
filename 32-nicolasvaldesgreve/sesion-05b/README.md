# sesion-05b

# Apuntes 10/04

Conceptos nuevos que aprendí hoy:

+ _UX_: User Experience, entender al usuario
+ _Campo de sentido_: Nosotros decimos qué es "aesthetic"

Al hacer un producto, hay que pensar en el usuario, por lo tanto en nuestro proyecto tenemos que procurar que el usuario entienda (no tirarle un 555 por la cabeza, sino poner cables). Para que el usuario entienda, vamos a tener que hacer un manual.

Para el gran proyecto 1, la carcasa de la entrega será de cartón para faltarle un poco el respeto y romper con lo aesthetic.

---

### Relojes (ondas cuadradas)

+ 555 astable más o menos lento
+ 4093 con 10 uf y un potenciador (no olvidar pin 7 y 14 como la última vez por favor)

Los relojes son para gatillar los secuenciadores!!

### CD4017 !!

Pins del chip 4017 y qué hacen:

+ Pata 8 - GND
+ Pata 16 - V+
+ Pata 1,- Salidas
+ Pata 14 - CLK
+ Pata 13 - CI (Clock Inhibit)
+ La salida del 555 va unida al pin 14 del 4017

Luego de que nos explicaran un poco el chip 4017, Misa nos envió un esquemático para que podamos seguirlo de manera independiente. Cuando lo vi, decidí hacer primero la parte del 4017 ya que asumí que el 555 no se me haría atadoso ya que lo hemos hecho bastantes veces y decidí dejar lo más liviano al final.

![Esquemático chip 4017 por misa](./imagenes/esquematico-4017-misa.png)

Cuando terminé de hacer la parte del secuenciador (4017), me acerqué a mi grupo para que podamos probar si funcionaba, por lo que mis compañeras conectaron su 555 al 4017, y cuando le dimos energía no funcionó. Como no entendimos qué había pasado, le preguntamos a Aarón y nos preguntó si revisamos primero que funcione el 555 de manera independiente, y como no lo hicimos decidimos probar y en efecto no estaba funcionando. Como no sabíamos cuál era el problema, hicimos la parte del 555 desde cero para poder ir de manera ordenada viendo si estaba todo bien, y cuando lo conectamos con el 4017 finalmente funcionó!! se veía así:

![Circuito funcionando pero no sabemos si de la manera correcta](./imagenes/circuito-casi-bueno.gif)

Luego de celebrar que nos había funcionado, me puse a ver a otros compañeros y me di cuenta de que la secuencia de luces de ellos era distinta a la de nosotros, ya que como se puede ver en el gif a nosotros se nos hacían solo dos parpadeos distintos pero los LEDs funcionaban como parejas, en cambio en el de nuestros compañeros cada LED era independiente. Como no teníamos lo mismo que nuestros compañeros, me confundí un poco pero de igual manera lo tomé como una victoria!! 
