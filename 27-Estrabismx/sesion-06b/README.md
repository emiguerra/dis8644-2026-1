# sesion-06b

## Clase 17 de Abril ##

### 30 Minutos / Referentes ###

- Frei Otto → Soap Film → Jabón

> Paralelismo Gaudi → Sagrada familia → Catenarias 

<br>

- Tokio Metro Fungi 

<br>

### Correcciones al Circuito ### 

Misa nos comentó que luego de desarrollar y experimentar el ejercicio en casa descubrió 4 puntos claves a corregir:

1. PullDown: Se conecta un extremo de una resistencia de 100kΩ entre el output del 555 (pin 3) y el input del 4017 (pin 14), el otro extremo debe llegar a GRND.  Esto con el fin de filtrar la corriente más _dispersa_, en otras palabras eliminar el ruido

![](./imagenes/sc15.png)

>Se implento de la siguiente manera

- Considerar que tambien existe el **PullUp**

2. Condensador Desacople: Este concepto se mencionó anteriormente, pero ahora se profundizó de mejor manera. Similar al Pulldown (según yo xd), en el sentido de que se utiliza para estibilizar al chip del ruido y variaciones de voltaje extremas, que podrían quemarlo. Importante es que fisicamente se ubique cerca del chip, para mayor efectividad.

Se debe conectar un extremo al pin de alimentación y el otro a VCC. Considerar que no se debe reemplezar el capacitor por el cable, deben existir ambos, es decir deben haber 2 conexiones desde el pin de alimentación, un cable / alambre y el capacitor

En este caso se trabajó con capacitores de 100nF (lentejas 104)

3. Condensador De Acople: En este caso se utiliza un capacitor electrólitico de 100μF, que interrumpe la conexión directa del parlante al potenciometro, es decir que el + se conecta al pin 2 de la resistencia variable y el - debe ir al parlante. 

La función es que sirva a modo de _filtro_, para evitar que los componentes previos se quemen, además de reducir el ruido

4. Alimentación

Acá se nos planteo que la familia de chips 4000 (revisar sesion-06a) opera dentro de 3 voltajes posibles, por lo que podemos probar y experimentar para realizar diversas conexiones

  a. 12v: Baterías de auto

  b. 9v: Baterías (las que usamos), paneles solares

  c. 5v: USB A

Mi plan es tener un cable USB A, con conexión dupont al otro extremo, para alimentar los chips con mi batería portatil o con un transformador de celular

<br>

### Desarrollo en clase ###

[Adjuntar imagenes y detaller que salió mal
Spoiler: el error estaba entre el circuito y la silla]

## Desarrollo Post clase ##
