# sesion-08a  
28 de Abril

Llegué muy tarde ups... trabajamos en Kicad por primera vez  
***recordar: traer coyacs para prestar atención***  

FALTA: Terminar esquemáticos, revisar la cápsula de la clase, subir capturas y lo que se vio en el archivo de Kicad

## Componentes (nombres en librería)  
- Resistencias → `R` / `Device:R`  
- Capacitores:
  - `C` → no polarizado  
  - `CP` → polarizado  
- Potenciómetro → `R_Potentiometer` (valor ej: 100k)  
- Batería → `Device:Battery` (valor: 9V)  
- Parlante → `Device:Speaker`  
- LED → `LED`

---

## Footprints (tipos físicos)  
- Capacitor cerámico → `Disc` (no polarizado)   
- Capacitor electrolítico → `Radial` (polarizado)  
- Resistencia → `Axial` (ej: DIN0207)  
- LED → `LED_D5.0mm`  
- Potenciómetro → tipo panel (ej: Alps)

---

## Dimensiones y estándares  
Atención con la búsqueda y uso de componentes, hay que prestar especial atención a las dimensiones físicas de uno. En general no es necesario buscar componentes con capacidades de voltaje demasiado altas (perdida de plata, mejor quedarse con lo necesario. A menos que...)

Para encontrar dimensiones exactas, recomendación práctica:

1. Usar footprint de KiCad
2. Leer sus dimensiones
3. Solo si es crítico → confirmar con datasheet  
Ejemplo:  
- *resistor 1/4W datasheet*

- Los fabricantes usan **estándares comunes** → DIN, JEDEC, EIA  
Ejemplo:  
- `DIN0207` → resistencia axial típica (~1/4W)

**Parámetros:**  
- `L` → largo  
- `D` → diámetro  
- `P` → pitch (distancia entre patas)

---

## Conceptos clave  
- `P (pitch)` = distancia entre patas  
- Un mismo componente puede tener distintas huellas  
- En asignación de huellas:
  - se puede copiar/pegar → mismo componente, distinta huella

---

## Capacitores  
- Polarizado → electrolítico (`CP`)  
- No polarizado → cerámico (`C`)  

**nota:** `µ` (micro) y `n` (nano) **NO indican polaridad**, solo unidad  

  - µF = microfaradios  
  - nF = nanofaradios  

---

## Conexiones en esquemático
- `●` → conexión real  
- cruce sin punto → conexión  
- `▢` → punto de edición (no conexión)

---

## Capas PCB 
(7) Capas principales en PCB de 2 capas:

- `F.Cu` / `B.Cu` → cobre  
- `F.SilkS` / `B.SilkS` → serigrafía  
- `F.Mask` / `B.Mask` → máscara de soldadura  
- `Edge.Cuts` → borde de la placa  

- Son las capas básicas más usadas en el curso.

---

## Edición / visualización
- Propiedades de texto → `E` o doble clic  
- Render PCB → `Alt + 3`

---

## Edición PCB
- Cambiar dimensiones del borde:  
  - seleccionar borde → `E`

---

## Guardado de proyecto  
- Guardar desde `.kicad_pro`  
- Contiene:  
  - esquemático  
  - PCB  
  - config general  

---

## Notas
- las resistencias más largas → dependen de estándar (ej: DIN0207, DIN0309)  
- los fabricantes usan las mismas dimensiones (estandarización industrial)

---

# !!!!!! Por revisar / corroborar

1. **“que el filtro corresponda a la librería de la izquierda”**  

2. **Dimensiones exactas de resistencias “largas”**  

3. **Asignación de huellas (copiar/pegar)**  
   → importante: 
   - solo válido si el componente físico es equivalente  
   - no siempre intercambiable (ej: radial vs axial)



