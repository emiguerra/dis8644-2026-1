# sesion-06a

## Schmitt Trigger

Un **Schmitt Trigger** es un comparador con histéresis.

### Función:
Convierte señales analógicas ruidosas en señales digitales limpias.

---

### Ejemplo real: CD4093

- 4 compuertas NAND
- Entradas con histéresis

### Usos:
- Debouncing (botones)
- Osciladores RC
- Limpieza de señal

---

##  4. Comparador

- Si `A > B` → salida = 1
- Si `A < B` → salida = 0

###  Relación:
El Schmitt Trigger es un comparador mejorado:
- Añade memoria
- Mayor estabilidad
  
![notas](./imagenes/notas.jpeg)
---

## Voltajes

- `Vcc` → alimentación
- `GND` → referencia
- `Vi` → entrada
- `Vo` → salida


## Memoria en circuitos

La histéresis implica que:
> El sistema recuerda su estado anterior

---

##  Puertas lógicas

| Puerta | Función |
|------|--------|
| AND | Todas deben ser 1 |
| OR | Al menos una es 1 |
| NOT | Invierte señal |
| NAND | AND negada |


## Sistema práctico con ICs

### Componentes:
- NE555 
- CD4017 
- CD4093 
---

### Funcionamiento:

El **NE555** en modo astable genera:
- Señal cuadrada (clock)

El **CD4093**:
- Elimina ruido
- Estabiliza la señal

El **CD4017**:
- Cuenta pulsos
- Activa salidas secuenciales

---

## Familia CMOS 4000

### Características:
- Bajo consumo
- Amplio rango de voltaje
- Alta inmunidad al ruido

---

## Problemas comunes

Sin histéresis:
- Oscilaciones no deseadas
- Rebotes
- Señales inestables

---

##  Aplicaciones

- Botones (debounce)
- Sensores analógicos → digital
- Osciladores
- Sistemas secuenciales
- Interfaces electrónicas

---

## resumennn

- Histéresis → introduce memoria
- Schmitt Trigger → limpia señales
- Comparador → toma decisiones
- CD4093 → histéresis integrada
- NE555 → genera señales
- CD4017 → secuencia digital

## ejercicio en clases 
Bueno, el circuito no nos funcionó completamente. Solo logramos que encendieran las luces en las dos primeras partes del circuito; el resto no funcionó en absoluto.
![sesion06a](./imagenes/sesion06a.jpeg)
![sesion06aa](./imagenes/sesion06aa.jpeg)

