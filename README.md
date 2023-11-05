# 📊 Análisis de Datos de Jump2Digital2023: Reto "Data Science" 🚀

## Introducción 🌟

Para afrontar el reto "Data Science" de Jump2Digital 2023, opté por analizar dos datasets propuestos. Dada la ausencia de una meta específica, formulé algunas preguntas de interés que emergieron al examinar los datos proporcionados. Las preguntas que guiaron mi análisis son:

1. ¿Qué barrios son los más caros y más baratos de Barcelona?
2. ¿El ruido tiene un impacto en el precio del alquiler?
3. ¿En qué barrio se podría tener un descanso más afectado por el ruido?
4. ¿Hay una relación clara entre la cantidad de accidentes y el precio del alquiler? ¿Y sobre el ruido?
5. ¿Qué tipo de accidentes son más comunes en los distintos tipos de barrios?
6. ¿Cual es el mejor barrio para vivir dependiendo el alquiler, ruido y accidentes?

## Depuración de Datos 🧹

Para una comprensión detallada del proceso de depuración de datos, por favor, consulta el Jupyter Notebook adjunto. Hay hallazgos interesantes y pasos críticos que mejoran la calidad de nuestro análisis. Es importante ver el proceso, ya que se explica como se han conseguido los indices de ruido y accidentes.

## Resultados 📈

Gracias a una visualización efectiva, pudimos responder a nuestras preguntas iniciales. Veamos las respuestas una por una.

### Precios de Alquiler en Barcelona por Barrio 🏡💰

#### Barrios Más Caros 📈
<div align="center">

| N° | Nom_Barri                  | Preu (Euros/mes) Media |
|----|----------------------------|------------------------|
| 1  | Pedralbes                  | 901.01                 |
| 2  | les Tres Torres            | 822.02                 |
| 3  | Sarrià                     | 685.49                 |
| 4  | Sant Gervasi - Galvany     | 663.48                 |
| 5  | la Vila Olímpica del Poblenou | 632.68             |

</div>

#### Barrios Más Baratos 📉

<div align="center">

| N° | Nom_Barri          | Preu (Euros/mes) Media |
|----|--------------------|------------------------|
| 1  | Vallbona           | 153.49                 |
| 2  | Can Peguera        | 209.45                 |
| 3  | Ciutat Meridiana   | 221.80                 |
| 4  | Torre Baró         | 225.12                 |
| 5  | la Trinitat Vella  | 254.74                 |

</div>

📊 **Figura 1:** Comparativa de Precios por Barrio en Barcelona

![](figs\preciomedio.png)

El barrio más costoso es Pedralbes, mientras que Vallbona es el más accesible.

### Impacto del Ruido en el Precio del Alquiler 🌆🔊💲

📊 **Figura 2:** Correlación entre Niveles de Ruido y Precios de Alquiler

![](figs\correlacionruido.png)

Se observa que no existe una relación fuerte entre el ruido y el precio del alquiler, indicando una correlación media-baja.

### Descanso y Ruido por Barrio 😴🔊

#### Barrios con Mayor Ruido Nocturno 🌜🔊

<div align="center">

| N° | Nom_Barri                        | Índice de Sonido Nocturno |
|----|----------------------------------|---------------------------|
| 1  | l'Antiga Esquerra de l'Eixample  | 0.34                      |
| 2  | la Dreta de l'Eixample           | 0.33                      |
| 3  | la Sagrada Família               | 0.31                      |
| 4  | el Fort Pienc                    | 0.30                      |
| 5  | el Clot                          | 0.30                      |

</div>

#### Barrios con Menor Ruido Nocturno 🌜🔇

<div align="center">

| N° | Nom_Barri                              | Índice de Sonido Nocturno |
|----|----------------------------------------|---------------------------|
| 1  | Vallvidrera, el Tibidabo i les Planes | 0.11                      |
| 2  | la Font d'en Fargues                   | 0.13                      |
| 3  | Montbau                                | 0.15                      |
| 4  | Can Peguera                            | 0.16                      |
| 5  | la Marina del Prat Vermell             | 0.16                      |

</div>

📊 **Figura 3:** Índices de Ruido Nocturno por Barrio

![](figs\indiceruidonoche.png)

### Relación entre Accidentes, Ruido y Precio del Alquiler 🚗🔊💲

📊 **Figura 4:** Correlación entre Accidentes y Precios de Alquiler

![](figs\precioaccidentes.png)

📊 **Figura 5:** Correlación entre Niveles de Ruido y Precios de Alquiler

![](figs\accidentesruido.png)

#### Tipos de Accidentes Predominantes 🚑🚒🚓

📊 **Figura 6:** Tipos de Accidentes por Barrio

![](figs\mapaaccidentes.png)

#### Mejor Barrio para Vivir🌳🏙️

##### En base al ruido y los accidentes 🔈🚑

<div align="center">

| Nom_Barri                          | indice    |
|------------------------------------|-----------|
| Vallvidrera, el Tibidabo i les Planes | 0.926114 |
| la Font d'en Fargues               | 0.873708  |
| Can Peguera                        | 0.856228  |
| Montbau                            | 0.853503  |
| Can Baró                           | 0.850446  |

</div>

📊 **Figura 7:** Barrios con indice de calidad de vida (ruido y accidentes)

![](figs\noimportaalquiler.png)

##### En base el precio del alquiler, el ruido y los accidentes 💶🔈🚑

<div align="center">

| Nom_Barri         | indice   |
|-------------------|----------|
| Can Peguera       | 0.875351 |
| Vallbona          | 0.846785 |
| Torre Baró        | 0.843818 |
| Ciutat Meridiana  | 0.841999 |
| les Roquetes      | 0.839736 |

</div>

📊 **Figura 8:** Barrios con indice de calidad de vida (precio, ruido y accidentes)

![](figs\mismaimportancia.png)

## Conclusiones 📝

Este análisis nos ha permitido desentrañar información valiosa sobre los precios de alquiler en Barcelona y su relación (o falta de ella) con los niveles de ruido. Los barrios más lujosos, como Pedralbes, tienden a tener precios de alquiler más altos independientemente del ruido. Por otro lado, barrios como Vallbona se destacan por su accesibilidad en términos de costo.

Curiosamente, el ruido no parece influir significativamente en el precio del alquiler. Esto podría sugerir que otros factores, como la ubicación, el tamaño del inmueble, y las comodidades, pueden estar desempeñando roles más decisivos.

Por último, para aquellos preocupados por las noches tranquilas, barrios como Vallvidrera y la Font d'en Fargues ofrecen un retiro más silencioso en comparación con áreas más céntricas y bulliciosas como l'Antiga Esquerra de l'Eixample.

Si quieres ver el conjunto resultante procesado, puedes verlo en el archivo `alquileres.csv` dentro de la carpeta `data`.

## Recursos 📚

- [Dataset de Alquileres](https://opendata-ajuntament.barcelona.cat/data/es/dataset/est-mercat-immobiliari-lloguer-mitja-mensual/resource/0a71a12d-55fa-4a76-b816-4ee55f84d327)
- [Dataset de Ruido](https://opendata-ajuntament.barcelona.cat/data/es/dataset/poblacio-exposada-mapa-estrategic-soroll/resource/3846500e-72aa-4780-967f-f09aa184eaba)
- [Dataset de Accidentes](https://opendata-ajuntament.barcelona.cat/data/ca/dataset/accidents_causa_conductor_gu_bcn/resource/1a05cdd4-4844-41a5-872d-a0824d11b517?inner_span=True)
- [Dataset de Barrios Mapa](https://opendata-ajuntament.barcelona.cat/data/es/dataset/20170706-districtes-barris/resource/b21fa550-56ea-4f4c-9adc-b8009381896e)

## Autor ✒️

**Juan Manuel Camara Diaz** - [LinkedIn](https://www.linkedin.com/in/juanma-camara/)

## Licencia 📄

Este proyecto está bajo la Licencia (Apache License 2.0) - mira el archivo [LICENSE.md](LICENSE.md) para detalles

## Expresiones de Gratitud 🎁

Gracias a Jump2Digital por la oportunidad de participar en este reto 🤓, espero que os guste el trabajo realizado.