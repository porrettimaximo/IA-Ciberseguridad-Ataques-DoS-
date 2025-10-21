
#  Detección de Ataques DoS con IA 

## Objetivo

Desarrollo y optimización de un clasificador para detectar ataques de **Denegación de Servicio (DoS)** utilizando el modelo **HistGradientBoostingClassifier (HGB)** de `scikit-learn`.

El enfoque principal fue la **optimización progresiva de hiperparámetros** con *early stopping* y **validación cruzada** para lograr un modelo generalizado y estable.

-----

##  Metodología

1.  **Preparación de Datos**: Limpieza y transformación de un dataset orgánico de tráfico de red (conversión de etiquetas a binario, eliminación de columnas no numéricas, tratamiento de nulos).
2.  **Modelo Base**: Entrenamiento inicial con HGB, que mostró sobreentrenamiento (métricas $>$ 0.999).
3.  **Optimización**: Aplicación de un algoritmo automatizado para encontrar la configuración óptima (bajo complejidad y **`learning_rate`** bajo).

-----

##  Resultados Finales

El modelo optimizado alcanzó un equilibrio ideal entre precisión y *recall* (tasa de detección), consolidándose como una herramienta efectiva:

| Métrica | Valor Final | Observación Clave |
| :--- | :--- | :--- |
| **Accuracy** | 0.9776  | |
| **F1-Score** | 0.9720  | Alto equilibrio. |
| **PR-AUC** | 0.9950  | Excelente rendimiento en clases desbalanceadas. |
| **Recall (Tasa de Detección)** | $>$ 99% | Muy baja cantidad de Falsos Negativos (solo 44). |


##  Recursos
[Link a Documentacion](https://drive.google.com/file/d/1v1TZR4N2b63n8rSsKH-PfGIrVwnRaQnS/view?usp=sharing)
