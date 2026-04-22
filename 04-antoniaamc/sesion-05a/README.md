# sesion-05a  
7 de Abril

### *Sintetizador modular*  
sonido como sistema

El sonido no es algo inmediato:  
es el resultado de un **flujo estructurado de electricidad + decisiones lógicas + manipulación modular**

electricidad -> organización -> sonido

-------------------

## 2. Arquitectura general del sistema

### Flujo completo:
**Gesto -> Voltaje -> Procesamiento -> Amplificación -> Sonido**

1. **Input**  
   - gesto / interacción
     
2. **Conversión**  
   - voltaje (señal eléctrica)
  
3. **Procesamiento modular**  
   - VCO (oscilador)
   - LFO (modulación)
   - Filtro RC
   - VCA (control de volumen)
     
5. **Salida**  
   - LM386 -> parlante

------------------------------

## 3. Módulos (más importantes!!)

### Generación

- **CD4093 (Oscilador)**
Circuito integrado de 14 patas que contiene 4 compuertas NAND con *disparador Schmitt (Schmitt Trigger)*. Se usa para generar la señal (sonido).

![bitacora-05-a](./imagenes/cd4093-bitacora-sesion-05-a-antoniaamc.jpg)  
Página con muy buenas explicaciones: [CD4093](https://www.build-electronic-circuits.com/4000-series-integrated-circuits/ic-4093/)

![bitacora-05-a](./imagenes/circuito-integrado-4093-bitacora-sesion-05-a-antoniaamc.jpg)

## Tabla de Pines (Pinout)

El CD4093 contiene 4 compuertas NAND con Schmitt Trigger  
Cada compuerta tiene: 2 entradas + 1 salida

| Pin | Tipo | Función | Descripción |
|----|------|--------|------------|
| 1  | Entrada | Gate 1 - Input A | Entrada A de la compuerta NAND 1 |
| 2  | Entrada | Gate 1 - Input B | Entrada B de la compuerta NAND 1 |
| 3  | Salida  | Gate 1 - Output  | Salida de la compuerta NAND 1 |
| 4  | Salida  | Gate 2 - Output  | Salida de la compuerta NAND 2 |
| 5  | Entrada | Gate 2 - Input A | Entrada A de la compuerta NAND 2 |
| 6  | Entrada | Gate 2 - Input B | Entrada B de la compuerta NAND 2 |
| 7  | Alimentación | GND | Tierra (0V) |
| 8  | Entrada | Gate 3 - Input A | Entrada A de la compuerta NAND 3 |
| 9  | Entrada | Gate 3 - Input B | Entrada B de la compuerta NAND 3 |
| 10 | Salida  | Gate 3 - Output  | Salida de la compuerta NAND 3 |
| 11 | Salida  | Gate 4 - Output  | Salida de la compuerta NAND 4 |
| 12 | Entrada | Gate 4 - Input A | Entrada A de la compuerta NAND 4 |
| 13 | Entrada | Gate 4 - Input B | Entrada B de la compuerta NAND 4 |
| 14 | Alimentación | VCC | Voltaje positivo (+3V a +15V) |

## Explicación General

| Categoría | Descripción |
|----------|------------|
| Tipo | Circuito integrado lógico |
| Función principal | Contiene 4 compuertas NAND con Schmitt Trigger |
| Número de pines | 14 |
| Alimentación | Pin 14 = VCC (+) / Pin 7 = GND (−) |
| Tipo de señal | Digital (0 y 1), pero puede trabajar con señales analógicas simples |
| Rango de voltaje | 3V a 15V |
| Uso principal | Osciladores, temporizadores, lógica digital, modulación |

## Compuerta NAND (base del 4093)

| Entrada A | Entrada B | Salida |
|----------|----------|--------|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

**Regla:**  
La salida es 0 solo cuando ambas entradas son 1.

## Usos en el sintetizador

| Función | Cómo se implementa |
|--------|------------------|
| Oscilador | NAND + resistencia + capacitor |
| Control de tono | Cambiando resistencia (potenciómetro) |
| Control de ritmo | Cambiando capacitor |
| Modulación | Conectando una compuerta a otra |
| Generación de textura | Interferencia / variaciones en señal |

### Modulación
- **LFO / segundo oscilador**
  - altera:
    - tono
    - volumen
    - ritmo
- Ejemplo:
  - oscilador que controla otro oscilador

### Control
- **VCA**
  - permite activar/desactivar el sonido
- **potenciómetros**
  - control manual (tono / ritmo)

### Estabilidad
- **Schmitt Trigger (CD4093)**
  - limpia señales
  - convierte ruido → 0 o 1

### Amplificación

- **LM386 / JRC386**
  Circuito integrado que consiste en un amplificador que requiere bajo voltaje, tanto en la entrada de audio como en la alimentación (hace audible la señal).
 
![bitacora-05-a](./imagenes/lm386-bitacora-sesion-05-a-antoniaamc.jpg)  
Fuente: [Link](https://www.electrosmash.com/es/analisis-lm386)

## Tabla de Pines (Amplificador de Audio)

El LM386 es un amplificador de baja potencia que toma una señal débil y la hace audible en un parlante.

| Pin | Nombre | Función | Explicación |
|----|--------|--------|------------|
| 1  | Gain   | Control de ganancia | Junto al pin 8 permite ajustar la amplificación (con capacitor se aumenta la ganancia) |
| 2  | Input (-) | Entrada inversora | Entrada negativa de la señal (generalmente conectada a GND) |
| 3  | Input (+) | Entrada no inversora | Aquí entra la señal de audio desde el circuito (ej: CD4093) |
| 4  | GND    | Tierra | Conexión a tierra (0V) |
| 5  | Output | Salida de audio | Señal amplificada hacia el parlante (normalmente con capacitor) |
| 6  | VCC    | Alimentación | Voltaje positivo (4V a 12V aprox.) |
| 7  | Bypass | Filtro de ruido | Se puede conectar un capacitor a GND para reducir ruido |
| 8  | Gain   | Control de ganancia | Junto al pin 1 define el nivel de amplificación |
 
--------------------------------------

## 4. LÓGICA: BASE DEL CIRCUITO

### Valores:
- 0 = apagado  
- 1 = encendido  

### Operadores:
- AND -> ambos activos
- OR -> al menos uno activo
- XOR -> solo uno activo
- NAND -> no ambos
- NOR -> ninguno activo
- XNOR -> iguales
- NOT -> invierte
  
-----------------------------------------

### Referentes y recomendaciones

  ## Circuito Sonoro Lab

Circuito Sonoro Lab (Chile, Claudia González) es un referente clave.  
Trabajan desde el **low-tech**, usando chips como el CD4093, mostrando que no se necesita tecnología cara para generar sonido complejo.

### Textura

- **RV1 (tono)** → cambia el “grosor” del sonido  
- **RV2 (ritmo)** → fragmenta el sonido  
- **Interferencia** (cables sueltos / tocar el chip) → agrega “suciedad”  

El circuito no es solo técnico, es un **instrumento que se toca**

### Conexión con el proyecto

Estamos pasando de lo teórico a lo táctil:  
manipular electricidad -> convertirla en sonido

### 💡Dato

Funciona como **arqueología de medios**:  
reutiliza componentes antiguos para crear dispositivos nuevos.

-------------------------------------------------------------

## Digital a físico

### VCV Rack 
Software de código abierto que simula sintetizadores modulares bajo el estándar Eurorack.

- simulación modular
- sin errores físicos
- ideal para entender flujo de señal

### Protoboard

- implementación real
- ruido eléctrico
- errores de conexión
- polaridad

**Resumen:**  
VCV = teoría  
Protoboard = práctica

## Anotaciones y síntesis:

**Textura y error**:

- interferencia = textura
- cables sueltos = variación
- error = recurso creativo

**Capa conceptual**

- lógica filosófica -> verdad  
- lógica computacional -> 0/1  
- lógica electrónica -> voltaje  

***lógica sonora -> experiencia***

**Patrones clave**

- modulación
- flujo de señal
- control vs ruido
- modularidad
- traducción (idea -> electricidad -> sonido)

## Insight para nuestro proyecto

Diseñar un sintetizador implica definir:

- cómo se controla
- qué se deja al error
- cómo opera la lógica
- cómo interactúa el usuario

***> diseñar sonido = diseñar comportamiento eléctrico***

- Oscilador -> genera señal  
- Lógica -> decide comportamiento  
- Modulación -> transforma  
- Schmitt Trigger -> estabiliza  
- Amplificador -> hace audible  
- Error -> aporta carácter

----------------------------------
## Encargo

### ¿Qué es un Schmitt Trigger?  
Circuito que convierte señales inestables o ruidosas en señales digitales limpias (0 o 1).

Funciona mediante dos umbrales de voltaje:
- si la señal supera el umbral alto -> se interpreta como 1  
- si baja del umbral bajo -> se interpreta como 0  

Esto evita errores y hace que la señal sea más estable.
-> Transforma ruido en una señal clara y utilizable.

## Bibliografía

- Colaboradores de Wikipedia. (2025, 25 de diciembre). *VCV Rack*. Wikipedia, la enciclopedia libre.  
  https://en.wikipedia.org/wiki/VCV_Rack

- Colaboradores de Wikipedia. (2020, 2 de agosto). *LM386*. Wikipedia, la enciclopedia libre.  
  https://es.wikipedia.org/wiki/LM386

- Build Electronic Circuits. (2023, 3 de enero). *CD4093 – Circuito integrado con cuatro compuertas NAND con Schmitt Trigger*.  
  https://www.build-electronic-circuits.com/4000-series-integrated-circuits/ic-4093/












