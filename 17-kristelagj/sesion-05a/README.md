# sesion-05a
## Clase clase 070426

### clase

- Misaa

Hoy se nos presentó que realizaremos de primera entrega: un sintetizador

**¿Qué es un sintentizador:** es un instrumento musical electrónico que genera, modifica y manipula señales eléctricas para producir sonido artificialmente. A diferencia de los instrumentos acústicos, crea timbres desde cero mediante osciladores y circuitos (analógicos o digitales), permitiendo imitar instrumentos reales o diseñar sonidos totalmente nuevos.

**Oscilador:** tomar un gesto para que sea suficientemente amigable

**VCV RACK:** es un sintetizador modular virtual de código abierto y gratuito que emula el funcionamiento de sistemas hardware tipo Eurorack en tu ordenador. Permite crear sonidos complejos conectando virtualmente módulos (osciladores, filtros, efectos) mediante cables. Es ideal para aprender síntesis, diseñar sonidos y crear música sin coste inicial.

![vcv rack](imagenes/vcv-rack.jpg)

| Sigla | Nombre completo                          | Descripción                                                                 | Función principal                          | Parámetro controlado     |
|-------|------------------------------------------|-----------------------------------------------------------------------------|--------------------------------------------|--------------------------|
| VCA   | Amplificador Controlado por Voltaje      | Ajusta la ganancia de una señal de audio según un voltaje externo          | Controlar el volumen/amplitud              | Ganancia (amplitud)      |
| VCF   | Filtro Controlado por Voltaje            | Moldea el timbre del sonido filtrando frecuencias                          | Filtrar armónicos de la señal              | Frecuencia de corte      |
| VCO   | Oscilador Controlado por Tensión         | Genera señales periódicas cuya frecuencia depende del voltaje de entrada   | Generar la señal base (onda)               | Frecuencia (pitch)       |

Salida de VCO

![vco](imagenes/vco.png)

![RUIDO](imagenes/ruido.jpg)

RITMO Y FRECUENCIA ES LO MISMO

-Compuertas Lógicas AND, OR Y NOT

**AND:** la luz prende solo si ambos están encendidos (da 1 cuando todas las entradas son 1)
**OR:** la luz prende si uno o ambos están encendidos (Da 1 cuando al menos una entrada es 1)
**NOT:** si el interruptor está apagado, la salida se comporta como encendido (invertido) (invierte el valor de entrada) 

## Compuerta AND (Y)
| A | B | Salida |
|---|---|--------|
| 0 | 0 |   0    |
| 0 | 1 |   0    |
| 1 | 0 |   0    |
| 1 | 1 |   1    |

## Compuerta OR (O)
| A | B | Salida |
|---|---|--------|
| 0 | 0 |   0    |
| 0 | 1 |   1    |
| 1 | 0 |   1    |
| 1 | 1 |   1    |

## Compuerta NOT (NO)
| A | Salida |
|---|--------|
| 0 |   1    |
| 1 |   0    |

1 significa nivel alto (HIGH) y 0 nivel bajo (LOW). Tambien podria ser 1 es que se entrega voltaje y 0 no se entrega voltaje, osea inactivo. 

![compuertas](imagenes/compuertas-logicas.jpg)


### imagenes de proceso

### post-clase

Quiero ser sincera ante lo que es el taller y me he sentido muy desanimada. Al principio estaba muy entusiasmada, conversé con los profes de cómo me sentía, pero siento que me estoy quedando muy atrás. Lo cual no me motiva ni a subir la bitácora. 

Si me preguntaran puedo rescatar algo, que he podido entender un poco, por ejemplo, lo que hace mi padre, entender algo de audio, diferenciar un condensador polarizado y el que no, pero no puedo explicarte algo de como funciona o que hace realmente. Llego a clases sólo escuchando y no entendiendo nada a pesar de siempre estar preguntando. 
