
#  Detección de Ataques DoS con IA (HistGradientBoostingClassifier)

## Objetivo

[cite\_start]Desarrollo y optimización de un clasificador para detectar ataques de **Denegación de Servicio (DoS)** utilizando el modelo **HistGradientBoostingClassifier (HGB)** de `scikit-learn`[cite: 15, 39].

[cite\_start]El enfoque principal fue la **optimización progresiva de hiperparámetros** con *early stopping* y **validación cruzada** para lograr un modelo generalizado y estable[cite: 16, 64, 68].

-----

## 💻 Metodología

1.  [cite\_start]**Preparación de Datos**: Limpieza y transformación de un dataset orgánico de tráfico de red (conversión de etiquetas a binario, eliminación de columnas no numéricas, tratamiento de nulos)[cite: 18, 20, 25, 29, 31].
2.  [cite\_start]**Modelo Base**: Entrenamiento inicial con HGB, que mostró sobreentrenamiento (métricas $>$ 0.999)[cite: 60, 61].
3.  [cite\_start]**Optimización**: Aplicación de un algoritmo automatizado para encontrar la configuración óptima (bajo complejidad y **`learning_rate`** bajo)[cite: 62, 75, 82, 83].

-----

## 📈 Resultados Finales

El modelo optimizado alcanzó un equilibrio ideal entre precisión y *recall* (tasa de detección), consolidándose como una herramienta efectiva:

| Métrica | Valor Final | Observación Clave |
| :--- | :--- | :--- |
| **Accuracy** | [cite\_start]0.9776 [cite: 106] | |
| **F1-Score** | [cite\_start]0.9720 [cite: 106] | Alto equilibrio. |
| **PR-AUC** | [cite\_start]0.9950 [cite: 106] | Excelente rendimiento en clases desbalanceadas. |
| **Recall (Tasa de Detección)** | [cite\_start]$>$ 99% [cite: 110] | [cite\_start]Muy baja cantidad de Falsos Negativos (solo 44)[cite: 109]. |

### Configuración Óptima:

```python
HistGradientBoostingClassifier(
    max_depth=3,
    max_leaf_nodes=7,
    min_samples_leaf=5,
    l2_regularization=0.0,
    learning_rate=0.03
[cite_start]) [cite: 77, 78, 79, 80, 82]
```

-----

## 🔗 Recursos

  * [cite\_start]**Código**: `Untitled1.ipynb` [cite: 121]
  * [cite\_start]**Video Presentación**: `VideoCACIC2025.mkv` [cite: 123]
