# README - Análisis de Predicción de Salario Utilizando Árboles de Decisión y Random Forest
Este proyecto tiene como objetivo predecir el salario de los empleados en función de su experiencia laboral y edad utilizando dos modelos de aprendizaje automático: Árbol de Decisión y Random Forest. El propósito principal es evaluar el desempeño de ambos modelos a través de diversas métricas y determinar cuál de ellos es más eficaz para predecir los salarios. A continuación, se describe el flujo general del código y su propósito.

## Propósito del Código
El propósito de este código es construir, entrenar y evaluar dos modelos de predicción: Árbol de Decisión y Random Forest. Los modelos se entrenan utilizando dos variables predictoras, YearsExperience y Age, para predecir la variable objetivo Salary. El rendimiento de ambos modelos se evalúa mediante métricas como el Error Absoluto Medio (MAE), Error Cuadrático Medio (MSE), Raíz del Error Cuadrático Medio (RMSE) y el Coeficiente de Determinación.

## Descripción del Código
1. Carga y Preprocesamiento de Datos
El código comienza cargando el archivo Salary_Data.csv que contiene los datos de entrada. El archivo incluye tres columnas:
YearsExperience: Años de experiencia laboral del empleado.
Age: Edad del empleado.
Salary: Salario anual del empleado.
Una vez cargado el archivo, se realiza un preprocesamiento básico para separar las filas en pares e impares, y luego se reorganizan y se guardan en un nuevo archivo CSV llamado datos_salary.csv.

2. División de los Datos
El conjunto de datos es dividido en un conjunto de entrenamiento y un conjunto de prueba utilizando train_test_split de sklearn. El conjunto de entrenamiento (80% de los datos) se utiliza para entrenar los modelos, mientras que el conjunto de prueba (20% de los datos) se usa para evaluar su rendimiento.

3. Creación y Entrenamiento de Modelos
El código entrena dos modelos de predicción:
Árbol de Decisión: Utiliza el DecisionTreeRegressor de sklearn.
Random Forest: Utiliza el RandomForestRegressor de sklearn.
Ambos modelos son entrenados utilizando el conjunto de entrenamiento.

4. Evaluación de los Modelos
Una vez que los modelos han sido entrenados, se utilizan para predecir los salarios en el conjunto de prueba. Las predicciones se comparan con los valores reales de los salarios para calcular varias métricas de rendimiento:
Error Absoluto Medio (MAE): Mide el error promedio entre los valores predichos y los valores reales.
Error Cuadrático Medio (MSE): Mide el error cuadrático promedio, penalizando más los errores grandes.
Raíz del Error Cuadrático Medio (RMSE): La raíz cuadrada del MSE, que da una medida del error en las mismas unidades que la variable objetivo.
Coeficiente de Determinación R^2 Mide el porcentaje de la variabilidad en los salarios que es explicado por el modelo.

6. Análisis y Visualización
El código también genera gráficos para comparar las predicciones de los modelos con los valores reales de los salarios. Esto se realiza mediante un gráfico de dispersión que compara los valores reales frente a los valores predichos, y una línea ideal que representa la relación perfecta entre ellos.

7. Interpretación de Resultados
Los resultados de las métricas de evaluación se analizan para comparar el rendimiento de los modelos. En este caso:

Random Forest obtuvo un R^2 de 0.9608, lo que indica que el modelo es capaz de predecir el salario con una alta precisión, explicando más del 96% de la variabilidad en los datos.
Árbol de Decisión, aunque también eficiente, mostró un  R^2 de 0.8355, lo que sugiere que el modelo no captura tan bien las relaciones en los datos como el modelo de Random Forest.
Además, el código también puede evaluar la importancia de las características para entender qué variables tienen un mayor impacto en la predicción de los salarios.


Este análisis proporciona una base sólida para predecir salarios en función de la experiencia y la edad, lo que puede ser útil para la toma de decisiones en recursos humanos, políticas salariales, y la planificación organizacional.

## Requisitos del Proyecto
Para ejecutar este código, necesitarás las siguientes bibliotecas:
-numpy
-pandas
-matplotlib
-seaborn
-sklearn
