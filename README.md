# MAESTRÍA EN CIENCIA DE DATOS Y ANALÍTICA<br>
## ST1800 ALMACENAMIENTO Y RECUPERACIÓN DE INFORMACIÓN<br>
## CASO DE ESTUDIO - PROCESAMIENTO DE DATASET DE NOTICIAS<br>

### Integrantes del Equipo
- Danny Styvens Cardona Pineda
- Alirio Rodríguez Mesías
## Actividades
1.	Realizar el entendimiento de los datos <br>
2.	Especificar los retos o casos de negocio sobre los datos<br>
  i.	Realizar indexación (solo en META) <br>
  ii.	Realizar búsqueda y recuperación (Solo en META)<br>
  iii.	Modelado de tópicos (en SparkML o AWS comprehend o META)<br>
  iv.	Análisis de sentimientos (en SparkML o AWS comprehend)<br>
  v.	Agrupamiento (en SparkML o AWS comprehend)<br>

## Estructura de Archivos y directorios
Para dar cumplimiento a las actividades propuestas se tienen los siguientes archivos:

### 1. Entendimiento de los datos
- *analisis_descriptivo_news.ipynb* <br>
En  este Jupyter Notebbok se tienen las instrucciones del pre-procesamiento de la información, que incluye:
   - Carga de los datos <br>
   - Limpieza de registros con datos nulos  <br>
   - Contabilización de palabras inicial<br>
   - Remoción de stopwords<br>
 
 ### 2. Implementación de Casos de Negocios
*indexacion_busqueda_metapy* <br>
Tiene la implementación de la indexación del dataset completo de news.csv y del proceso de búsqueda de noticias a partir de unos términos de una consulta (query).<br>
Para esto se tienen:
- En el directorio data, están dos subdirectorios:<br>
   - news: que contiene el dataset completo de noticias<br>
   - mini-news: un selección de las primeras 20.000 noticias del dataset, que se debieron de utilizar, dado la limitada capacidad del procesamiento del servidor que se tuvo disponible. 

*modelado_topicos_news_using_pyspark.ipynbk*
Para este archivo sólo se procesaron 20.000 noticias del dataset, y aplicando el algoritmo de LDA se realizó una clasificación no supervisada de las noticas en diez tópicos.

*agrupamientos_articulos_pyspar.ipynbk*
Para este archivo sólo se procesaron 20.000 noticias del dataset, y aplicando el algoritmo de K-means se realizó una clasificación no supervisada de las noticas en diez grupos. El resultado final está en un archivo denominado clustertable_news.csv.

*analisis_sentimientos_news_using_pyspark.ipynb*
Para este archivo sólo se procesaron 20.000 noticias del dataset, y aplicando el algoritmo de SentimentIntensityAnalyzer de NLTK se realizó una clasificación de cómo se califica cada noticia(Negativa, Neutra o Positiva)

