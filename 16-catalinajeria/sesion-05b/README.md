# sesion-05b

## Clase 14-04-2026

### Apuntes de la clase

En esta clase se profundizó en el concepto de Schmitt Trigger y cómo se relaciona con el comportamiento de los circuitos electrónicos, especialmente en la estabilidad de las señales.

También se continuó trabajando con los chips 4093 y 4017, entendiendo mejor su funcionamiento dentro de los circuitos.

### Schmitt Trigger

Se explicó que el Schmitt Trigger es un tipo de circuito que permite estabilizar señales.

A diferencia de un comparador simple:
- No trabaja con un solo valor de referencia  
- Utiliza dos umbrales distintos  

Esto se conoce como histéresis.

### Histéresis

La histéresis significa que el circuito considera no solo el estado actual de la señal, sino también su estado anterior.

- Tiene un umbral para subir  
- Tiene otro umbral para bajar  

Esto evita cambios bruscos o inestables en la señal.

### Comparador

Se explicó el funcionamiento básico de un comparador:

- Si A > B → hay salida (se activa)  
- Si B > A → no hay salida o se invierte  

Esto permite decidir cuándo una señal debe activarse o no.

### Chip 4093

Se trabajó con el chip 4093:

- Funciona con compuertas tipo NAND  
- Solo oscila si el pin 2 está en positivo (V++)  

Este chip se utiliza para trabajar con señales digitales y oscilaciones controladas.

### Chip 4017

Se reforzó el uso del chip 4017:

- Es un contador de década  
- Cuenta de forma secuencial  

En la práctica:
- Se configuró para contar hasta 4  
- En el quinto pulso se resetea  

Esto permite controlar secuencias específicas dentro del circuito.

### Conceptos importantes

- El comportamiento de una señal no depende solo del momento actual, sino también de su historial  
- La histéresis permite mayor estabilidad  
- Los chips pueden trabajar en conjunto para lograr comportamientos más complejos  

### Conclusión

En esta clase se entendió cómo el Schmitt Trigger y la histéresis ayudan a estabilizar señales en los circuitos. También se reforzó el uso de los chips 4093 y 4017, logrando un mayor control sobre las secuencias y el comportamiento del circuito.
