# sesion-05b
La clase empezó a las 11 y aun asi me quede dormido y casi llego muy tarde pero solo me atrase un poco por lo menos
## apuntes viernes 10 de abril

### referencias de la clase
* Push turn move = libro de referencia aclamado sobre el diseño de interfaces en instrumentos musicales electrónicos.
* Pedalboard = Permite cambiar efectos de la guitarra sin necesidad de tocar la guitarra o algún botón cerca de este, asi se puede tocar y cambiar los efectos en tiempo real.
* David bryrne = Lo caracteriza que nadie está sentado ni enfrente de uno ya que todos los de la banda importan lo mismo, por lo tanto, también deben tener las mismas prendas, además de tener un estilo experimental y un acercamiento a la electrónica. de hecho tiene una versión de "The Model" de Kraftwerk.
* St. Vincent = Usa una guitarra personalizada para las personas de género femenino ya que se adapta usualmente a su cuerpo, y también las distribuye.
* Banda Marinero = Dúo chileno que usa guitarras de St. Vincent.

### significado o funcionamiento de cosas
**Secuenciador** = reproduce eventos musicales en orden, controlando sintetizadores, cajas de ritmos o sampler. Actúa como un cerebro. La diferencia con un sintetizador es que no genera sonido por sí mismo, sino que envía señales a otros equipos para que ellos toquen.
* Se puede hacer un reloj con un 555 y un 4093 (ambos chips)
* Funciona de 0 a 9 y reproduce diferentes notas en base a eso, es un contador de década.
**4017** = de Q0 a Q3 toca notas y vuelve a 0 si conectamos el final con 14 rst.
* Cuenta también con 16 patitas, a diferencia del 555, que solo tiene 8.

---

### experimentacion
* Hicimos un experimento junto a mi compañero Angel Sabogal, en donde unimos un 555 y un 4093:
![Prueba](./imagenes/prueba.gif)

Gracias al 555, es posible hacer que los LEDs  conectados al 4093 empiecen a prenderse en secuencia; al aumentar el potenciómetro la secuencia será más rápida.

