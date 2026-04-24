# grupo-01

## integrantes

- Bruno Ferrari // chknngttts
- Martina Echavarría // martinaechavarria-stack
- Lucas Ortiz // ryukivol

## descripción del sintetizador realizado

Al hablar como grupo sobre lo que queríamos hacer, pensamos en distintos synths y nos interesó mucho hacer uno que lograra producír sonidos más parecidos al noise (Esto porque escuchamos a algunos artistas del genero noise/drone). Al buscar "Pink/Brown/Blue/Drone noise generator" en internet, encontramos uno en un forum de electronica y circuitos llamado "https://electro-music.com". El circuito utilizaba componentes que ya aprendímos en clase pero permitía hacer nuevos sonidos.

El "NANDulator - PHOBoS" utiliza un 4093* (4 Schmitt Triggers) para generar las oscilaciones. Dentro del esquemático en la pagina no muestran como amplificar la señal para que se pueda escuchar, por lo que decidimos añadir un LM386, conectando el pin 4 del 4093 al pin 3 del LM386. Eso si al utilizar el synth, sentimos que faltaba algo para poder controlar el volumen además de tener un filtro, por lo que añadimos un este circuito de "https://generalguitargadgets.com" entre la salida del 4093 y el AMP (Pin 4 del 4093 a la barra del filtro donde se encuentra el R6 y C6). Consiste en 2 filtros R/C y un linear pot (todo conectado a un potenciómetro) que permite controlar el Dry/Wet del filtro, actuando como un EQ modular. 

*4093
  - El creador del NANDulator actualizó en su forum que distintos 4093 creaban resultados variados. Dependiendo de la empresa del chip, el circuito podía o no funcionar a corde a lo que tenia pensado el creador. Uno de los IC's que no funcionaba supuestamente es el CD4093 de Texas Instruments, que es el que utilizamos para el synth. De igual manera estamos contentos con el resultado, nos interesaría averiguar las variabilidades en sonido intercambiando el chip con otros de distintas empresas.

![Esquemático Original del NANDulator](./imagenes/nandulator.png)
- Esquemático Original del NANDulator

![Esquemático Original del Big Muff](./imagenes/big-muff.png)
- Esquemático Original del Big Muff

![Esquemático final del proyecto](./imagenes/brumarcas-ulator-esquematico.jpg)
- Esquemático final del proyecto

https://github.com/user-attachments/assets/e0853da8-d528-4f0e-9732-b4b83ad4852e

https://github.com/user-attachments/assets/4a88d2e4-f8b4-4142-862d-35357690364e


https://github.com/user-attachments/assets/fe5147e6-22c0-429e-88b1-f8da4cb4dce4


![Esquemático Original del NANDulator](./imagenes/nandulatorplanosoriginales.gif)



## Componentes

En este proyecto utilizamos diferentes componentes cada uno para funciones especificas los cuales son:
- Resistencias: Se encargan de limitar el flujo de corriente eléctrica y establecer niveles de voltaje específicos dentro del circuito, las resistencias son fundamentales para proteger otros componentes más sensibles como los leds.
- Diodos: Actúan como ¨válvulas¨ que permiten el paso de la corriente en una sola dirección. Se utilizan generalmente para proteger el circuito contra inversiones de polaridad o para rectificar señales.
- Condensadores: Se encargan de almacenar energia temporalmente. 
- Potenciómetros: Son resistencias variables que permiten ajustar manualmente el nivel de resistencia. Se utilizan para controlar diferentes parámetros como el volumen del audio o la intensidad de la señal.
- parlante: Es el ¨traductor¨ de salida que convierte las señales eléctricas amplificadas en ondas sonoras

Ademas diferentes chips, siendo estos:
- LMD386: Es un amplificador de potencia de audio de bajo voltaje. Su función principal es tomar una señal de audio débil y aumentarle la potencia lo suficiente para que pueda ser reproducida por el parlante con claridad.
  
- CD4093BE: Es un circuito integrado que contiene cuatro puertas NAND Schmitt Trigger, se suele utilizar para generar oscilacione, crear pulsos de reloj o limpiar señales con ruido gracias a su histéresis.

¿Que Son las compuertas NAND Schmitt Trigger y la histéresis?

- Las compuertas NAND son puertas lógicas que entrega una señal 0 solo cuando todas sus entradas están en 1, Si alguna entrada es 0, la salida será de 1. por otro lado el Schmitt Trigger es un diseño de circuito interno que le da "decisión" a la compuerta. En vez de tener un solo punto de cambio, tiene dos umbrales de voltaje distintos.

- La histéresis es la diferencia entre los dos umbrales del Schmitt Trigger, genra una sona de memoria de los V que se necesitan para apagar y encender un circuito, entregando una señal limpia a posibles interferencias

   ### ¿Que hacen especifcamente en nuestro sintetizador?

- CD4093BE:  Este chip es nuectro oscilador que fabrica el sonido utilizando ondas cuadradas, es el que genera el "ruido" base del sintetizador que después mediante los potenciómetros modificando.
- LM386: Como el sonido que sale del primer chip es muy débil, usamos este chip amplificador para darle potencia. Su función es amplificar la señal lo suficiente para que el parlante la pueda reproducir.
- Resistencias: Las usamos para limitar el paso de la corriente y proteger los componentes, a su vez trabajan junto con los condensadores para definir los rangos de frecuencia del sonido.
- Potenciómetros: Son las perillas que nos permiten interactuar con el circuito. Generan la instancia de interacción usuario-circuito para generar los diferentes sonidos del sintetizador.
- Diodos: Los usamos para que la corriente fluya en un solo sentido y para generar el efecto de "clipping" o recorte. Esto le da una distorsión armónica al sonido para que no sea una onda tan limpia.
- Condensadores: Funcionan para filtrar el ruido y para acoplar la señal de audio entre una etapa y otra, bloqueando la corriente continua que podría quemar el parlante.
- Parlante: Es el ¨traductor¨ de salida este toma la señal eléctrica que ya fue creada y amplificada para convertirla en ondas sonoras que podemos escuchar.
- Batería de 9V: Es la fuente de energía de todo el sistema.

## Proceso y resultados de 4Steps synth

4steps synth

+ Nuestro desarrollo: 

Desde el día martes 14 de abril, sesión 6a, desarrollamos el circuito en grupo durante las clases. Reiteradas veces rehicimos y analizamos el circuito pero no logró sonar del modo que debía, este no producía ningún sonido.

En el primer intento la secuencia de luces leds se terminaba la secuencia de prendido y apagado con un reatraso. Para aclarar el circuito de los leds debían  de ser un apagado y encendido espontaneo, lo cuál no nos resultó en nuestro primer intento de desarrollo en la protoboard. Luego pudimos encontrar nuestro error en la protoboard, lo resolvimos y  funcionó con la secuencia y frecuencia adecuada.

Al momento de conectar el clock generator y el sintetizador notábamos que todo iba con los resultado esperados, las luces led se prendían y llegaba el voltaje por todo el conjunto de circuitos. Pero conectando el parlante y esperando a que se produjera el sonido, no sonaba nada más que un leve "cck" por menos de un segundo.

Reordenamos todos los cables por color, cambiamos los chips usados nes555, 4017 y 4093B e incluso cambiamos componentes básicos como la batería debido a una posibilidad de carga baja resultando en un bajo voltaje no suficiente para funcionar y hacer ruido.

Rehicimos y probamos de todo con el circuito en la protoboard pero nunca nos resultó.


![4017 y 555 funcionando](./imagenes/4017-prendido-cerca.gif)

![Intendo 4stepsynth 1](./imagenes/555-4017-4093-386.jpg)

![Intendo 4stepsynth 2](./imagenes/4093-386.jpg)


## Modificaciones realizadas a los circuitos originales

En cuanto a modificaciónes de los circuitos base, en el Schmitt Trigger del pin 4-5-6 cambiamos el potenciómetro de 500k a 100k. El condensador conectado al pin 12 usamos un condensador de 47nf en vez de 470nf. Todos los diodos los remplazamos por diodos zener. En el filtro, cambiamos la resistencia de 39k por una de 47k y el potenciómetro de 100K a uno de 1M, más que nada por la accesibilidad a materiales en el laboratorio.


## Carcasas de cartón

+ Orden

Dividimos en 3 cajas el synth. 
Una para el circuito con el chip 386 la cuál corresponde a una caja pequeña debido a que tenía menos componentes y estaba desarrollada en una protoboard miniatura, en esta caja también se encuentra el  conector de la batería recargable de 9v. 
Para el circuito con el chip 4093 usamos una caja exageradamente grande, con la intención de que fuera así, además considerando que usamos una protoboard larga debido a su alta cantidad de componentes era la opción más adecuada.
La ultima caja es la más pequeña ya que lleva únicamente el parlante, por lo cual no es necesario mucho espacio.

+ Estética y montaje

Desde un comienzo planeábamos desarrollar el proyecto en unas cajas más grandes de lo necesario.
Desde un principio queríamos que nuestro distintivo fuera que el parlante estuviera colgando, después llegamos a una solución para nuestra propuesta la cual fue colgarlo desde el techo con hilo de pesca.

Para decorar las cajas optamos por un diseño o estética inclinada al brutalismo, ya que armoniza muy bien con el sonido que produce nuestro sintetizador. Para lograr el acabado deseado recubrimos todas las cajas con cinta americana y pegamos unas etiquetas asimétricas a propósito.

+ Alternativas

Otra propuesta para el recubrimiento de las cajas fueron pegar stickers por toda la caja al punto de sobre ponerlos, pero por tema de presupuesto no nos convenía.
También consideramos pegarle hojas de diario o cartulina. Que luego se descartó para usar la cinta americana.


![cajas](./imagenes/modulos-1.jpg)

![cajas](./imagenes/modulos-2.jpg)


## Interconexión entre módulos

Al hablar entre nosotros nos interesó la idea de tener 3 modulos, uno para el 4093 y "Big Muff", uno para el LM386 y uno para el parlante. Desde el principio quizimos tener una caja inecesariamente grande para lo que sea que contenga. Al tener esto en mente nos que damos con este diseño.

![Idea modulos cajas](./imagenes/cajas.png)

Todo estaría conectado con cables dupont. Eso por temas de alcanze entre cajas y por seguridad en la conexión a la protoboard, el modulo con el parlante lo terminamos conectando con cables comunes para lograr la distancia y largo deseado. En cuanto a los colores de cables externos, en el parlante para indicar positivo y negativo usamos rojo y negro respectivamente. Del 4093/Filtro al LM386 usamos duponts in/out blanco/gris y amarillo. El amarillo para marcar el output del filtro, el gris para positivo y blanco para tierra. Estos colores para mantenernos dentro de los colores que eligimos. La trenza en la parte del LM386 se hizo más que nada para decorar y para que por ese lado los cables no estén sueltos.

Decidímos también poner el LM386 sobre la caja del 4093/Filtro principalmente por razones de estetica, pero tambíen por el largo de los cables, que para no arriesgar una mala conexión a la protoboard usamos dupont. En el parlante usamos de cable común a caimán/dupont en la protoboard.

![Modulos montados](./imagenes/modulos-1.jpg)

![Parlante cable caiman](./imagenes/parlante-modular.jpg)


## Resultados finales

Como resultado final tenemos un "brumarcas-ulator", que funciona como generador de ruido inspirado en artistas de drone/noise como "Belong" y "Tim Hecker". Un synth modular con 3 cajas distintivas, una con un IC 4093 y filtro "Big Muff" con 6 potenciómetros para controlar el sonido, otra con un amplificador LM386 que se conecta a la ultima caja que contiene el parlante.

![brumarcas-ulator 1](./imagenes/brumarcas-foto-3.jpg)

![brumarcas-ulator 2](./imagenes/brumarcas-foto-4.jpg)


https://github.com/user-attachments/assets/228fa58b-05e1-4e26-8721-6c8a360c92b5


Estamos muy contentos y orgullosos con el resultado final :)

## Aprendizajes y errores


En el proceso de intentar hacer ambos synths, nos encontramos con varios problemas.

En cuanto al 4stepsynth de misaaaaa, nunca logramos hacerlo funcionar correctamente. Las primeras veces nos encontramos en la misma situación que varios de nuestros compañeros, donde todo parecía estar bien conectado, pero claramente algo pasaba ya que el sonido no se manifestaba en el parlante. El 555 y 4017 no fueron problema para nosotros, ya que si funcionaban los 4 steps y el reset, el problema se encontraba en la conexión entre el 4017 y el LM386. Los profesores nos ayudaron viendo el synth buscando lo que podría ser el problema, Aaron nos sugirió usar cables acorde a los colores para que todo esté más ordenado y sea más facil de leer. Volvimos a hacer el synth con cables acorde a las conexiones pero nuevamente algo hicimos mal.

En la siguiente clase, misaaaaa trajo una versión actualizada del synth con mejoras/alteraciones que podrían ayudar a que nos funcionara. Al intentarlo nuevamente, omitimos las luces en el 4017 y cambiamos las resistencias de conexión al LM386 además de añadir condensadores de desacople en cada conexión a VCC. Nuevamente no encontramos la solución a nuestro problema. De igual manera teníamos pensado desde el principio hacer un synth que nos permita hacer ruido (Pink Noise).

En el "brumarcas-ulator" (NANDulator + Big Muff + alteraciones), inicialmente no tuvimos problemas graves. La primera vez que intentamos armar el **NANDulator**, solo teníamos una protoboard pequeña, por lo que se nos hizo imposible armarlo completamente y confundimos los diodos en el esquemático por LEDs. Al saber esto, compramos una protoboard de 830 puntos y sacamos diodos del LID. Con el synth en una protoboard grande, diodos y un LM386 con parlante conectado al NANDulator, conectamos una batería y efectivamente funcionaba. Algo que inicialmente ignoramos es que en uno de los schmitt trigger conectamos los diodos de manera incorrecta (positivo donde debería ser negativo), esto afectó el potenciómetro haciendo que al usarlo no afectará el sonido de grán manera, si cambiaba levemente la frecuencia, pero solo si el resto de los potenciómetros estaban al mínimo. Esto fue corregido en la segunda versión del "brumarcas-ulator". 

En cuanto al "Big Muff", el único problema que nos encontramos fue usar los valores correctos en las resistencias y potenciómetro. La primera vez que añadimos el filtro al NANDulator el efecto funcionaba más como volumen que como EQ (R/C) ya que el potenciómetro era de 10K (En vez de 100K como aparece en el esquemático) y la resistencia (R1) era de 30k (En vez de 39k) Esto lo arreglamos cambiando el potenciómetro por uno de 1M y la R1 por una de 47K. Al hacer estos cambios el filtro suena más como un muffler.

Hicimos funcionar el filtro, pero no sabíamos qué estaba haciendo para que el sonido se atenuará. Buscamos videos explicando esto y logramos entender un poco más. Los filtros en general suelen estar compuestos con resistencias y condensadores y dependiendo del valor en ambos, ciertas frecuencias se ven afectadas. Esto sirve para bajar/aumentar frecuencias altas/bajas.

Un error final que nos afectó en la segunda versión del "brumarcas-ulator" fue al momento de soldar los potenciómetros con cables. La primera vez soldamos cables comunes (No dupont) a los potenciómetros, esto hacía difícil la conexión a la protoboard y los cables se desconectaban con el más mínimo movimiento. Entonces soldamos finales de cables dupont out a los cables ya soldados en los potenciómetros. Este fue un grave error ya que al conectar todo de vuelta nada sonaba. Sacamos los finales dupont y probamos nuevamente pero seguía sin sonar. Claramente pasó algo al soldar y mover la protoboard que contenía el 4093. 

No logramos identificar el problema exacto en esa versión por lo que hicimos una nueva de cero en una nueva protoboard. Esta segunda versión contiene todos los arreglos mencionados anteriormente y efectivamente suena como se suponía.

Más en general, a lo largo de todo el proceso siempre ocurrían los mismos errores que suelen ser simples como:
- Batería con poca carga
- Componente quemado
- Componente equivocado
- Componentes tocandose cuando no deberían
- Batería mal conectada
- No conectando ambas tierras/positivos en distintas protoboard
- Componentes con polaridad conectados al revez
- Cables mal organizados
- Cables mal conectados
  - Sobretodo en potenciómetros con cables/componentes conectados 1 pin hacia al lado
 

![4093 muerto](./imagenes/4093-pin-muerto.jpg)

![Fallo soldadura potenciometros](./imagenes/caja-potenciometros-fallo.jpg)

![Fallo brumarcas](./imagenes/test-fallo-brumarcas-1-1.jpg)



## Conclusiones

El desarrollo de este proyecto ha sido un proceso de aprendizaje constante, descubrimientos técnicos, manejo de errores y un fuerte componente emocional. No todo nos resultó, a pesar de que el sintetizador de 4-steps inicial no funcionó como esperábamos, ese percance nos permitió redireccionar nuestro trabajo. En lugar de rendirnos ante el fallo técnico, decidimos explorar rutas alternativas, lo que nos llevó a profundizar en el funcionamiento del NANDulator y a experimentar con el género del noise.

Al adaptar este circuito y acoplarlo con un amplificador LM386 y un filtro Big Muff, logramos transformar la frustración inicial en un sentimiento de satisfacción y en un interés por seguir explorando el mundo de la electrónica.

A través del trabajo en equipo, logramos equilibrar el trabajo electrónico de precisión con el trabajo manual, donde la materialidad cobró un rol protagonista ideando las cajas bajo conceptos de modularidad para que fueran el soporte funcional y estético de nuestra propuesta. Entendemos que el sonido es algo subjetivo que puede ser percibido de formas muy distintas dependiendo de la persona quien lo escuche, por eso nuestra pieza busca ser el soporte físico de esa experiencia mas lúdica, ridícula y llamativa, uniendo lo técnico con lo humano.

## Bibliografía 
Referencias

- Electro-music.com. (s. f.). NANDulator - PHOBoS: Single NAND chip noise machine. Forum Index. https://electro-music.com/forum/viewtopic.php?t=64169

- General Guitar Gadgets. (s. f.). Design Your Own Distortion. https://generalguitargadgets.com/how-to-build-it/technical-help/articles/design-distortion/

- Hecker, T. (s. f.). Tim Hecker [Página de Bandcamp]. Bandcamp. https://timhecker.bandcamp.com/

- Lanza, J. (21 de mayo de 2017). NANDulator Noise Machine [Vídeo]. YouTube. https://www.youtube.com/watch?v=8IdCYjax5VI

- Misaaaaaa. (s. f.). 4-Step Square Wave Synth with LM386 [Archivo PDF]. GitHub. https://github.com/misaaaaaa/4stepSQRsynth/blob/main/docs/seq4pasos-lm386.pdf

- Spectrum Spools. (s. f.). October Language [Álbum]. Bandcamp. https://spectrumspools.bandcamp.com/album/october-language

