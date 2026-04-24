
# sesion-05b  
## Martes 07 de Abril del 2026  
### Sintetizador Modular y Amplificación

---

### Síntesis de la sesión

En esta clase trabajamos en la transición entre lo digital y lo físico dentro del sonido, combinando lógica electrónica con amplificación real. La experiencia se centró en entender cómo un circuito deja de ser solo un esquema y se convierte en un sistema audible, donde cada componente influye directamente en el resultado.

El foco estuvo en construir un sintetizador básico utilizando el chip CD4093 como generador de señal y el LM386 como amplificador. A través de esto, se hizo evidente que el sonido no aparece “de la nada”, sino que es el resultado de una serie de procesos eléctricos que se organizan en el tiempo.

---

### El circuito como sistema (CD4093 + LM386)

El CD4093 funciona como el origen del sonido. A partir de compuertas lógicas, genera una señal oscilante que se puede interpretar como tono. Lo interesante es que, aunque es un chip digital, en este contexto se comporta como un generador sonoro, mostrando cómo la lógica puede convertirse en ritmo y frecuencia.

Por otro lado, el LM386 cumple un rol fundamental: amplificar esa señal. Sin este componente, el sonido existe, pero no es perceptible. Esto permite entender que en un circuito no basta con generar información, también es necesario traducirla a algo físico, como el movimiento de un parlante.

---

### Control del sonido y experimentación

Uno de los aprendizajes más relevantes fue cómo pequeñas variaciones en los componentes afectan directamente el resultado. Al modificar resistencias, capacitores o potenciómetros, cambia la frecuencia, el ritmo y la textura del sonido.

El uso de dos osciladores conectados en cadena permitió observar una jerarquía dentro del sistema: uno define el pulso (ritmo) y el otro el tono. Esta relación hace que el circuito deje de ser algo estático y pase a comportarse como un sistema dinámico, donde un elemento controla a otro.

También se incorporó la idea de “textura”, entendida no solo como un sonido limpio, sino como la suma de imperfecciones, interferencias y variaciones. Elementos como el contacto físico con el circuito o conexiones menos estables generan ruido, que en lugar de ser un error, puede ser parte del resultado expresivo.

---

### Aprendizaje práctico

Trabajar en el protoboard implicó enfrentarse a errores reales, lo que fue clave para el aprendizaje. Aspectos como la orientación de los capacitores, la correcta identificación de resistencias o la lectura de los pines de los chips fueron fundamentales para que el circuito funcionara.

Más allá de lo técnico, el proceso consistió en entender el flujo de la señal. Seguir el recorrido desde la generación hasta la amplificación permitió construir una lógica más clara de cómo interactúan los componentes.

---

### VCV Rack vs. protoboard

El uso de VCV Rack complementó el trabajo físico, funcionando como un espacio de simulación donde se pueden probar ideas sin errores materiales. En este entorno, las conexiones son limpias y los módulos funcionan de manera ideal.

En contraste, el protoboard introduce variables reales como ruido, fallas de conexión o limitaciones de energía. Esta diferencia permitió comprender que el software sirve para entender la lógica, mientras que el hardware obliga a enfrentarse a las condiciones reales del sistema.

---

### Enfoque de aprendizaje

Un aspecto importante del proceso fue la decisión de descomponer el circuito en partes más pequeñas para entenderlo mejor. Analizar cada componente por separado facilitó la comprensión general, especialmente en un sistema donde todo está interconectado.

Aunque al inicio costó entender la lógica del circuito y evitar errores básicos, la repetición y la práctica permitieron avanzar. El aprendizaje se dio principalmente a través de la experimentación, donde equivocarse fue parte del proceso para lograr resultados funcionales.


<img width="400" height="550" alt="SintetizadorModularyAmplificación" src="https://github.com/user-attachments/assets/d91fbbab-4e2a-4e01-bb15-06ed43b2e2cd" />

---

### Conclusión

La sesión permitió entender el circuito como un instrumento más que como un objeto técnico. A través del CD4093 y el LM386, se evidenció cómo la electricidad puede transformarse en sonido, y cómo ese sonido puede ser manipulado a través de decisiones de diseño.

Este enfoque conecta directamente con la idea de síntesis modular: no se trata solo de construir, sino de explorar, modificar y comprender el comportamiento del sistema en su totalidad.

---

### Fuentes

- https://vcvrack.com/  
- https://circuitosonorolab.com/  
- https://www.soundonsound.com/techniques/introduction-frequency-modulation  
- https://learn.sparkfun.com/tutorials/capacitors/application-examples  
- https://www.ti.com/lit/ds/symlink/cd4093b.pdf  
- https://www.ti.com/lit/ds/symlink/lm386.pdf  
