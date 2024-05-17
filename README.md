# 1. Análisis Colisiones de Vehículos en New York
El proyecto se fundamenta en el dataset **Motor_Vehicle_Collisions_-_Crashes.csv**. Obtenido de [Data.gov](https://catalog.data.gov/dataset/motor-vehicle-collisions-crashes) 

---

## 1.1. Resumen del dataset

La tabla de accidentes de colisiones de vehículos motorizados, contiene detalles sobre el evento del accidente vial. Cada fila representa un evento de accidente. Las tablas de datos de colisiones de vehículos motorizados contienen información de todas las colisiones de vehículos motorizados reportadas por la policía en la ciudad de Nueva York

A continuación una breve descripción de las variables:
    
| Campo | Descripción | Tipo de dato |
| :--- | :--- |:--- |
|FECHA DEL ACCIDENTE| Fecha de ocurrencia de la colisión| date time|
|TIEMPO DE CHOQUE|Hora de ocurrencia de la colisión|date time|
|CIUDAD|Municipio donde ocurrió la colisión|texto sin formato|
|CÓDIGO POSTAL|Código postal donde ocurrió el incidente|texto sin formato|
|LATITUD|Coordenada de latitud-Sistema de Coordenadas Global (EPSG 4326)|Numérico|
|LONGITUD|Coordenada de longitud-Sistema Global de Coordenadas (EPSG 4326)|Numérico|
|UBICACIÓN|Par de latitud y longitud|texto sin formato|
|NOMBRE DE LA CALLE|Calle en la que ocurrió la colisión.|Texto sin formato|
|NOMBRE DEL CRUCE DE CALLES|Cruce de calles más cercano al lugar de la colisión|Texto sin formato|
|NOMBRE FUERA DE LA CALLE|Dirección si se conoce|Texto sin formato|
|NÚMERO DE PERSONAS HERIDAS|Número de personas heridas en la colisión vial|Numérico|
|NÚMERO DE PERSONAS MUERTAS|Número de personas muertos en la colisión vial|Numérico|
|NÚMERO DE PEATONES HERIDOS|Número de peatones heridos en la colisión vial|Numérico|
|NÚMERO DE PEATONES MUERTOS|Número de peatones muertos en la colisión vial|Numérico|
|NÚMERO DE CICLISTAS HERIDOS|Número de ciclistas heridos en la colisión vial|Numérico|
|NÚMERO DE CICLISTAS MUERTOS|Número de ciclistas muestos en la colisión vial|Numérico|
|NÚMERO DE MOTORISTAS HERIDOS|Número de motociclistas heridos en la colisión vial|Numérico|
|NÚMERO DE MOTORISTAS MUERTOS|Número de motociclistas muertos en la colisión vial|Numérico|
|FACTOR CONTRIBUYENTE VEHÍCULO 1|Factores que contribuyen a la colisión del vehículo designado|Texto sin formato|
|FACTOR CONTRIBUYENTE VEHÍCULO 2|Factores que contribuyen a la colisión del vehículo designado|Texto sin formato|
|FACTOR CONTRIBUYENTE VEHÍCULO 3|Factores que contribuyen a la colisión del vehículo designado|Texto sin formato|
|FACTOR CONTRIBUYENTE VEHÍCULO 4|Factores que contribuyen a la colisión del vehículo designado|Texto sin formato|
|FACTOR CONTRIBUYENTE VEHÍCULO 5|Factores que contribuyen a la colisión del vehículo designado|Texto sin formato|
|ID DE LA COLISIÓN|Código de registro único generado por el sistema|Numérico|
|CÓDIGO DE TIPO DE VEHÍCULO 1|Tipo de vehículo según la categoría de vehículo seleccionada|Texto sin formato|
|CÓDIGO DE TIPO DE VEHÍCULO 2|Tipo de vehículo según la categoría de vehículo seleccionada|Texto sin formato|
|CÓDIGO DE TIPO DE VEHÍCULO 3|Tipo de vehículo según la categoría de vehículo seleccionada|Texto sin formato|
|CÓDIGO DE TIPO DE VEHÍCULO 4|Tipo de vehículo según la categoría de vehículo seleccionada|Texto sin formato|
|CÓDIGO DE TIPO DE VEHÍCULO 5|Tipo de vehículo según la categoría de vehículo seleccionada|Texto sin formato|

---

# 2. Objetivo del proyecto:
Predecir la cantidad de víctimas fatales en una colisión vehícular en la ciudad de New York, dadas ciertas condiciones como ubicación y factores contribuyentes a los accidentes viales

---

# 3. Pasos Iniciales para la ejecución del Notebook del proyecto:

## 3.1 Carga del dataset
### Para realizar la carga del dataset es necesario realizar los siguientes pasos:

#### A. Iniciar la ejecución de las librerías en la sección `B. Carga de Librerías` del notebook [`ME03-G17-[1020418701].ipynb`](https://github.com/n-upegui/UdeA_EAyCD-Seminario/blob/main/momentos_evaluativos/ME03-G17-%5B1020418701%5D.ipynb) para genrar primer paso de acceso al Google Drive

#### B. Iniciar la ejecución de la sección `1. Carga de los datos` del notebook para realizar la descarga y montaje del dataset [Motor_Vehicle_Collisions_-_Crashes.csv](https://catalog.data.gov/dataset/motor-vehicle-collisions-crashes)

#### Paso 1: 
* Al ejecutar la primera celda se generará la siguiente ventana emergente, en esta ventana se debe dar clic en permitir.

<img src="https://github.com/n-upegui/UdeA_EAyCD-Seminario/blob/main/image/Paso_1.png" style="height: 60%; width:60%;"/></a>

#### Paso 2: 
* Al dar clic en permitir se generará la siguiente ventana emergente, en esta ventana se debe dar clic en la cuenta de gmail con la que se va a generar el permiso de acceso a Google Colaboratory.

<img src="https://github.com/n-upegui/UdeA_EAyCD-Seminario/blob/main/image/Paso_2.png" style="height: 60%; width:60%;"/></a>

#### Paso 3: 
* Presionar en continuar.

<img src="https://github.com/n-upegui/UdeA_EAyCD-Seminario/blob/main/image/Paso_3.png" style="height: 60%; width:60%;"/></a>

#### Paso 4: 
* Seleccionar al menos la primera opción de ver, modificar, crear y eliminar archivos de Google Drive, o se puede seleccionar todo.

<img src="https://github.com/n-upegui/UdeA_EAyCD-Seminario/blob/main/image/Paso_4.png" style="height: 60%; width:60%;"/></a>

#### Paso 5: 
* Dar clic en continuar.

<img src="https://github.com/n-upegui/UdeA_EAyCD-Seminario/blob/main/image/Paso_5.png" style="height: 60%; width:60%;"/></a>

Con lo anterior se iniciará la descarga del dataset [*Motor_Vehicle_Collisions_-_Crashes.csv*](https://catalog.data.gov/dataset/motor-vehicle-collisions-crashes) en el entorno de Google Colaboratory

#### C. Iniciar la escritura del dataset al entorno de Colab, al ejecutar la segunda celda de código de la sección `1. Carga de los datos`, se cargará automáticamente el archivo `.csv` en la sección de archivos, pudiendo así leer el dataset normalmente con el nombre del archivo.

#### D. Al ejecutar la tercera celda de código de la sección `1. Carga de los datos`, se toma un fragmento del 0.1% `(2087 registros)` del dataset completo, para facilitar la ejecución del entorno y probar los resultados de los diferentes procesos de ejecución del proyecto.
---
#### Al ejecutar lo descrito anteriormente ya se podrán ejecutar las celdas de código de las secciones posteriores del notebook:

2. Análisis exploratorio de los datos,

3. Preparación de los datos,

4. Creación de datasets** `(Entrenamiento y Testeo)`, y

5. Análisis descriptivo avanzado.
     
---

# 4. Análisis y descripción inicial del Proyecto:
Como se mencionó en el **numeral 2** del presente documento. Para el proyecto se plantea realizar un modelo de regresión con el fin de establecer una predicción $(\hat{y})$ de la cantidad de víctimas fatales en una colisión vehícular en la ciudad de New York. para este modelo se plantean como variables predictoras $(X)$ factores que contribuyeron a la colisión vial, la ubicación del evento y el tipo de vehículo.

---

# 5. Descripción de las actividades de análisis exploratorio:
Se evalúan los problemas más comunes que se encuentran dentro de un dataset, que son: registros nulos y cadenas de caracteres vacíos ("Espacios"). Y se muestran los valores únicos para cada variable, con el fin de encontrar problemas que requieran tratamiento.

* Para el dataset, se encuentra que se tienen 18 variables `object-("Categóricas")`, 4 variables `float64-(Coma flotante)` y 7 variables `int64-(Enteros)`
* En el dataset se evidencia la existencia de muchos valores nulos para las variables que involucran más de 3 vehículos en accidentes viales, dado que es más raro que haya una colisión con más de tres vehículos involucrados.
* Se validan que no existen valores duplicados en el dataset, ya que no aportarían información veráz al modelo, porque al tener accidentes viales repetidos se generarían eventos puntuales que la contabilizarse varias veces estaría sesgando el comportamiento de cada accidente individual

Tomando en consideración los resultados obtenidos en la exploración inicial de los datos se decide realizar los siguientes tratamientos a los datos:

* transformar las columnas `'CRASH DATE'` y `'CRASH TIME'` de `string` a `datetime`.
* Eliminar los espacios en blanco de la variable `'ZIP CODE'` y transformarla en `float64`
* Rellenar los valores faltantes de las variables `'NUMBER OF PERSONS INJURED'` y `'NUMBER OF PERSONS KILLED'` con cero $(0)$ dado que eran muy pocos los valores que se encontraban como `NaN` y dado que el tener los espacios vacíos podía indicar que no se presentaron muertes en esos accidentes viales.
* Por último se transforman las variables anteriores (`'NUMBER OF PERSONS INJURED'` y `'NUMBER OF PERSONS KILLED'`) en `int64` dado que no se pueden presentar muertes de personas en decimales (no existe media muerte)

---

# 6. Descripción y creación de los datasets para el modelo de regresión:
Se utiliza la librería [`sklearn.model_selection`](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html) para dividir los datos en partes de Entrenamiento y Testeo para la variable predictora $(X)$ como para la variable respuesta $(y)$.

* Dada la cantidad de los datos se utiliza una división de 70% para `train`y 30% para `test` (esto ya que con una cantidad de 2.086.527 registros el 70% podría ser suficiente para entrenar el modelo y con un 30% realizar el testeo)
* Se utiliza un random_state para que no haya variación entre cada ejecución del Notebook y se pueda mantener el valor de la respuesta del modelo
* Se utiliza una mezcla aleatoria inicial para garantizar que si existe un ordenamiento de los datos por alguna razón, estos no afecten las divisiones de `train` y `test`

---

# 7. Análisis de los resultados del proyecto:
Al analizar el comportamiento de los datos con las variables categóricas, se puede inferir lo siguiente:

* Las ciudades que más cuentan con registros de accidentes son Brooklin y Queens
* Para el análisis de los factores que contribuyen a la colisión está como mayoritario el registro `no especificado` que no aporta información al modelo, pero siguen los valores de `desatención/distracción del conductor`, `no ceder el paso` y `no respetar la distancia entre vehículos`. Que ***podrían*** aportar al análisis de los resultados y a las predicciones del modelo.

Se evalúa el comportamiento de las variables numéricas y se obtiene el siguiente resultado:

* Al parecer existe una aparente correlación positiva entre las variables `'NUMBER OF MOTORIST INJURED'` y `'NUMBER OF PERSONS INJURED'` lo que se podría explicar dado que un accidente en motocicleta hay una muy alta probabilidad de que el conductor salga lastimado, lo que no se ve por ejemplo con vehículos con mayor protección tales como carros, camionestas, buses, etc.
* Las demás variables parecen no tener un comportamiento relacional para el modelo, dado que no presentan tendencias identificables a simple vista.
* Al realizar una matriz de correlación entre las variables numéricas, se logra identificar que la aparente correlación entre las variables `'NUMBER OF MOTORIST INJURED'` y `'NUMBER OF PERSONS INJURED'` si tiene un comportamiento lineal positivo dada la correlación de un 88% entre ambas variables.

Para el desarrollo del proyecto, con el ánimo de realizar un reconocimiento visual del comportamiento de los accidentes viales en la ciudad de Nueva York, se optó por validar los casos de `personas muertas en accidentes viales`e intentar comprender si existe un patrón de comportamiento de atropellamientos mortales en algún sector específico de la ciudad.

Con los datos que se tomaron para este ejemplo, se ve que los accidentes viales tienen una pequeña aglomeración en el área sur de Manhattan (cerca al área empresarial) y central park. Pero sería necesario analizar este comportamiento con los datos completos para validar la hipótesis, aunque podría ser un comportamiento acertado dada la alta afluencia de personas y vehículos en dicha área.

---

# 8. Referencias:

* [Base de Datos: *Motor Vehicle Collisions - Crashes*](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95/about_data)
*  [Librería Scikit-Learn: sklearn.model_selection.train_test_split](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html)

* [Notebooks](https://colab.research.google.com/drive/1-dI12bCSAgWu6lfzVkViedtJva21fQK7)
Autor: [David Villanueva Valdes](mailto:david.villanueva@udea.edu.co)
    * ACT02 Towards Data Monography.ipynb

* [Notebooks](https://drive.google.com/drive/folders/1jmjSNu9xSOjExauNBp-no3wEep0OtQLl)
Autor: [Jorge Bedoya](mailto:jabedoyap79@gmail.com)
    * 00_PreparaciónDataset01Regresion.ipynb
    * 02_RegresionLineal.ipynb
    * 03_RegresionLineal(2da Parte).ipynb

---

## Integrante del Proyecto:
Nelson Fabián Ramírez Upegui - C.C: 1.020.418.701 - [![Gmail](https://img.shields.io/badge/Gmail-nelson.ramirez1@udea.edu.co-026937?style=for-the-badge&logo=gmail&logoColor=white&labelColor=EA4335)](mailto:nelson.ramirez1@udea.edu.co)
