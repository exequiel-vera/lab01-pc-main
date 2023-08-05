![Logo UCN](images/60x60-ucn-negro.png)
# Laboratorio 01: Cálculo de frecuencia peatonal 


## 1. Introducción 

El estudio del flujo de personas en espacios unidireccionales podría tratarse de un tema fundamental para la planificación urbana y la gestión de multitudes ya que entender cómo se mueven las personas podría garantizar la seguridad, eficiencia y comodidad en diversos escenarios. En este informe, se presenta la primera parte del desarrollo para abordar el dicho problema, con los datos recopilados, los cuales contienen las coordenadas en metros que describen la ruta seguida por las personas, las cuales serán transformadas posteriormente a píxeles, lo que permitirá calcular una matriz de frecuencia que represente la ruta seguida por las personas en términos de píxeles.

### 1.1 Justificación 

En situaciones como evacuaciones de emergencia, eventos deportivos o festivales musicales se requieren de una planificación cuidadosa que garantice la seguridad de las personas. La transformación de las coordenadas (X, Y) a píxeles es esencial para cuantificar y analizar de manera más precisa el recorrido de estas ya que con ello se puede construir una matriz de frecuencia con la cual se pueden implementar mapas de calor y así visualizar los patrones de densidad, dado que cada píxel representa una unidad de área y su intensidad de color se correlaciona con la magnitud de los datos en esa ubicación por lo que se mostraran aquellas áreas más transitadas, facilitando la identificación de áreas críticas que requieran intervenciones específicas.

### 1.3 Objetivos 

**Objetivo general**

Calcular una matriz de frecuencia representada en píxeles de la ruta que siguen las personas en un pasillo unidireccional, con el fin de identificar las áreas más transitadas.

**Objetivos específicos**

1. Cargar los datos de las coordenadas (x, y) que describen la ruta seguida por las personas
2. Transformar los datos de coordenadas, que se encuentran en formato de texto (string), a valores numéricos (float).
3. Convertir las coordenadas (x, y) en valores de metros a píxeles, aplicando una transformación adecuada según la escala del espacio representado.

## 2. Marco teórico 

Python: Es un lenguaje de programación de alto nivel. Presenta una sintaxis clara y legible. Es un lenguaje versátil que se utiliza en una amplia variedad de aplicaciones.

Visual Studio Code (VSCode): Editor de código fuente desarrollado por Microsoft.  Admite una variedad de lenguajes de programación, incluido Python, y proporciona funciones útiles como resaltado de sintaxis, autocompletado y depuración integrada.

NumPy: Es una biblioteca de Python ampliamente utilizada para realizar cálculos numéricos y operaciones con matrices y matrices multidimensionales. Introduce un objeto de matriz multidimensional llamado numpy.array, que permite realizar operaciones eficientes en grandes conjuntos de datos.

Funciones en Python: Son bloques de código reutilizable que permiten dividir tareas complejas en tareas más pequeñas y manejables. Una función toma uno o más argumentos de entrada, realiza ciertas operaciones y devuelve un resultado o realiza una acción específica.

## 3. Materiales y métodos

El dataset utilizado en el laboratorio es un archivo de texto descargado de “Pedestrian Dynamics Data Archive”, fue denominado 'Pea.txt', que contiene datos de coordenadas (x, y, z) que describen la ruta seguida por las personas en el corredor unidireccional. Cada línea del archivo representa una ruta individual con sus respectivas coordenadas.

El tamaño del dataset dependerá de la cantidad de rutas registradas en el archivo 'Pea.txt', y corresponderá al número de líneas presentes en el archivo, en este caso fueron 25.536. El tipo de datos del archivo son representados en formato de texto (string) para las coordenadas (x, y, z). Durante el proceso de lectura y manipulación, estos datos son transformados a valores numéricos (float) para poder realizar cálculos y operaciones matemáticas.

Descripción del Experimento:
El experimento consiste en analizar el flujo de personas en un pasillo unidireccional mediante el análisis de datos de coordenadas (x, y) proporcionados en el archivo 'Pea.txt'. Durante el proceso del laboratorio, se llevan a cabo diferentes operaciones como la lectura del archivo, la transformación de datos de texto a valores numéricos, la creación de matrices y diccionarios para el conteo de frecuencias y la identificación de los valores más repetidos. Esto tiene como objetivo principal obtener información sobre las coordenadas más frecuentes en las rutas de las personas, lo que permitirá identificar áreas de mayor concentración. 

Secuencia de Pasos:
El laboratorio se enfoca en analizar el flujo de personas en un corredor unidireccional mediante el uso del archivo 'Pea.txt', que contiene las coordenadas de las rutas seguidas por las personas. La secuencia de pasos en el laboratorio es la siguiente:
Se inicia con la lectura del archivo y creación de una lista de coordenadas, donde se abre el archivo 'Pea.txt' y se lee línea por línea y se separan las coordenadas (x, y, z) para almacenarlas en la lista 'matriz' y luego en las listas 'Coordenadas_X', 'Coordenadas_Y' y 'Coordenadas_Z'. Posteriormente, se utilizan funciones para contar la frecuencia de aparición de cada valor de las coordenadas X, Y y Z. Los resultados se almacenan en los diccionarios 'frecuencia_X', 'frecuencia_Y' y 'frecuencia_Z', además se vuelven a utilizar funciones para encontrar el valor que más se repite en las coordenadas X, Y y Z, y se almacenan en las variables 'valor_x_mas_repetido', 'valor_y_mas_repetido' y 'valor_z_mas_repetido', junto con sus frecuencias correspondientes y se repiten estos pasos para contar la frecuencia de aparición de cada par de coordenadas (X, Y) combinadas, almacenándolo en el diccionario 'frecuencia_XY' y encontrar el par de coordenadas que más se repite y se almacena en la variable 'valor_xy_mas_repetido', junto con su frecuencia correspondiente.
Una vez terminada esa parte, se calculan las pendientes (Mx y My) para convertir las coordenadas de metros a píxeles y las coordenadas de píxel resultantes se almacenan en el diccionario 'FrecCoordPixel'. Finalmente, se debe encontrar la coordenada X, Y que más se repite en píxel y se almacena en la lista 'XYPixel_mas_repetida', junto con su frecuencia 'max_frecuenciaPixelXY'.

## 4. Resultados obtenidos


|        Coordenadas       |  N° de frecuencia   |  
|--------------------------|---------------------|
| x = 0.3181               |                   4 |                         
| y = 2.988                |                   6 |  
| x,y = (-2.2467, 2.937)   |                   2 |
 
Tabla 1: **Mayores frecuencias de coordenadas**



## 5. Conclusiones

Apartir de los resultados inferir nuevo conocimiento. Por ejemplo, al ultilizar concatenación de listas cono "+" el programa es menos eficiente en términos de tiempo que utilizar 'append()'.





