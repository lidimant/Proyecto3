## Proyecto 3 – Análisis de Datos de Intrusiones en Red - archivo data_analisis.ipynb 
Descripción del dataset

Este proyecto realiza un análisis exploratorio de un conjunto de datos de tráfico de red utilizado para la detección de intrusiones. El dataset contiene información sobre flujos de red capturados en diferentes condiciones de operación, incluyendo tráfico normal (benigno) y tráfico asociado a distintos tipos de ataques.

Cada registro del dataset representa una conexión o flujo de red y contiene múltiples variables relacionadas con características del tráfico, tales como:

Puertos de origen y destino

Duración del flujo de red

Número de paquetes enviados y recibidos

Longitud de paquetes

Estadísticas de actividad e inactividad

Etiqueta de clasificación del tráfico (benigno o ataque)

Este tipo de dataset es ampliamente utilizado en estudios de ciberseguridad y sistemas de detección de intrusiones (IDS), ya que permite analizar patrones de comportamiento del tráfico y diferenciar entre actividad legítima y potencialmente maliciosa.

##Limpieza y transformación de datos

Antes de realizar el análisis, se aplicaron varios pasos de limpieza y transformación para garantizar la calidad y consistencia de los datos.

### 1. Carga del dataset

Los archivos CSV fueron cargados utilizando la librería pandas, que permite manipular grandes volúmenes de datos de forma eficiente.

### 2. Limpieza de nombres de columnas

Se realizó una normalización de los nombres de columnas eliminando espacios innecesarios para evitar errores durante el análisis.

### 3. Creación de la variable de clasificación

Se generó una nueva variable llamada attack, donde:

0 representa tráfico benigno

1 representa tráfico asociado a ataques

Esto permite transformar el problema en una tarea de clasificación binaria, útil para modelos de machine learning.

### 4. Eliminación de valores problemáticos

Se identificaron y eliminaron valores:

infinitos

valores nulos

Estos valores pueden afectar el análisis estadístico y el entrenamiento de modelos de aprendizaje automático.

### 5. Exploración de variables

Se realizaron análisis descriptivos y visualizaciones para observar la distribución de variables relacionadas con características del tráfico de red, especialmente aquellas relacionadas con el tamaño y comportamiento de los paquetes.

Se utilizaron gráficos como boxplots para comparar el comportamiento de ciertas variables entre tráfico benigno y tráfico malicioso.

## Principales hallazgos del análisis

A partir del análisis exploratorio se identificaron varios patrones relevantes en el comportamiento del tráfico de red:

Algunas variables relacionadas con la longitud de paquetes presentan diferencias significativas entre tráfico benigno y tráfico de ataque.

Las distribuciones de ciertas métricas de red muestran mayor variabilidad en flujos asociados a ataques.

Los valores extremos (outliers) son más frecuentes en registros asociados a actividad maliciosa, lo cual puede ser útil para identificar comportamientos anómalos.

Las variables relacionadas con la duración del flujo y la cantidad de paquetes también muestran diferencias importantes entre los distintos tipos de tráfico.

## Insights y conclusiones

El análisis exploratorio del dataset permite identificar características del tráfico de red que pueden ser útiles para la detección automática de intrusiones.

Entre los principales insights obtenidos se destacan:

Existen patrones claros en algunas variables que permiten diferenciar tráfico benigno de tráfico malicioso.

La limpieza de datos es un paso fundamental antes de realizar cualquier análisis o entrenamiento de modelos.

La transformación de la variable de etiqueta en una variable binaria facilita la aplicación de algoritmos de clasificación.

Este análisis constituye un paso preliminar importante para el desarrollo de modelos de machine learning orientados a la detección de intrusiones en redes informáticas.




### Proyecto 3 – Análisis de Datos para Detección de Intrusiones en Red
## Descripción del propósito del dataset

Este proyecto tiene como objetivo analizar un conjunto de datos de tráfico de red con el fin de identificar patrones asociados a actividades benignas y posibles intrusiones. El dataset contiene múltiples variables que describen características de las conexiones de red, tales como duración del flujo, número de paquetes transmitidos, tamaño de paquetes y otras métricas relacionadas con el comportamiento del tráfico.

El propósito principal del dataset es apoyar el análisis y desarrollo de sistemas de detección de intrusiones (Intrusion Detection Systems – IDS). Estos sistemas permiten identificar actividades sospechosas o ataques dentro de una red informática mediante el análisis de patrones de tráfico.

Cada registro del dataset representa una conexión o flujo de red y contiene múltiples atributos que permiten caracterizar el comportamiento del tráfico. Además, se incluye una etiqueta que clasifica el tráfico como benigno (normal) o ataque, lo cual permite realizar análisis comparativos entre ambos tipos de comportamiento.

Los datasets de intrusiones son ampliamente utilizados en investigaciones de ciberseguridad para entrenar modelos capaces de reconocer patrones de ataques y detectar anomalías en el tráfico de red.

## Explicación de los pasos de limpieza y transformación

Antes de realizar el análisis exploratorio de los datos, se ejecutaron varios procesos de limpieza y preparación del dataset para garantizar la calidad de la información.

## 1. Carga del dataset

El dataset fue cargado en el entorno de Google Colab utilizando Python y librerías especializadas en análisis de datos.

Las principales librerías utilizadas fueron pandas para manipulación de datos, NumPy para operaciones numéricas, Matplotlib y Seaborn para visualización de datos

## 2. Limpieza de los nombres de columnas

Se realizó una normalización de los nombres de columnas para eliminar espacios innecesarios o caracteres inconsistentes que podían generar errores durante el análisis.

Esto permitió acceder a las variables del dataset de manera consistente dentro del código.

## 3. Creación de una variable de clasificación

Se creó una nueva variable denominada attack, con el objetivo de simplificar la clasificación del tráfico de red.

0: tráfico benigno

1: tráfico asociado a ataque

Esto permitió transformar el problema en una clasificación binaria, lo cual facilita el análisis exploratorio y la posterior aplicación de algoritmos de aprendizaje automático.

## 4. Tratamiento de valores nulos e infinitos

Durante el análisis se identificaron valores problemáticos dentro del dataset, como valores infinitos y valores nulos

Estos valores fueron eliminados o tratados adecuadamente para evitar distorsiones en el análisis estadístico y en las visualizaciones.

## 5. Exploración de variables relevantes

Se analizaron variables relacionadas con el comportamiento del tráfico de red, especialmente aquellas asociadas a longitud de paquetes y número de paquetes transmitidos, duración del flujo de red

estadísticas de actividad e inactividad

Para analizar la distribución de estas variables se utilizaron gráficos como boxplots, los cuales permiten comparar el comportamiento de las variables entre tráfico benigno y tráfico malicioso.

## Principales hallazgos del análisis

A partir del análisis exploratorio de los datos se identificaron varios patrones relevantes en el comportamiento del tráfico de red.

Entre los principales hallazgos destacan las diferencias en la distribución de variables, algunas variables relacionadas con la longitud y cantidad de paquetes presentan diferencias notables entre el tráfico benigno y el tráfico asociado a ataques, Presencia de valores extremos

Se observaron valores extremos (outliers) en algunas variables del dataset, especialmente en registros asociados a tráfico malicioso.

## Variabilidad en el comportamiento del tráfico

El tráfico asociado a ataques tiende a presentar mayor variabilidad en ciertas métricas de red, lo que puede ser un indicador de comportamiento anómalo dentro del sistema.

## Conclusiones

El análisis exploratorio del dataset permitió identificar características relevantes del tráfico de red que pueden utilizarse para la detección de intrusiones.

Entre las principales conclusiones se destacan que existen patrones diferenciables entre tráfico benigno y tráfico malicioso, la limpieza y preparación de los datos es un paso fundamental antes de realizar cualquier análisis o entrenamiento de modelos.

Algunas variables del dataset presentan un alto potencial para ser utilizadas como características en modelos de machine learning orientados a la detección de ataques.

La visualización de datos facilita la identificación de patrones y anomalías dentro del tráfico de red.
