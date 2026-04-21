# sesion-04b

## Clase 07-04-2026

### Apuntes de la clase

En esta clase se comenzó a trabajar con herramientas digitales para la creación de sonido, específicamente con VCV Rack, que permite simular sintetizadores modulares de forma virtual.

Se explicó cómo funcionan los sintetizadores tipo Eurorack y cómo se pueden replicar de manera digital sin necesidad de tener el hardware físico.

### Introducción a sintetizadores

Se mencionaron distintas formas de construir sintetizadores:

- Eurorack (modular)  
- Moog Unit  

También se explicó el flujo básico del sonido en un sintetizador:

Voltaje → Oscilador → Filtro → VCA → Salida (parlante)

### VCV Rack

Se utilizó el programa VCV Rack:

- Permite crear sintetizadores virtuales  
- Se pueden agregar módulos haciendo click derecho  
- Tiene entradas y salidas que se conectan mediante cables virtuales  

Algunos módulos tienen distintos tipos de conexión:
- Entrada (input)  
- Salida (output)  

Cuando una señal pasa, se activa una compuerta (gate).

### Tipos de módulos

**VCO (Oscilador controlado por voltaje):**
- Genera sonido  
- Se puede controlar su frecuencia  

Tipos de ondas:
- Seno (Sin)  
- Triangular (Tri)  
- Sierra (Saw)  
- Cuadrada (Square)  

Cada una tiene un sonido distinto.

**LFO (Low Frequency Oscillator):**
- Oscilador de baja frecuencia  
- Se usa para modular otros parámetros  

**VCA (Amplificador controlado por voltaje):**
- Controla el volumen  
- Permite subir o bajar la intensidad del sonido  

**VCF (Filtro):**
- Modifica el sonido  
- Permite dejar pasar ciertas frecuencias  

### Conceptos digitales

Se introdujo la lógica digital basada en el álgebra de Boole:

- 1 = encendido (9V)  
- 0 = apagado (tierra)  

Compuertas lógicas:

- AND: solo funciona si ambas entradas están activas  
- OR: funciona si al menos una entrada está activa  
- NOT: invierte la señal  
- NAND: contrario de AND  

También se mencionó el concepto de clock (CLK), que funciona como temporizador.

### Chip 4093

Se trabajó con el chip 4093:

- Utiliza compuertas lógicas tipo NAND  
- Permite trabajar con señales digitales  

Se usaron resistencias y capacitores para modificar la frecuencia del circuito.

### Observaciones en protoboard

Se detectó que la protoboard tiene líneas internas separadas, por lo que:

- Es necesario unir las líneas de positivo  
- Es necesario unir las líneas de negativo  

Esto se hace utilizando cables jumper.

### Encargo

Investigar el concepto de Schmitt Trigger.

**Definición:**

Un Schmitt Trigger es un circuito que convierte señales inestables en señales digitales más claras.

- Usa dos niveles de referencia  
- Evita cambios erráticos en la señal  
- Genera una salida más estable  

Se utiliza para limpiar señales y mejorar la transición entre señales analógicas y digitales.

### Conclusión

En esta clase se introdujo el uso de sintetizadores digitales y conceptos básicos de lógica electrónica. También se entendió cómo distintos módulos trabajan juntos para generar sonido y cómo se pueden controlar mediante voltaje.

Además, se reforzó la importancia de la conexión correcta en la protoboard y el uso de componentes para modificar el comportamiento del circuito.
