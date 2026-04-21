# sesion-02b

## Clase 20-03-2026

### Apuntes de la clase

En esta clase seguimos avanzando en electrónica y comenzamos a trabajar con esquemáticos, capacitores y el chip 555. Se entendió cómo se pueden crear circuitos que funcionan de forma automática, como hacer que un LED parpadee solo.

También se reforzaron conceptos importantes como la ley de Ohm y su aplicación en los circuitos armados en protoboard.

### Ley de Ohm

Se trabajó con la fórmula:

V = I × R  

Donde:
- V = voltaje  
- I = corriente  
- R = resistencia  

Ejemplo visto en clase:  
9V / 220Ω ≈ 0,04 A → 40 mA  

Esto permite calcular la corriente del circuito y entender si los componentes están funcionando correctamente.

### Capacitores y condensadores

Se trabajó con dos tipos de capacitores:

**Capacitor electrolítico:**
- Es polarizado  
- Tiene una banda gris que indica el lado negativo  
- Se mide en µF (microfaradios)  
- Sirve para almacenar energía y controlar tiempos  

**Condensador cerámico:**
- No es polarizado  
- Es más pequeño (tipo lenteja)  
- Tiene códigos como “104”  
- Sirve para estabilizar o filtrar el circuito  

Los valores de los capacitores pueden variar, ya que tienen un margen de error.

### Chip 555

El chip 555 es un circuito integrado importante.

- Tiene 8 patas  
- Se identifica por una muesca  
- Se cuentan en sentido contrario a las agujas del reloj  

Su función principal es generar pulsos y permitir temporización en circuitos, por ejemplo, hacer que un LED se prenda y apague automáticamente.

### Experimentos realizados

**Uso de capacitores:**

- Con 10 µF el LED parpadea rápido  
- Con 100 µF el LED parpadea más lento  
- Con más capacitores el tiempo aumenta  
- Sin capacitor el LED queda encendido  

Esto demuestra que el capacitor controla el tiempo del circuito.

**Potenciómetro:**

- Tiene 3 patas  
- Funciona como una resistencia variable  
- Permite regular la velocidad del parpadeo del LED  

**Fotoresistor:**

- No tiene polaridad  
- Funciona dependiendo de la luz  

A mayor luz, cambia su resistencia y modifica el comportamiento del circuito.

### Conceptos importantes

- Un circuito es un lazo cerrado  
- Si se interrumpe, deja de funcionar  
- VCC corresponde al voltaje positivo  
- GND corresponde a tierra (0V)  

También se trabajó con conexiones en serie y paralelo. La forma del circuito puede cambiar, pero si las conexiones son las mismas, el funcionamiento no cambia.

En esta clase se entendió cómo los capacitores y el chip 555 permiten controlar el tiempo en un circuito. También se vio cómo distintos componentes como el potenciómetro y el fotoresistor modifican el comportamiento del circuito, permitiendo experimentar y entender mejor su funcionamiento.
