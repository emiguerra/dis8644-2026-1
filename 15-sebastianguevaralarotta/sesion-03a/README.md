# sesion-03a

## Taller de informática – Diseño de máquinas electrónicas

---

### Análisis – Documental "Variaciones Espectrales" – José Vicente Asuar

El documental presenta el trabajo de José Vicente Asuar como una exploración temprana en la relación entre música y tecnología, donde la máquina deja de ser solo una herramienta y pasa a formar parte activa del proceso creativo. Su enfoque combina conocimientos técnicos con una búsqueda artística, generando sonidos a partir de sistemas electrónicos construidos y modificados por él mismo.

Desde una perspectiva analógica, el documental muestra cómo el sonido se genera a partir de fenómenos físicos reales, como variaciones de voltaje y comportamiento de circuitos. Esto implica una relación directa con el material, donde cada cambio en los componentes afecta el resultado sonoro. A diferencia de la tecnología digital actual, que trabaja con datos discretos y resultados más controlados, en el enfoque de Asuar existe una dimensión más experimental, donde el error y la inestabilidad también forman parte del proceso creativo.

Se puede entender que hay una conexión entre lo analógico y la tecnología, pero no como oposición, sino como evolución. En el documental, los sistemas creados por Asuar funcionan como un punto intermedio, donde comienzan a integrarse lógicas más cercanas a lo computacional, sin perder la materialidad del sonido analógico. Esto refleja una etapa de transición importante en la historia de la música electrónica.

---

### Conclusiones

- La tecnología puede ser utilizada como un medio artístico y expresivo.
- Lo analógico permite una exploración más experimental e impredecible.
- El diseño de sistemas electrónicos también implica decisiones creativas.
- La relación entre humano y máquina es clave en la producción sonora.

---

### Funcionamiento del chip 555 en breadboard

El chip 555 es un circuito integrado muy utilizado para generar señales de temporización, especialmente en configuraciones como el modo astable, donde produce una señal continua que alterna entre encendido y apagado. En la breadboard, su uso requiere una correcta conexión de sus pines, ya que cada uno cumple una función específica dentro del circuito.

El funcionamiento general se basa en la carga y descarga de un condensador a través de resistencias. Cuando el condensador se carga hasta cierto nivel de voltaje, el chip cambia el estado de la salida, y luego comienza a descargarse, repitiendo este ciclo constantemente. Este proceso genera una oscilación, que puede traducirse en un parpadeo (si usamos un LED) o en un sonido (si usamos un parlante).

En la práctica realizada, en lugar de utilizar un LED con su respectiva resistencia, se reemplazó por un capacitor y un parlante. Esto permitió transformar la señal eléctrica en una señal audible, generando un tono continuo cuya frecuencia depende directamente de los valores de las resistencias y del capacitor presentes en el circuito.

Para realizar las conexiones, se utilizaron cables tipo caimán (alligator clips), lo que facilitó la manipulación rápida del circuito y permitió hacer cambios sin necesidad de fijar permanentemente los componentes.

Durante la experimentación, se pudo observar que al cambiar los valores de las resistencias o del capacitor, la frecuencia de oscilación del circuito también cambia. Esto se traduce en variaciones en la velocidad del pulso o en el tono del sonido emitido por el parlante, lo que demuestra de forma práctica la relación entre los componentes y el comportamiento del sistema.

---

### Reflexión de aprendizaje

En lo personal, me ha costado aplicar la lógica del funcionamiento del chip 555, especialmente entender cómo interactúan sus pines y cómo se genera la oscilación internamente. A pesar de esto, mediante la práctica constante en casa he logrado obtener resultados funcionales en los circuitos, lo que demuestra un avance progresivo en mi aprendizaje.

Considero que este proceso ha sido importante, ya que no solo implica entender la teoría, sino también desarrollar una comprensión práctica a través del error y la repetición. Como comentario hacia los profesores, creo que este tipo de ejercicios ayuda bastante, aunque en mi caso requiere más tiempo de experimentación para lograr internalizar completamente la lógica del circuito.
