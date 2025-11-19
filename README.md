# proyecto-regresion

Integrantes: Mauro Fernandez, Tomás Caceres, Tomas Zucchi. 

# Predicción de Precios de Casas con Regresión Lineal Múltiple

## Descripción del proyecto
Este proyecto implementa un modelo de Regresión Lineal Múltiple para predecir el precio de casas a partir de un conjunto de características específicas.  
El objetivo es analizar el desempeño del modelo, identificar las variables más influyentes y evaluar la capacidad de generalización a nuevos datos.



## Tecnologías utilizadas
- Python
- Pandas  
- Scikit-Learn  
- Numpy  
- Matplotlib



## Features utilizadas
Las características elegidas para entrenar el modelo fueron:

- pies_cuadrados_casa  
- num_banios  
- num_habitaciones  
- num_cocinas  
- num_coches_garaje  
- pies_cuadrados_garaje

## Desempeño del modelo

### Métricas principales

| Métrica                         | Entrenamiento | Test     | Interpretación                                                 |
|-------------------------------- |--------------|---------- |----------------------------------------------------------------|
| R²                              | 0.72          | 0.70     | El modelo explica ~72-70% de la variabilidad del precio        |
| MAE (Error Absoluto Medio)      | $26,429       | $26,429  | Desviación promedio de las predicciones respecto al valor real |
| Median Absolute Error           | $20,600       | $20,950  | Error típico de predicción, menos afectado por valores extremos|
| MSE (Error Cuadrático Medio)    | -             | -        | Valores grandes pero similares → sin sobreajuste               |

La cercanía entre entrenamiento y test indica que el modelo generaliza bien y no está sobreajustado.

## Variables más influyentes

| Variable               | Coeficiente (USD)  | Interpretación                 |
|------------------------|--------------------|--------------------------------|
| Número de baños         | 18,950.72         | Incremento positivo del precio |
| Número de coches garaje | 10,470.65         | Incremento positivo del precio |
| Pies cuadrados casa     | 82.35             | Incremento positivo del precio |
| Pies cuadrados garaje   | 62.61             | Incremento positivo del precio |
| Número de cocinas       | -14,532.83        | Efecto negativo relativo       |
| Número de habitaciones  | -50,229.29        | Efecto negativo relativo       |

Los valores negativos reflejan que, considerando todas las demás variables, estas características tienen un efecto inverso sobre el precio. No indican error en el modelo.

## Evaluación de las features

- Las features elegidas lograron un buen desempeño, pero podrían mejorarse incluyendo información adicional como:
  - Años de antigüedad de la propiedad  
  - Ubicación (zona, barrio)  
  - Barrio privado o no  

## Conclusión

- El modelo es estable y generaliza bien.  
- Las predicciones son razonablemente precisas considerando las features utilizadas.  
- Las variables más influyentes son número de baños y coches en garaje, mientras que algunas presentan efectos negativos relativos según el dataset.
