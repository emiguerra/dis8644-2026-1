# sesion-06a

## Schmitt Trigger

+ Histeresis: tiene memeoria ( 2 umbrales)
+ Señales analógicas ruidosas o lentas en ondas cuadradas digitales limpias

![strigger](https://github.com/paulafuentesm/dis8644-2026-1/blob/d6a6e44617e317b651eb1897a4edefcffe1bc1a2/13-paulafuentesm/sesion-06a/imagenes/strigger.jpg)

**Simbolo:**

![trigger-simbo](https://github.com/paulafuentesm/dis8644-2026-1/blob/d6a6e44617e317b651eb1897a4edefcffe1bc1a2/13-paulafuentesm/sesion-06a/imagenes/trigger-simbo.jpg)

### Chip 4093
+ Tiene 4 compuertas NAND
+ Solo oscila sì pin 2=V++

![4093chip](https://github.com/paulafuentesm/dis8644-2026-1/blob/04b7354c96847a86b798138b7ccf12991414997b/13-paulafuentesm/sesion-06a/imagenes/4093chip.png)

------

### Ejercicio:

**4 pasos**
+ se ocuparon chip 555 - 4017 - 4093
+ se agraga una salida de parlaten alfinal

![4pasos](https://github.com/paulafuentesm/dis8644-2026-1/blob/2dc2d52d0b8f82fddb086983cd40040dbd95627a/13-paulafuentesm/sesion-06a/imagenes/ejercicio/4pasos.png)
Imagen: extraida del repositorio de Misaaaa.

**Metodologia grupal:** Cada integrante comenzó desarrollando un módulo distinto. Una vez finalizados, los íbamos intercambiando entre los tres para revisarlos y detectar posibles errores o conexiones incorrectas. A mí me correspondió trabajar con el 4093 (mencionado para contexto futuro). Además, verificábamos el funcionamiento según lo aprendido en clases: utilizando LEDs como indicadores y comprobando si cada botón generaba sonido.

![555-4017chips](https://github.com/paulafuentesm/dis8644-2026-1/blob/2ce3574a4457e589278e9ab6944be07ccd533f46/13-paulafuentesm/sesion-06a/imagenes/ejercicio/555-4017chips.jpg)

+ Comprobamos que los dos primeros chips funcionaran correctamente, tanto por separado como en conjunto, verificando que no presentaran errores. Para ello, utilizamos un LED como indicador y nos aseguramos de que todas las conexiones a tierra (GND) estuvieran correctamente realizadas.

**Problema**

+ 555 - 4017= estaban funcionando (se comprobaron muchas veces)
+ 4093 - Salida= no estaban funcionado, sonido sucio he inestable

+ No hubo un registro del sistema de botones del sintetizador (4093), ya que, al no funcionar como debía, se generó un punto de frustración colectiva que impidió documentar el módulo 3. Personalmente, llegué al punto de explotar ( ella era un chip ) y no pude controlar mi frustración hasta el final de la clase. Desarmamos los circuitos alrededor de tres veces, pero aun así no funcionaban, generaba un ruido sucio y no una melodia o pulsos como se supone que debia sonar con el modulo 4. Se llamó a los profesores, pero no se logró identificar cuál podía ser el problema.

**Después**

+ El profesor dio un discurso sobre la frustración y expresó que estaba contento con los avances de cada uno, destacando que no sería fácil, ya que es una materia nueva para todos y no se aprende de un día para otro ( me lo tome personal (broma) ). Se concluyó que existía un problema entre las luces LED, los botones y el módulo 4, aunque en ese momento no se logró identificar con claridad cuál era la causa. Finalmente, Misa dijo que lo revisaría en su casa y que en la próxima clase nos daría la respuesta junto con el nuevo módulo.

**Conclusión**

+ No todo sale a la primera y nadie me está apurando.
