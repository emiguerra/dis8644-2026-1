# Sesión 02b: Martes 24 de marzo 
**Temas:** Profundización en el Chip NE555P, componentes de almacenamiento y análisis de frecuencia. 
## 1. Apuntes y Kit de Hardware:
En esta sesión recibimos un set de componentes críticos para la gestión de un **lazo cerrado de energía**. 

### Análisis de Componentes Entregados: 
 ### 🔹**Circuito Integrado NE555P:** 
 📌 **Descripción:**  
 Dispositivo semiconductor utilizado para la generación de pulsos y oscilaciones. Se identifica su orientación mediante el **calado o muesca** en el encapsulado plástico; esta marca posiciona el Pin 1 a su izquierda.
**Especificaciones Técnicas:**
1. **GND (Tierra):** Conexión obligatoria al negativo (0V).
2. **TRIGGER (Disparador):** Inicia el ciclo de salida del chip.
3. **OUTPUT (Salida):** Entrega energía al LED para que parpadee.
4. **RESET (Reinicio):** Interrumpe el ciclo si se conecta a tierra.
5. **CONTROL (Voltaje de Control):** Ajusta la sensibilidad del temporizador.
6. **THRESHOLD (Umbral):** Finaliza el tiempo de encendido del LED.
7. **DISCHARGE (Descarga):** Vacía el capacitor para reiniciar el ciclo.
8. **VCC (Positivo):** Conexión al positivo de la batería (9V).

<img width="400" height="1080" alt="Removed Background" src="https://github.com/user-attachments/assets/9f53d555-630d-4100-b33a-ccecfc42537a" /><img width="500" height="1080" alt="Removed Background(4)" src="https://github.com/user-attachments/assets/53570542-0e43-4dd9-9798-7f9fd0def8aa" />

### 🔹 **Fotorresistor (LDR):** 
📌 **Descripción:**  
Resistencia variable dependiente de la luz. Su función es traducir la intensidad lumínica en una señal eléctrica (resistencia), permitiendo controlar la frecuencia del circuito según el entorno.

Comportamiento dinámico:
- Presenta una relación inversamente proporcional entre la luz y la resistencia.
  - **☀️Alta luminosidad:** La resistencia disminuye drásticamente, permitiendo un mayor flujo de corriente hacia el pin 2 (Trigger) del NE555P.
  - **🌙Baja luminosidad (oscuridad):** La resistencia aumenta, limitando el paso de electrones y ralentizando el ciclo de disparo.

Integración en el sistema:
- En nuestro circuito, el LDR actúa como sensor de entrada que define la **frecuencia de oscilación**.
- Al variar la luz, se modifica el tiempo de carga del capacitor.
- Esto se traduce visualmente en un cambio en la velocidad de parpadeo del LED.

### 🧠 Dato extra:
El LDR es un componente **analógico**, ya que no funciona solo como encendido/apagado, sino que trabaja con un rango continuo de valores de resistencia.

<img width="500" alt="Circuito 555" src="https://github.com/user-attachments/assets/d5dc931d-e25e-44cc-bf00-f6708f591b80" /> 
<img width="500" height="1080" alt="Removed Background(2)" src="https://github.com/user-attachments/assets/835ffe75-f13a-42a1-9ac6-47d786de76d7" />



### 🔹 **Capacitores Cerámicos:** Almacenamiento
 
📌 **Descripción:**  
Es un componente electrónico pasivo que almacena energía en un campo eléctrico, utilizando pequeñas láminas de cerámica como material dieléctrico (aislante) o en otras palabras un capacitor cerámico es como una jeringa (poca capacidad, pero entrega el líquido con mucha precisión).


🔸Forma tipo lenteja
🔸 No tiene polaridad
🔸Ideal para alta frecuencia
🔸Uso: señales rápidas, oscilaciones (como con el NE555)

🧮 Escalas de Medida

    Picofaradios (pF): Los más pequeños (ej. código 22 = 22 pF22 pF). → milímetros 
    Nanofaradios (nF): Los medianos (ej. código 103 = 10 nF10 nF). → centímetros 
    Microfaradios (µF): Los más grandes (ej. código 104 = 100 nF100 nF o 0.1 µF0.1 µF). → metros


<img width="500" height="1080" alt="Removed Background(5)" src="https://github.com/user-attachments/assets/3d3d7d4b-b663-4e4d-87f3-ca7242278de2" />
<img width="500" height="1080" alt="Removed Background(6)" src="https://github.com/user-attachments/assets/51fcad7b-030a-494d-9cbc-8538ceab1a43" />

### 🟠 ¿Cómo leer un Capacitor Cerámico? 
(Código EIA ⭐Electronic Industries Alliance, estandar mundial) Como estos capacitores son tan diminutos, usan un código de **3 números** para decirnos cuánta energía guardan (su capacidad). 

1. Los **dos primeros números** se quedan tal cual.
2. El **tercer número** te dice cuántos ceros tienes que agregar. 
3. El resultado siempre está en **Picofaradios (pF)**. 
> [Ejemplo] > **con el código 104:** > Tenemos un **10** + **0000** (4 ceros) = $100,000\text{ pF}$.
> *esto lo llamamos simplemente **0.1µF**.*

### 🧠 Dato extra:
Aunque se ven parecidos, su capacidad suele ser mucho menor que la de los electrolíticos. Por eso se miden en picofaradios (pF) o nanofaradios (nF), mientras que los grandes se miden en microfaradios (µF). Ademas, el código de 3 dígitos siempre te da el resultado en pF. Si necesitas pasarlo a Nanofaradios (nF) o Microfaradios (µF), tienes que mover la coma decimal hacia la izquierda.

### 🔹  **Capacitor Electrolítico: Almacenamiento Masivo**
📌**Descripción:**  
Es un componente diseñado para almacenar grandes cantidades de energía en comparación con los cerámicos. Se llama "electrolítico" porque utiliza un líquido iónico (electrolito) como una de sus placas, lo que permite que sea muy eficiente en un tamaño compacto.

🔸Forma: Cilíndrica (parece un tanque o barril).

🔸 Polaridad: ⚠️ Crítica porque tiene un polo positivo y uno negativo. Si se conecta al revés, el gas interno se expande y puede explotar o incendiarse.

🔸Uso principal: Filtrado de corriente, suavizado de voltajes y almacenamiento de energía en fuentes de alimentación.

<img width="500" height="1080" alt="Removed Background(7)" src="https://github.com/user-attachments/assets/8d44a0d5-12a9-4ec6-8fd3-830baa6200a5" />
<img width="500" height="1080" alt="Removed Background(8)" src="https://github.com/user-attachments/assets/37740732-a165-4761-990d-6961801787b1" />

🧮 Cómo leerlo (Sin códigos secretos)

A diferencia de las "lentejas", aquí el fabricante escribe todo claro en el cuerpo:

    Capacitancia: Se ve un número seguido de µF (microfaradios). Por ejemplo: 10 µF,100 µF,1000 µF10 µF,100 µF,1000 µF.
    Voltaje Máximo: Se ve un número seguido de V (voltios). Es el límite de "presión" eléctrica que aguanta antes de romperse (ej. 16V,25V,50V16V,25V,50V).
    Banda de Polaridad: Verás una franja de color distinto (usualmente gris o blanca) con signos de "menos" (-). Ese es el pin negativo (Cátodo).

**Diferencias Clave: Cerámico vs. Electrolítico**
| Característica | Cerámico ("Lenteja") | Electrolítico ("Cilindro") |
| --- | --- | --- |
| Capacidad | Muy pequeña (pFpFpF a nFnFnF) | Muy grande (μF\\mu FμF) |
| Polaridad | No tiene (da igual como lo pongas) | Sí tiene (debe respetarse) |
| Símbolo | Dos líneas paralelas iguales | Una línea blanca (+) y una negra (-) |
| Analogía | Una jeringa (poca agua, mucha precisión) | Un tanque (mucha agua, reserva) |

❗Peligro: El error de polaridad
Conectar un electrolítico al revés provoca una reacción química interna que genera calor y presión. La muesca en forma de "K" o "X" que ves en la parte superior metálica es una válvula de seguridad para que el capacitor se "infle" o se abra en lugar de estallar como un proyectil.

🔘 Guía de Lectura de Esquemáticos:

    Fixed Capacitor (No polarizado): Representado por dos líneas paralelas rectas. Es el símbolo para los cerámicos. Al ser simétrico, no importa la orientación.
    Polarized Capacitor (Polarizado): Tiene una línea recta (Positivo + + ) y una línea curva (Negativo − − ). En diseños antiguos, puede aparecer con una línea más gruesa o sombreada.
    Variable Capacitor: Es igual al fijo pero con una flecha que lo cruza, indicando que su capacidad se puede ajustar manualmente.

💡Tip montaje:
Si el capacitor es nuevo, la pata más larga siempre es la positiva (+). Si las patas están cortadas, guíarse por la franja de color en el cuerpo del cilindro para identificar el negativo (-).


## 2. Lectura de Esquemáticos y Simbología - Profundización:
* **Nodos de Conexión:** Puntos de unión física entre terminales. Si dos líneas se cruzan sin un punto marcado, no existe contacto eléctrico entre ellas.
* **Resistencias (R):** Identificadas por su valor en Ohms ($\Omega$). Se utiliza el **Código de Colores** para determinar su valor nominal y tolerancia (banda dorada).
* **Capacitancia (C):** Representada por el símbolo de dos líneas paralelas. Se miden en Faradios ($nF$ o $\mu F$ según el tamaño).
* **Diodo LED (D):** Semiconductor emisor de luz. Se diferencia el ánodo (positivo) del cátodo (negativo) por la longitud de sus terminales.
* **VCC / GND:** Diferencia de potencial necesaria para la circulación de electrones (9V hacia 0V).

## 3. Registro de Actividad y Análisis de Circuitos Basado en los esquemas proyectados, se realizaron las siguientes observaciones sobre la interacción de los componentes en paralelo y serie: 
* **Resistencias en Paralelo:** Al ofrecer múltiples caminos a la corriente, la resistencia total del sistema **disminuye**.
* **Capacitores en Paralelo:** A diferencia de las resistencias, sus capacidades se suman aritméticamente ($C_{total} = C_1 + C_2$), aumentando el tiempo de almacenamiento.
* **Modificación técnica:** Se integró un tercer LED con su respectiva resistencia de protección, puenteando el terminal hacia el nodo vinculado al pin 5 del integrado para observar variaciones en la salida de señal. ![Registro de bitácora: Diagrama del CI 555 y lógica de conexiones]

## 4. Investigación y Cuestionamiento Crítico Se plantean las siguientes interrogantes para profundizar en el comportamiento del hardware: 
1. ¿Cuál es el impacto térmico o eléctrico de invertir la polaridad en los pines de alimentación del NE555P?
2. ¿Cómo influye el material de las bandas de colores en la precisión del valor nominal de la resistencia?
3. ¿Por qué el capacitor cerámico, a diferencia del electrolítico, no requiere una orientación específica para cerrar el lazo?
4. ¿Cómo afecta la longitud física de los terminales (ánodo y cátodo) en la eficiencia de montaje del LED?
5. ¿Qué implicancias técnicas tiene el prefijo "k" ($10^3$) en la escala de medición de Ohms?
6. ¿Existe un estándar cromático en el cableado para diferenciar VCC de GND en prototipos complejos?
7. ¿Cuál es la función técnica de los pines que permanecen inactivos en el esquema del 555?
8. ¿Existe riesgo de descarga estática o térmica al manipular componentes bajo carga de 9V?
9. ¿Cuál es la convención de marcado para diferenciar capacitores cerámicos de valores similares a simple vista?
10. ¿Cuál es la curva de degradación de un LED operado sin resistencia de protección ante una fuente de 9V?
11. ¿Por qué los capacitores cerámicos son “más rápidos”?

🔹 🔸 🔷 🔶 ⭐ ⚡ 🔘 🟢 🔴
