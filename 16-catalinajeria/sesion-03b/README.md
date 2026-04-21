# sesion-03b

## Clase 27-03-2026

### Apuntes de la clase

En esta clase se trabajó el concepto de resistencias equivalentes y se comenzó a ver el modo de operación monostable del chip 555. También se continuó con el desarrollo del circuito tipo “toy organ”, agregando interruptores para generar distintas combinaciones.

### Resistencias equivalentes

Se explicó que las resistencias equivalentes permiten simplificar un circuito, reemplazando varias resistencias por una sola que tenga el mismo efecto.

**Resistencias en serie:**
- La corriente pasa por una sola trayectoria  
- Las resistencias se suman  
- Ejemplo: 10k + 10k + 10k = 30kΩ  
- A mayor resistencia, menor corriente  

**Resistencias en paralelo:**
- La corriente se divide en distintos caminos  
- La resistencia total disminuye  
- Ejemplo: 2 resistencias de 10k en paralelo = 5kΩ  
- A menor resistencia, mayor corriente  

Caso especial:
- Si las resistencias son iguales → Req = R / 2  

### Uso de interruptores (switch)

Se trabajó con interruptores dentro del circuito:

- Funcionan como elementos que permiten o bloquean el paso de corriente  
- Al presionar un botón, se cierra el circuito  
- Al soltarlo, se abre  

En el toy organ:
- Los botones permiten generar distintas combinaciones  
- Si se presionan varios al mismo tiempo, cambian las resistencias del circuito  

### Modo monostable del 555

Se introdujo el modo monostable del chip 555.

- A diferencia del modo astable, no oscila constantemente  
- Genera un solo pulso cuando se activa  
- Luego vuelve a su estado inicial  

Esto permite controlar eventos más específicos, como activar un sonido solo una vez al presionar un botón.

### Desarrollo del circuito

Se continuó trabajando con el toy organ, integrando:

- Interruptores  
- Resistencias  
- Chip 555  

También se realizaron pruebas conectando distintos componentes y corrigiendo errores en el circuito.

Durante el proceso:
- Se probaron distintas configuraciones  
- Se detectaron fallas en componentes (como un chip que no funcionaba)  
- Se reemplazaron piezas hasta lograr que el circuito funcionara correctamente  

### Conceptos vistos en clase

- LDR: fotoresistor (resistor dependiente de la luz)  
- Importancia de probar y corregir errores en los circuitos  
- Uso de combinaciones de botones para modificar el comportamiento  

También se mencionó que los circuitos pueden entenderse como sistemas que se van armando por partes (input, proceso, output).

### Conclusión

En esta clase se entendió cómo simplificar circuitos usando resistencias equivalentes y cómo los interruptores permiten modificar el comportamiento del circuito en tiempo real.

Además, se aprendió el funcionamiento del modo monostable del 555, lo que permite generar señales controladas en lugar de continuas. El trabajo práctico ayudó a entender mejor el proceso de prueba y error al armar circuitos.
