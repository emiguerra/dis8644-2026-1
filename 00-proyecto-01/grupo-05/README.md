# grupo-05

## Integrantes

- Antonia Améstica   antoniaamc
- Sebastián Guevara  sebastianguevaralarotta
- Luisa Toro         Luisaatoro9

## Descripción del sintetizador realizado 
**OPEN-BEAT KRAFT**

*Un sintetizador secuencial que apuesta por la transparencia técnica (Open), el ritmo constante (Beat) y la honestidad de los materiales reciclables (Kraft).*

### Descripción del Proyecto

Este proyecto consiste en un sintetizador rítmico de 4 notas basado en una arquitectura modular que combina generación de pulsos y modulación de sonido. El corazón del ritmo es un temporizador NE555 configurado para enviar una señal de reloj a un contador decimal CD4017, el cual secuencia las 4 notas de forma sucesiva. Para visualizar el funcionamiento en tiempo real, incluimos una interfaz de LEDs que indican tanto la velocidad del pulso (desde el pin 3 del 555) como la nota activa en la secuencia, permitiendo un control visual del tempo.

La generación del tono se realiza mediante un chip CD4093 (NAND gates), cuyas entradas son activadas por transistores 2N2222 que actúan como interruptores controlados por el secuenciador. Para expandir las posibilidades sonoras, cada nota cuenta con un potenciómetro de B100K y una combinación de capacitores cerámicos ("lentejas") de distintos valores (103, 104 y 471). Esta configuración permite al usuario un rango amplio de frecuencias, pudiendo manipular el sonido desde tonos muy graves hasta agudos profundos, personalizando cada una de las 4 etapas del ciclo.

Finalmente, la señal resultante se procesa a través de una etapa de potencia dual compuesta por dos chips LM386, cada uno dedicado a un parlante independiente para evitar la sobrecarga de un solo componente y mejorar la respuesta sonora. El circuito está estabilizado por una batería de 9V con capacitores de filtrado de 100uF a la entrada y salida para reducir el ruido, además de capacitores de 10uF en la etapa de amplificación. El resultado es un instrumento robusto y rítmico con una salida de audio clara y una interfaz táctil y visual intuitiva.

imagen del sintetizador en su contexto

audio o video del sintetizador en acción

## proceso y resultados del reloj y secuenciador

con chips 555 y 4017

incluir texto e imágenes sobre cableado, pruebas, resultados obtenidos.

## proceso y resultados de osciladores y amplificador

con chips 4093 y 386

incluir texto e imágenes sobre cableado, pruebas, resultados obtenidos.

## modificaciones realizadas a los circuitos originales

incluir texto, imágenes sobre modificaciones realizadas a los circuitos originales, incluyendo el proceso de diseño, pruebas y resultados obtenidos.

incluir modificaciones en posición, chips, parámetros, valores, etc.

## carcasas de cartón

textos, imágenes

incluir origen de materiales, decisiones de posiciones de los componentes, decisiones estéticas, pruebas, resultados obtenidos.

## interconexión entre módulos

textos, imágenes, diagramas de interconexión

## resultados finales

texto

imagen

video / audio

## aprendizajes y errores

las mejores lecciones aprendidas y los errores más comunes y cómo los resolvieron

## conclusiones

sobre modularidad, materialidad, trabajo en equipo, trabajo electrónico, trabajo maquinal.
