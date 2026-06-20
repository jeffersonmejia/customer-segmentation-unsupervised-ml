# Segmentación de clientes con K-Means

## Tabla de contenido

- [1. Resumen](#1-resumen)
- [2. Metodología](#2-metodología)
- [3. Ejecución en Google Colab](#3-ejecución-en-google-colab)

## 1. Resumen

El presente proyecto analiza la segmentación de clientes mediante el algoritmo K-Means, una técnica de aprendizaje no supervisado. Se identifican grupos de clientes con características similares a partir de las variables edad, ingreso mensual y gasto mensual.

El cuaderno `P2TareaKNN_MejiaJefferson.ipynb` utiliza datos sintéticos con fines académicos y presenta los segmentos, centroides y perfiles promedio obtenidos. La interpretación de los resultados se realiza después de la ejecución completa del cuaderno.

## 2. Metodología

Se aplica **K-Means**, un algoritmo de *clustering* que agrupa observaciones similares sin etiquetas previas. El cuaderno implementa el siguiente proceso:

1. Se generan 120 clientes sintéticos con cuatro perfiles de edad, ingreso y gasto.
2. Se estandarizan las tres variables con `StandardScaler`.
3. Se ajustan modelos K-Means para valores de `k` entre 2 y 6.
4. Se calcula la inercia de cada modelo y se representa el método del codo.
5. Se obtiene `k_optimo` mediante la distancia máxima de cada punto a la recta entre los extremos de la curva.
6. Se ajusta el modelo final con `k_optimo`, `n_init=20` y `random_state=42`.
7. Se transforman los centroides a la escala original y se muestran los clusters según edad y gasto mensual.

## 3. Ejecución en Google Colab

1. Se abre [Google Colab](https://colab.research.google.com/).
2. Se selecciona **Archivo > Subir cuaderno**.
3. Se carga `P2TareaKNN_MejiaJefferson.ipynb`.
4. Se ejecutan las celdas en orden.

No se requiere instalación manual: Google Colab incluye NumPy, Pandas, Matplotlib y scikit-learn.
