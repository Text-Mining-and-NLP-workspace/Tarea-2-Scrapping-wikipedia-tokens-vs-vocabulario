<a href="https://www.uvg.edu.gt/"><img align="left" src="https://www.uvg.edu.gt/wp-content/uploads/socialshare-logo.jpg" width="90" height="90"></a>
**_Corporate Master in Applied Data Science_**<br/>
**_Text Mining & Natural Language Processing_**<br/>
**_Catedratico: Pedro Alberto Aguilar Nuñez_**<br/>
<br/>

Integrantes:
- Aldo Montenegro Margnoni
- Gabriel Fernando Montenero Ortiz
- Axel Adolfo Muralles Carranza
- German Antonio Oliva Muralles

# Tarea 2 Scrapping wikipedia / tokens vs vocabulario

- [Descripcion](#descripcion)
- [Requerimientos](#requerimientos)
- [Instrucciones](#instrucciones)
- [Estructura del archivo de salida](#estructura-del-archivo-de-salida)
- [Descripcion del contenido del sitio web](#descripcion-del-contenido-del-sitio-web)
- [Contribuciones](#contribuciones)
- [Jupyter Notebook](#jupyter-notebook)


## Descripcion:

La tarea consiste en dos partes, la primera es el scrapping del texto de varios articulos de Wikipedia (en nuestro caso 500) para obtener un corpus de texto,
y la segunda parte en se trata del procesamiento incremental de estos textos de articulos para obtener la relacion entre la cantidad de tokens y el vocabulario.
## Requerimientos:
- Requiere instalacion de [Anaconda Distribution](https://www.anaconda.com/products/distribution) o [miniconda](https://docs.conda.io/en/latest/miniconda.html)

## Instrucciones:

clonamos este repositorio en el directorio deseado desde una terminal, para windows podemos utilizar [Git Bash](https://gitforwindows.org/) 
```
git clone https://github.com/Text-Mining-and-NLP-workspace/Scrapping-wikipedia-tokens-vs-vocabulario.git
```
Desde la terminal o anaconda prompt (windows) creamis un ambiente virtual con conda (reemplazar my_enviroment con el nombre deseado)
```
conda create -n my_enviroment
```
cuando conda pregunte por la confirmacion responder con _y_
```
proceed ([y]/n)?
```
una vez creado el ambiente virtual, proceder a activarlo
```
conda activate my_enviroment
```
instalamos los siguientes paquetes en nuestro ambiente:
```
conda install scrapy -c conda-forge
conda install pip
pip install jupyter
pip install notebook
```
nos cambiamos hacia el path en donde se clono el repositorio
```
cd Tarea-2-Scrapping-wikipedia-tokens-vs-vocabulario
```
Primero obtenemos el texto de varios articulos de wikipedia, para esto ejecutamos el siguiente comando para iniciar la spider y comenzar el scrapping
```
scrapy crawl token_VS_vocabulary
```
como salida se creara el archivo **_token_VS_vocabulary.json_** en nuestro directorio de trabajo el cual se puede procesar ya sea con el script python graph.py
```
python graph.py
```
como salida obtenermos el archivo de imagen **_token_VS_vocabulary_plot.png_** con la grafica de token VS vocabulary y la grafica del modelo utilizando la Ley de Heaps.
de igual manera se puede utilizar el notebook de jupyter [**_Token VS Vocabulary.ipynb_**](#jupyter-notebook) para procesar el archivo json y obtener las graficas deseadas
con el siguiente comando:

```
jupyter notebook "Token VS Vocabulary.ipynb"
```
para las indicaciones y descripcion ir a la seccion [Jupyter Notebook](#jupyter-notebook)


## Estructura del archivo de salida

El archivo de salida del scrapping tiene formato **json**, y consta de una coleccion de llaves  **text:** las cuales contienen en su valor el texto de un articulo de wikipedia.
<br/>
```
{
	{'text':'Este es un texto de ejemplo'} 
	...
}
```
<br/>

El archivo de salida del script graph.py es una imagen en formato png que contiene la grafica de cantidad de tokens VS vocabulario.
<img src="https://lh3.googleusercontent.com/9rWqXksk9MAw9Kf2EYW4tDWqpSpDKKRG2TxMXpr16Q1Rejhy96K36zVzjnBSd3K0wmSy3TT-DGd3nuvP4OKnGXHl4EsSh422NX7OJJvne5_WUZobeN7TwX1PtvsqkvP_Fgt_j72ZcQ=w2400" />
<br/>
## Descripcion del Contenido del sitio Web 

<a href="https://en.wikipedia.org/wiki/Wikipedia:Featured_articles"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b3/Wikipedia-logo-v2-en.svg/892px-Wikipedia-logo-v2-en.svg.png"  width="180" height="204"></a>
#### Wikipedia:Featured articles
> Featured articles are considered to be some of the best articles Wikipedia has to offer, as determined by Wikipedia's editors. They are used by editors as examples for writing other articles. Before being listed here, articles are reviewed as featured article candidates for accuracy, neutrality, completeness, and style according to our featured article criteria. Many featured articles were previously good articles (which are reviewed with a less restrictive set of criteria). There are 6,104 featured articles out of 6,510,887 articles on the English Wikipedia (about 0.09% or one out of every 1,060 articles).

## Contribuciones

- Aldo Montenegro Margnoni
    - a
<br/>

- Gabriel Fernando Montenero Ortiz
    - b
    
<br/>

- Axel Adolfo Muralles Carranza
    - c

<br/>

- German Antonio Oliva Muralles
    - d
<br/>

## Jupyter Notebook


