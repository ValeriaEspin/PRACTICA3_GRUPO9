# PRACTICA3_GRUPO9
TRABAJO GRUPAL - Heart Disease Cleveland UCI DATASET


Análisis de Enfermedad Cardíaca – Dataset Heart Disease Cleveland UCI

    Propósito del dataset

    Este proyecto tiene como objetivo explorar y analizar el dataset Heart Disease Cleveland, disponible en Kaggle, con el fin de identificar patrones y relaciones entre variables clínicas y la presencia de enfermedad cardíaca. Se busca visualizar y comprender cómo factores como edad, sexo, colesterol, frecuencia cardíaca y otros indicadores fisiológicos se asocian con el diagnóstico cardíaco.

    Dataset original: https://www.kaggle.com/datasets/cherngs/heart-disease-cleveland-uci


Limpieza y transformación de los datos

    Verificación de nulos:
    Se revisó la existencia de valores faltantes y se confirmó que el dataset no contenía valores NaN.

    Traducción de variables:
    Se tradujeron los nombres de las columnas del inglés al español para facilitar la comprensión del análisis. Por ejemplo:

        | Variable original | Nombre traducido               |
        | ----------------- | ------------------------------ |
        | `age`             | `EDAD`                         |
        | `sex`             | `GENERO`                       |
        | `cp`              | `TIPO_DOLOR_PECHO`             |
        | `trestbps`        | `PRESION_SANGUINEA`            |
        | `chol`            | `COLESTEROL`                   |
        | `fbs`             | `AZUCAR_AYUNAS`                |
        | `restecg`         | `RESULTADO_ELECTROCARDIOGRAMA` |
        | `thalach`         | `FRECUENCIA_CARDIACA`          |
        | `exang`           | `EJERCICIO_ANGINA`             |
        | `oldpeak`         | `CAMBIOS_ST_EJERCICIO`         |
        | `slope`           | `INCLINACION_ST_EJERCICIO`     |
        | `ca`              | `VASOS_CORONARIOS`             |
        | `thal`            | `FLUJO_CARDIACO`               |
        | `condition`       | `ENFERMEDAD_CORAZON`           |


Mapeo de variables categóricas: En el código se documenta el significado de los valores de variables, para asegurar su interpretación.

Estandarización de nombres: Todas las variables se renombraron en mayúsculas y con guiones bajos para uniformidad.


Principales hallazgos del análisis - Gráficos

1. Distribución de edad según presencia de enfermedad cardíaca
    Gráfico utilizado: Violin plot

El análisis muestra que las personas con enfermedad cardíaca tienden a concentrarse en un rango de edad ligeramente mayor (cercano a los 60 años). Aunque existe solapamiento entre los grupos, la distribución de quienes no presentan enfermedad es más dispersa.

2. Condición cardíaca según sexo
    Gráfico utilizado: Gráfico de barras agrupadas (countplot)

Se observó que la presencia de enfermedad cardíaca es mayor en hombres (112 casos) frente a mujeres (25 casos). En el grupo femenino, predomina la ausencia de enfermedad. Esto sugiere una posible relación entre el sexo masculino y la enfermedad cardíaca en este conjunto de datos.

3. Relación entre colesterol y edad según diagnóstico
    Gráfico utilizado: Gráfico de dispersión (scatter plot)

No se detectó una relación clara entre los niveles de colesterol y la edad. Ambos grupos, con y sin enfermedad, presentan una distribución similar. Algunos individuos con colesterol moderado también presentan enfermedad cardíaca.

***Hallazgo clave: El colesterol no discrimina efectivamente entre pacientes sanos y enfermos.

4. Mapa de correlación entre variables fisiológicas
    Gráfico utilizado: Heatmap (mapa de calor)

El mapa de calor permitió visualizar la relación entre cinco variables fisiológicas: edad, presión sanguínea, colesterol, frecuencia cardíaca máxima y cambios en el segmento ST inducidos por ejercicio. Se analizaron los coeficientes de correlación de Pearson, que varían entre –1 (relación inversa perfecta) y +1 (relación directa perfecta).

Interpretación de las principales correlaciones:

    Edad y frecuencia cardíaca máxima: correlación negativa moderada (–0.39). Esto indica que, a mayor edad, las personas tienden a alcanzar frecuencias cardíacas máximas más bajas, lo cual es fisiológicamente esperable.

    Frecuencia cardíaca máxima y cambios en el ST: correlación negativa (–0.35). Es decir, quienes alcanzan mayor frecuencia cardíaca durante el ejercicio tienden a presentar menor depresión del segmento ST, lo que puede asociarse a un mejor estado cardiovascular.

    Edad con presión arterial y colesterol: correlaciones positivas débiles (entre 0.19 y 0.25), lo que sugiere que, en este conjunto de datos, el aumento de la edad se asocia ligeramente con valores más altos de estos indicadores, aunque sin fuerza significativa.

    Colesterol y presión sanguínea: la correlación entre estas variables y el resto fue muy baja (cercana a 0), lo que indica ausencia de relación lineal clara entre ellas en este grupo de personas.

    ***Hallazgo clave: Las correlaciones más relevantes se dan entre edad, frecuencia cardíaca y respuesta al ejercicio, lo que sugiere que estas variables podrían ser mejores indicadores del riesgo cardiovascular que otras como colesterol o presión sanguínea, al menos dentro de este dataset.



Conclusiones

        *Edad y sexo son los factores más visiblemente asociados con la presencia de enfermedad cardíaca. En el dataset analizado, la enfermedad es más común en personas mayores y en hombres.

        *El colesterol y la presión arterial, si bien son variables clínicamente relevantes, no muestran correlaciones fuertes ni patrones visuales claros con la condición cardíaca en este análisis.

        *La frecuencia cardíaca máxima alcanzada y los cambios en el segmento ST inducidos por ejercicio mostraron correlaciones inversas con la edad y entre sí, lo que sugiere que podrían ser indicadores más sensibles del estado cardiovascular frente al esfuerzo físico.

        *Las visualizaciones permitieron identificar tendencias importantes, pero también confirmaron que ninguna *variable aislada es completamente determinante, por lo que el diagnóstico de enfermedad cardíaca debe considerar múltiples factores combinados.

        *Este análisis exploratorio sienta las bases para futuros estudios predictivos, modelos de clasificación y sistemas de apoyo al diagnóstico en entornos clínicos.