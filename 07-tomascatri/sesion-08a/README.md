# sesion-08a

Lunes 28 de Abril

## Apuntes
* Instalamos KiCad (en el apunte anterior explico qué es).
* Una vez instalado, debemos seguir estos pasos:
1) Dibujar esquemático (.kicad_sch).
2) Asociar huellas a símbolos.
3) Abrir PCBNew (para crear la PCB), intérprete del esquemático.
4) Definir tamaño de las pistas.
5) Repartir componentes físicamente.
6) Rutear componentes.
7) Ornamentar y exportar para fabricación.
* Probablemente tenga que crear/descargar mis huellas y símbolos.
* Winterbloom: Empresa que hacía sintetizadores con KiCad; todo era de código abierto. Creó plugins para cambiar cómo se veía KiCad; por así decirlo, hacía "skins" para KiCad.
* Theacodes: Creó un visualizador de esquemas de manera web.
* En esta clase realizamos los primeros 3 pasos.

## Cómo usar KiCad
* Al abrir KiCad, tenemos que darle a "Nuevo proyecto"; ahí se nos crearán 2 archivos nuevos.
* Tenemos que abrir el archivo .sch o, en otras palabras, el esquemático.
 
![MenuKiCad](./imagenes/archivo.png)
  
* Una vez abierto, los atajos para poner todos los componentes y cosas útiles para navegar por KiCad son:
1) Tecla A: Poner componentes; se debe navegar por la barra abierta por esta tecla para seleccionar el componente.
2) Tecla W: Pone el cableado del esquema; con eso se conecta todo.
3) Tecla Esc: Con esta volvemos al modo de ratón o al modo de selección.
4) Con el pad, juntando los dos dedos y moviéndolos arriba o abajo, se puede hacer zoom al esquemático.
5) Con el pad, juntando los dos dedos y moviéndolos de derecha a izquierda, se puede mover de manera horizontal por el esquemático.
6) Tecla T: Con esta puedes poner los textos.
7) Tecla Retroceso: Con esta eliminas componentes (de manera nativa es otro botón, pero yo puse ese para mayor comodidad; si alguien lee esto, puede cambiarlo en Preferencias y después en Atajos).

### Primer paso
* El primer paso será identificar cada uno de los componentes que usaremos para el esquemático e ir colocándolos.

![Componentes](./imagenes/componentes-usados.png)
  
* Una vez colocados los necesarios, se deberán poner sus correspondientes textos en la parte de abajo; esto se logra teniendo el modo selección y dándole doble clic. Ahí se pueden poner los textos que uno estime conveniente, aunque es súper recomendado que se ponga igual al valor del componente que usaremos.


![Batera antes y despues](./imagenes/ejemplo-bateria.png)

* Dicho esto, quedaría conectar todo a los componentes.

![Esquematico](./imagenes/esquematico.png)

* En este caso, que esté conectado a dos 555, con la finalidad de hacer un Atari Punk Console.
* Ya conectado todo, debemos pasar al segundo paso.

### Segundo paso
* Para empezar, tenemos que entender qué es la huella (footprint).
* Por lo que entendí yo, para pasar del diseño a la realidad, es obligatorio vincular cada símbolo del esquema con el componente físico que vamos a soldar en la placa. En otras palabras: qué componente de la vida real usaremos para representar el del esquemático.
* La opción de huella se encuentra en la barra superior de herramientas.

![Ubicacion de huella](./imagenes/lugar-huella.png)


* Dejaré acá los componentes con sus nombres:

![Lista de componentes](./imagenes/lista-componentes-con-huella.png)

* Con esto listo, pasaremos al tercer paso.

### Tercer paso
* Para este paso necesitamos abrir el archivo PCB desde KiCad o desde la barra de herramientas superior.
* Una vez en el archivo PCB, presionamos F8 para añadir todos los componentes a la placa; hecho esto, ya tendremos los componentes.
* Presionando ALT + 3 entraremos al modo 3D y, al hacerlo, nos daremos cuenta de que la placa es demasiado grande en comparación con nuestros componentes, por lo que debemos reducir su tamaño.
* Para esto debemos crear un cuadrado (1) que encierre a nuestros componentes y a la zona a delimitar (2). Vamos a la ventana de capas y seleccionamos que esté en "Edge.Cuts" (4); esto se logra presionando dos veces el cuadrado.

![Delimitar cuadrado](./imagenes/delimitar-espacio.png)

* Por ahora quedaría de esta manera:

![Placa 3D](./imagenes/placa-3d.png)

* EXTRA: Para añadir imágenes SVG hay que darle a Archivo, Importar y Gráfico, en ese orden. Luego seleccionar la capa F.Silkscreen si queremos que el diseño se muestre en la placa.
