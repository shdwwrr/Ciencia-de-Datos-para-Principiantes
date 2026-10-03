# Visualizando Distribuciones

|![ Sketchnote por [(@sketchthedocs)](https://sketchthedocs.dev) ](../../sketchnotes/10-Visualizing-Distributions.png)|
|:---:|
| Visualizando Distribuciones - _Sketchnote por [@nitya](https://twitter.com/nitya)_ |

En la lección anterior, aprendiste algunos datos interesantes sobre un conjunto de datos acerca de las aves de Minnesota. Encontraste datos erróneos visualizando valores atípicos y observaste las diferencias entre las categorías de aves según su longitud máxima.

## [Cuestionario previo a la lección](https://ff-quizzes.netlify.app/quiz/18?loc=es)
## Explora el conjunto de datos de aves

Otra forma de analizar los datos es observando su distribución, o cómo los datos están organizados a lo largo de un eje. Tal vez, por ejemplo, te gustaría aprender sobre la distribución general, para este conjunto de datos, de la envergadura máxima o la masa corporal máxima de las aves de Minnesota.

Descubramos algunos datos sobre las distribuciones de los datos en este conjunto. En el archivo _notebook.ipynb_ en la raíz de esta carpeta de lección, importa Pandas, Matplotlib y tus datos:

```python
import pandas as pd
import matplotlib.pyplot as plt
birds = pd.read_csv('../../data/birds.csv')
birds.head()
```

|      | Nombre                       | NombreCientífico       | Categoría             | Orden        | Familia  | Género      | EstadoConservación | MinLongitud | MaxLongitud | MinMasaCorporal | MaxMasaCorporal | MinEnvergadura | MaxEnvergadura |
| ---: | :--------------------------- | :--------------------- | :-------------------- | :----------- | :------- | :---------- | :----------------- | --------:   | --------:   | ----------:     | ----------:     | ----------:    | ----------:    |
|    0 | Pato silbador vientre negro  | Dendrocygna autumnalis | Patos/Gansos/Aves acuáticas | Anseriformes | Anatidae | Dendrocygna | LC                 |        47   |        56   |         652     |        1020     |          76    |          94    |
|    1 | Pato silbador fulvo          | Dendrocygna bicolor    | Patos/Gansos/Aves acuáticas | Anseriformes | Anatidae | Dendrocygna | LC                 |        45   |        53   |         712     |        1050     |          85    |          93    |
|    2 | Ganso de las nieves          | Anser caerulescens     | Patos/Gansos/Aves acuáticas | Anseriformes | Anatidae | Anser       | LC                 |        64   |        79   |        2050     |        4050     |         135    |         165    |
|    3 | Ganso de Ross                | Anser rossii           | Patos/Gansos/Aves acuáticas | Anseriformes | Anatidae | Anser       | LC                 |      57.3   |        64   |        1066     |        1567     |         113    |         116    |
|    4 | Ganso de frente blanca mayor | Anser albifrons        | Patos/Gansos/Aves acuáticas | Anseriformes | Anatidae | Anser       | LC                 |        64   |        81   |        1930     |        3310     |         130    |         165    |

En general, puedes observar rápidamente cómo se distribuyen los datos utilizando un gráfico de dispersión como hicimos en la lección anterior:

```python
birds.plot(kind='scatter',x='MaxLength',y='Order',figsize=(12,8))

plt.title('Max Length per Order')
plt.ylabel('Order')
plt.xlabel('Max Length')

plt.show()
```
![longitud máxima por orden](../../3-Data-Visualization/10-visualization-distributions/images/scatter-wb.png)

Esto da una visión general de la distribución de la longitud corporal por Orden de aves, pero no es la forma óptima de mostrar distribuciones reales. Esa tarea generalmente se maneja creando un Histograma.

## Trabajando con histogramas

Matplotlib ofrece muy buenas formas de visualizar la distribución de datos utilizando Histogramas. Este tipo de gráfico es como un gráfico de barras donde la distribución se puede observar a través del aumento y la caída de las barras. Para construir un histograma, necesitas datos numéricos. Para construir un Histograma, puedes graficar un gráfico definiendo el tipo como 'hist' para Histograma. Este gráfico muestra la distribución de MaxBodyMass para el rango completo de datos numéricos del conjunto de datos. Dividiendo el arreglo de datos en pequeños intervalos, puede mostrar la distribución de los valores de los datos:

```python
birds['MaxBodyMass'].plot(kind = 'hist', bins = 10, figsize = (12,12))
plt.show()
```
![distribución en todo el conjunto de datos](../../3-Data-Visualization/10-visualization-distributions/images/dist1-wb.png)

Como puedes ver, la mayoría de las más de 400 aves en este conjunto de datos caen en el rango de menos de 2000 para su Masa Corporal Máxima. Obtén más información sobre los datos cambiando el parámetro `bins` a un número mayor, algo como 30:

```python
birds['MaxBodyMass'].plot(kind = 'hist', bins = 30, figsize = (12,12))
plt.show()
```
![distribución en todo el conjunto de datos con mayor parámetro de bins](../../3-Data-Visualization/10-visualization-distributions/images/dist2-wb.png)

Este gráfico muestra la distribución de manera un poco más detallada. Un gráfico menos sesgado hacia la izquierda podría crearse asegurándote de seleccionar solo datos dentro de un rango dado:

Filtra tus datos para obtener solo aquellas aves cuya masa corporal sea menor a 60, y muestra 40 `bins`:

```python
filteredBirds = birds[(birds['MaxBodyMass'] > 1) & (birds['MaxBodyMass'] < 60)]      
filteredBirds['MaxBodyMass'].plot(kind = 'hist',bins = 40,figsize = (12,12))
plt.show()     
```
![histograma filtrado](../../3-Data-Visualization/10-visualization-distributions/images/dist3-wb.png)

✅ Prueba algunos otros filtros y puntos de datos. Para ver la distribución completa de los datos, elimina el filtro `['MaxBodyMass']` para mostrar distribuciones etiquetadas.

El histograma ofrece algunas mejoras agradables de color y etiquetado para probar también:

Crea un histograma 2D para comparar la relación entre dos distribuciones. Comparemos `MaxBodyMass` vs. `MaxLength`. Matplotlib ofrece una forma integrada de mostrar convergencia utilizando colores más brillantes:

```python
x = filteredBirds['MaxBodyMass']
y = filteredBirds['MaxLength']

fig, ax = plt.subplots(tight_layout=True)
hist = ax.hist2d(x, y)
```
Parece haber una correlación esperada entre estos dos elementos a lo largo de un eje esperado, con un punto particularmente fuerte de convergencia:

![gráfico 2D](../../3-Data-Visualization/10-visualization-distributions/images/2D-wb.png)

Los histogramas funcionan bien por defecto para datos numéricos. ¿Qué pasa si necesitas ver distribuciones según datos de texto?

## Explora el conjunto de datos para distribuciones usando datos de texto 

Este conjunto de datos también incluye buena información sobre la categoría de las aves y su género, especie y familia, así como su estado de conservación. Analicemos esta información de conservación. ¿Cuál es la distribución de las aves según su estado de conservación?

> ✅ En el conjunto de datos, se utilizan varios acrónimos para describir el estado de conservación. Estos acrónimos provienen de las [Categorías de la Lista Roja de la UICN](https://www.iucnredlist.org/), una organización que cataloga el estado de las especies.
> 
> - CR: En Peligro Crítico
> - EN: En Peligro
> - EX: Extinto
> - LC: Preocupación Menor
> - NT: Casi Amenazado
> - VU: Vulnerable

Estos son valores basados en texto, por lo que necesitarás hacer una transformación para crear un histograma. Usando el dataframe filteredBirds, muestra su estado de conservación junto con su Envergadura Mínima. ¿Qué observas?

```python
x1 = filteredBirds.loc[filteredBirds.ConservationStatus=='EX', 'MinWingspan']
x2 = filteredBirds.loc[filteredBirds.ConservationStatus=='CR', 'MinWingspan']
x3 = filteredBirds.loc[filteredBirds.ConservationStatus=='EN', 'MinWingspan']
x4 = filteredBirds.loc[filteredBirds.ConservationStatus=='NT', 'MinWingspan']
x5 = filteredBirds.loc[filteredBirds.ConservationStatus=='VU', 'MinWingspan']
x6 = filteredBirds.loc[filteredBirds.ConservationStatus=='LC', 'MinWingspan']

kwargs = dict(alpha=0.5, bins=20)

plt.hist(x1, **kwargs, color='red', label='Extinct')
plt.hist(x2, **kwargs, color='orange', label='Critically Endangered')
plt.hist(x3, **kwargs, color='yellow', label='Endangered')
plt.hist(x4, **kwargs, color='green', label='Near Threatened')
plt.hist(x5, **kwargs, color='blue', label='Vulnerable')
plt.hist(x6, **kwargs, color='gray', label='Least Concern')

plt.gca().set(title='Conservation Status', ylabel='Min Wingspan')
plt.legend();
```

![envergadura y estado de conservación](../../3-Data-Visualization/10-visualization-distributions/images/histogram-conservation-wb.png)

No parece haber una buena correlación entre la envergadura mínima y el estado de conservación. Prueba otros elementos del conjunto de datos utilizando este método. También puedes probar diferentes filtros. ¿Encuentras alguna correlación?

## Gráficos de densidad

Es posible que hayas notado que los histogramas que hemos visto hasta ahora son 'escalonados' y no fluyen suavemente en un arco. Para mostrar un gráfico de densidad más suave, puedes probar un gráfico de densidad.

Para trabajar con gráficos de densidad, familiarízate con una nueva biblioteca de gráficos, [Seaborn](https://seaborn.pydata.org/generated/seaborn.kdeplot.html). 

Cargando Seaborn, prueba un gráfico de densidad básico:

```python
import seaborn as sns
import matplotlib.pyplot as plt
sns.kdeplot(filteredBirds['MinWingspan'])
plt.show()
```
![Gráfico de densidad](../../3-Data-Visualization/10-visualization-distributions/images/density1.png)

Puedes ver cómo el gráfico refleja el anterior para los datos de Envergadura Mínima; es solo un poco más suave. Según la documentación de Seaborn, "En comparación con un histograma, KDE puede producir un gráfico que es menos desordenado y más interpretable, especialmente al dibujar múltiples distribuciones. Pero tiene el potencial de introducir distorsiones si la distribución subyacente está limitada o no es suave. Al igual que un histograma, la calidad de la representación también depende de la selección de buenos parámetros de suavizado." [fuente](https://seaborn.pydata.org/generated/seaborn.kdeplot.html) En otras palabras, los valores atípicos, como siempre, harán que tus gráficos se comporten mal.

Si quisieras revisar esa línea irregular de MaxBodyMass en el segundo gráfico que construiste, podrías suavizarla muy bien recreándola usando este método:

```python
sns.kdeplot(filteredBirds['MaxBodyMass'])
plt.show()
```
![línea de masa corporal suave](../../3-Data-Visualization/10-visualization-distributions/images/density2.png)

Si quisieras una línea suave, pero no demasiado suave, edita el parámetro `bw_adjust`: 

```python
sns.kdeplot(filteredBirds['MaxBodyMass'], bw_adjust=.2)
plt.show()
```
![línea de masa corporal menos suave](../../3-Data-Visualization/10-visualization-distributions/images/density3.png)

✅ Lee sobre los parámetros disponibles para este tipo de gráfico y experimenta.

Este tipo de gráfico ofrece visualizaciones explicativas muy atractivas. Con unas pocas líneas de código, por ejemplo, puedes mostrar la densidad de masa corporal máxima por Orden de aves:

```python
sns.kdeplot(
   data=filteredBirds, x="MaxBodyMass", hue="Order",
   fill=True, common_norm=False, palette="crest",
   alpha=.5, linewidth=0,
)
```

![masa corporal por orden](../../3-Data-Visualization/10-visualization-distributions/images/density4.png)

También puedes mapear la densidad de varias variables en un solo gráfico. Prueba la MaxLength y MinLength de un ave en comparación con su estado de conservación:

```python
sns.kdeplot(data=filteredBirds, x="MinLength", y="MaxLength", hue="ConservationStatus")
```

![densidades múltiples, superpuestas](../../3-Data-Visualization/10-visualization-distributions/images/multi.png)

Tal vez valga la pena investigar si el grupo de aves 'Vulnerables' según sus longitudes es significativo o no.

## 🚀 Desafío

Los histogramas son un tipo de gráfico más sofisticado que los gráficos de dispersión, gráficos de barras o gráficos de líneas básicos. Busca en internet buenos ejemplos del uso de histogramas. ¿Cómo se utilizan, qué demuestran y en qué campos o áreas de investigación tienden a utilizarse?

## [Cuestionario posterior a la lección](https://ff-quizzes.netlify.app/quiz/19?loc=es)

## Repaso y Autoestudio

En esta lección, utilizaste Matplotlib y comenzaste a trabajar con Seaborn para mostrar gráficos más sofisticados. Investiga sobre `kdeplot` en Seaborn, una "curva de densidad de probabilidad continua en una o más dimensiones". Lee la [documentación](https://seaborn.pydata.org/generated/seaborn.kdeplot.html) para entender cómo funciona.

## Tarea

[Aplica tus habilidades](assignment.md)
