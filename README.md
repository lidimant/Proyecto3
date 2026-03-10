##Proyecto 3 – Análisis de Datos de Intrusiones en Red - archivo data_analisis.ipynb
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

###1. Carga del dataset

Los archivos CSV fueron cargados utilizando la librería pandas, que permite manipular grandes volúmenes de datos de forma eficiente.

###2. Limpieza de nombres de columnas

Se realizó una normalización de los nombres de columnas eliminando espacios innecesarios para evitar errores durante el análisis.

###3. Creación de la variable de clasificación

Se generó una nueva variable llamada attack, donde:

0 representa tráfico benigno

1 representa tráfico asociado a ataques

Esto permite transformar el problema en una tarea de clasificación binaria, útil para modelos de machine learning.

###4. Eliminación de valores problemáticos

Se identificaron y eliminaron valores:

infinitos

valores nulos

Estos valores pueden afectar el análisis estadístico y el entrenamiento de modelos de aprendizaje automático.

###5. Exploración de variables

Se realizaron análisis descriptivos y visualizaciones para observar la distribución de variables relacionadas con características del tráfico de red, especialmente aquellas relacionadas con el tamaño y comportamiento de los paquetes.

Se utilizaron gráficos como boxplots para comparar el comportamiento de ciertas variables entre tráfico benigno y tráfico malicioso.

##Principales hallazgos del análisis

A partir del análisis exploratorio se identificaron varios patrones relevantes en el comportamiento del tráfico de red:

Algunas variables relacionadas con la longitud de paquetes presentan diferencias significativas entre tráfico benigno y tráfico de ataque.

Las distribuciones de ciertas métricas de red muestran mayor variabilidad en flujos asociados a ataques.

Los valores extremos (outliers) son más frecuentes en registros asociados a actividad maliciosa, lo cual puede ser útil para identificar comportamientos anómalos.

Las variables relacionadas con la duración del flujo y la cantidad de paquetes también muestran diferencias importantes entre los distintos tipos de tráfico.

##Insights y conclusiones

El análisis exploratorio del dataset permite identificar características del tráfico de red que pueden ser útiles para la detección automática de intrusiones.

Entre los principales insights obtenidos se destacan:

Existen patrones claros en algunas variables que permiten diferenciar tráfico benigno de tráfico malicioso.

La limpieza de datos es un paso fundamental antes de realizar cualquier análisis o entrenamiento de modelos.

La transformación de la variable de etiqueta en una variable binaria facilita la aplicación de algoritmos de clasificación.

Este análisis constituye un paso preliminar importante para el desarrollo de modelos de machine learning orientados a la detección de intrusiones en redes informáticas.

##Estructura del repositorio
Proyecto3
│
├── data_analisis.ipynb   # Notebook con el análisis de datos
└── README.md             # Documentación del proyecto
