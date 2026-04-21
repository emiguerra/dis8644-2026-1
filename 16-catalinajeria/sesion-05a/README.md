# sesion-05a

## Clase 10-04-2026

### Apuntes de la clase

En esta clase se comenzó a trabajar con la idea de interfaz y experiencia de usuario (UX), aplicándola a los circuitos electrónicos que hemos estado desarrollando.

Se planteó que los circuitos no solo deben funcionar, sino también tener una forma de interacción clara, por ejemplo mediante perillas, botones o movimientos.

### Interfaz y UX

Se habló sobre cómo interactuamos con los dispositivos:

- Push (presionar)  
- Turn (girar)  
- Move (mover)  

La idea es que el usuario pueda entender fácilmente cómo usar el dispositivo.

También se mencionó el concepto de “campo de sentido”, relacionado con la estética (aesthetic), es decir, cómo se percibe y se entiende un objeto más allá de su funcionamiento técnico.

### Propuesta de interfaz

Se propuso construir una interfaz física utilizando cartón:

- Una caja con perillas o controles  
- Otra sección donde esté el parlante  
- El objetivo es que el dispositivo emita sonido y sea manipulable  

Esto busca integrar lo técnico con lo visual y lo interactivo.

### Uso del chip 555 y CD4093

Se continuó trabajando con el chip 555 en modo astable.

También se mencionó el uso del chip CD4093:
- Se debe conectar la pata 14 a positivo (VCC)  
- Se debe conectar la pata 7 a negativo (GND)  

### Contador de década (chip 4017)

Se introdujo el chip 4017:

- Tiene 16 patas  
- Funciona como contador de década  
- Cuenta de 0 a 9 (10 estados distintos)  

Este chip permite activar salidas de forma secuencial.

### Circuito realizado

Se trabajó en un circuito que combina:

- Chip 555 (genera pulsos)  
- Chip 4017 (cuenta y distribuye la señal)  

El resultado fue:

- Encendido secuencial de 4 LEDs  
- Control de velocidad mediante potenciómetro  

Durante el desarrollo:

- Se presentaron dificultades para conectar correctamente los chips  
- Fue importante respetar el esquema  
- Revisar bien la posición de los jumpers  
- Asegurar que positivos y negativos estén correctamente conectados  

Finalmente, el circuito logró funcionar correctamente.

### Conceptos importantes

- El chip 555 genera la señal  
- El chip 4017 distribuye la señal en secuencia  
- El potenciómetro permite controlar la velocidad  
- La correcta conexión de los componentes es clave para el funcionamiento  

### Conclusión

En esta clase se integró el concepto de interfaz con los circuitos electrónicos, entendiendo que no solo importa el funcionamiento, sino también cómo el usuario interactúa con el sistema.

Además, se aprendió a utilizar el chip 4017 junto al 555 para generar secuencias, lo que permite crear circuitos más dinámicos e interactivos.
