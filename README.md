# Who is that Avenger

Este proyecto es una aplicacion de algoritmos de **machine learning** diseñado para identificar personajes de la pelicula Avengers, a través de puntos clave de sus rostros. Este proyecto se basa en el uso de diferentes técnicas y tecnologías:

## Librerias usadas
* **Python**
* **NumPy**
* **OpenCV**
* **scikit-learn**
* **LIME**
* **face_recognition**

## Tecnicas usadas

### Detección de bounding box de un rostro

Este proyecto usa la librería `face_recognition` la cual entrega un arreglo que delimita una bounding box que contiene un rostro encontrado. Con esto y a traves del metodo `get_landmarks` de esta misma libreria, se pueden encontrar las coordenadas de puntos clave de la cara como la posicion de la nariz, de los ojos, mejillas, etc.

### Extracción de características 

De los lankmarks detectados, se extraen ciertas caracteristicas, tales como las distancias o razones entre ciertos puntos. 

### Modelos usados

Se usaron varios modelos de machine learning de `sklearn`:

* **SVM**
* **DecisionTreeClassifier**
* **GaussianNB**
* **RandomForestClassifier**
* **KNeighborsClassifier**
* **GradientBoostingClassifier**

### Hiperparámetros
Para la selección de hiperparámetros óptimos se usó `GridSearchCV` con validación cruzada.

### Interpretabilidad de modelos y resultados

Para interpretar y dar explicabilidad a las features o seleccion de clases, se uso `LIME`.

### Resultados

1. Random Forest (69%)
2. Gradient Boosting (65%)
3. Arboles de decision (55%)
4. SVM (51%)
5. KNN (42%)




