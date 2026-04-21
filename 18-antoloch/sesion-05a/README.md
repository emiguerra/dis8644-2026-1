# sesion-05a
# Apuntes 
> No pude asistir a clases porque me sentía mal del estómago, pero gracias a mis compañeras pude acceder a estos apuntes.

---

## Síntesis y módulos básicos

- **Voltaje (Gate):** señal cuadrada que abre/cierra el paso del sonido.  
- **Oscilador (VCO):** genera ondas (seno, cuadrada, triangular).  
- **LFO:** oscilador de baja frecuencia (<20 Hz), usado para modulación, no audible directamente.  
- **Filtro RC:** controla qué frecuencias pasan o se atenúan.  
- **VCA (Voltage Controlled Amplifier):** amplificador controlado por voltaje.  
- **VCV Rack / Eurorack:** entornos de síntesis modular (software y hardware).  

### Relación entre notas y oscilaciones
- Notas ↔ frecuencia ↔ oscilaciones.  
- El **ruido** también se usa como fuente sonora.

---

##  Lógica digital aplicada

- **Definición de lógica:** ciencia formal que estudia estructuras del pensamiento y razonamiento correcto.  
- **George Boole:** convierte la lógica en operaciones matemáticas → **Álgebra de Boole**.  
- Variables binarias: `0` (GND) y `1` (9V).  
- Onda cuadrada = alternancia rápida entre 0 y 1.  

### Tabla de verdad y compuertas
- **Chip 4093:** compuertas NAND con entradas y salidas definidas.  
- Ejemplo: al armar un circuito, se obtiene ruido como resultado.
    
![4093](./imagenes/4093.png)
---

## Osciladores prácticos

- **Ejercicio con VCO:**  
  - LED conectado.  
  - Potenciómetro RV2 100k.  
  - A mayor capacitancia → oscilación más lenta.  

---

## Schmitt Trigger
![schmitttrigger](./imagenes/schmitttrigger.png)

- **Definición:** comparador con histéresis que convierte señales analógicas ruidosas en ondas cuadradas limpias.  
- Usa dos umbrales (superior e inferior) para evitar falsas conmutaciones.  
- Ejemplo visual:  
  - Entrada: señal ondulada.  
  - Salida: señal cuadrada que cambia al cruzar los umbrales.  
- Analogía: sensor de presión y bomba de agua → la bomba funciona solo cuando la presión está bajo un umbral y se detiene al superar otro.  
- Importante: el sensor **no consume corriente**, solo detecta voltaje.

---

## Ideas clave

- Los sintetizadores combinan **módulos eléctricos** (osciladores, filtros, amplificadores) con **lógica digital** (compuertas, triggers).  
- La lógica binaria (0/1) se traduce en ondas cuadradas, esenciales para el control de sonido.  
- El Schmitt Trigger es fundamental para limpiar señales y evitar ruido en el control.

  
