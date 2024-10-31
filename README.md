# Análisis de Modelos Predictivos

Este proyecto incluye tres modelos predictivos aplicados a diferentes conjuntos de datos: regresión lineal, regresión logística y árbol de decisión. A continuación, se presenta un resumen del análisis de cada modelo.

## 1. Regresión Lineal

**Conjunto de Datos:** El modelo se aplicó a un dataset que contiene información sobre precios de vehículos, incluyendo diversas características.
**R-cuadrado: 0.960**, indicando que el modelo explica el 96% de la variabilidad en los precios.
**Significancia de Variables:**
- Model_encoding y Year son altamente significativos (p < 0.001), sugiriendo su fuerte influencia en el precio.
- Kilometer tiene un efecto negativo significativo, donde un aumento en el kilometraje reduce el precio.
- Variables Insignificantes: id_Make, Transmission_Manual, id_Owner, y id_Fuel_Type no mostraron significancia estadística, sugiriendo que podrían eliminarse para simplificar el modelo.
**Problemas Detectados:** Un alto número de condición indica posible multicolinealidad. La normalidad de los residuos no se cumplió, lo que puede requerir un ajuste adicional.

## 2. Regresión Logística
**Conjunto de Datos:** Se utilizó el dataset de Heart Disease Cleveland UCI para predecir la presencia de enfermedad cardíaca.
**Precisión del Modelo:** 0.79, mostrando que el modelo tiene un desempeño moderado.
**Matriz de Confusión:**
- Verdaderos Positivos: 34 (Enfermedad) y 37 (No Enfermedad).
- Falsos Negativos: 8 (Enfermedad) y 11 (No Enfermedad).
**Reporte de Clasificación:**
- F1-score: 0.78 para la clase 1 (enfermedad) y 0.80 para la clase 0 (sin enfermedad), indicando un buen equilibrio entre precisión y exhaustividad.

**Conclusión:** El modelo es eficaz en la predicción de enfermedades cardíacas, con un rendimiento equilibrado en ambas clases.

## 3. Árbol de Decisión
**Conjunto de Datos:** Se aplicó un árbol de decisión al dataset de calidad de vino, que contiene 10 clases de calidad.
**Precisión del Modelo:** 0.573, lo que sugiere que el modelo tiene un desempeño limitado en la clasificación de calidad de vino.
**Matriz de Confusión:**
Presenta confusiones significativas entre varias clases, con un alto número de predicciones incorrectas.
**Reporte de Clasificación:**
- F1-score: Bajo para clases como 3 y 4, lo que indica que el modelo tiene dificultades para predecir estas clases.

**Conclusión:** Aunque el árbol de decisión es fácil de interpretar, su capacidad predictiva en este caso es limitada. Se sugiere la optimización del modelo o la exploración de otros algoritmos de clasificación.

## Conclusiones Generales
La regresión lineal muestra un excelente ajuste para el conjunto de datos de precios de vehículos, aunque se deben abordar problemas de multicolinealidad.
La regresión logística es efectiva en la predicción de enfermedades cardíacas, con una precisión razonable y un buen balance entre las clases.
El árbol de decisión tiene un rendimiento insatisfactorio en la clasificación de calidad de vino, lo que sugiere la necesidad de ajustes o la consideración de otros enfoques.
