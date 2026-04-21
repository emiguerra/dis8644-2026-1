# sesion-06a

## Clase 17-04-2026

### Apuntes de la clase

En esta clase se trabajó en la mejora y estabilización de los circuitos que hemos venido desarrollando, enfocándonos en detalles técnicos que afectan directamente el funcionamiento correcto de los chips.

También se revisaron distintos tipos de condensadores y fuentes de energía.

### Ajustes en el circuito

Se realizaron mejoras en las conexiones entre los chips:

- Se agregó una resistencia entre la pata 3 del chip 555 y la pata 14 del chip 4017  
- Esta resistencia funciona como **pull-down**, ayudando a estabilizar la señal  

Esto permite evitar comportamientos erráticos en el circuito.

### Condensadores

Se revisaron distintos tipos de uso de condensadores:

**Condensador de desacople:**
- Se conecta lo más cerca posible del chip  
- Va a tierra (GND)  
- Ayuda a estabilizar la alimentación  

**Condensador de acople:**
- Permite el paso de señal entre partes del circuito  
- Bloquea componentes no deseados  

Estos condensadores son importantes para mejorar el rendimiento del circuito.

### Fuentes de energía

Se revisaron distintas fuentes de alimentación según el voltaje:

- 9V: batería (como las usadas en clase)  
- 12V: batería de auto o paneles solares  
- 5V: USB o power bank  

Es importante considerar el voltaje adecuado según el circuito.

También se mencionó que los dispositivos como cargadores se calientan debido a la fricción generada por el movimiento de la energía.

### Conceptos importantes

- Las resistencias pueden usarse para estabilizar señales  
- La ubicación de los componentes afecta el funcionamiento  
- Es importante revisar el datasheet de los componentes  

### Conclusión

En esta clase se entendió la importancia de ajustar y optimizar los circuitos, agregando componentes que permiten estabilizar su funcionamiento. También se reforzó el uso de distintas fuentes de energía y el rol de los condensadores dentro del circuito.
