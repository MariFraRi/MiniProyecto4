# Clasificación de Préstamos con Random Forest en PySpark

Este proyecto aplica **modelos de clasificación supervisada** usando **Random Forest** en **PySpark** para predecir el **incumplimiento de préstamos**, a partir de un dataset con información financiera y crediticia de los clientes.  
Además, se incluyen comparaciones con **scikit-learn** y un análisis de interpretabilidad con **LIME**, con el fin de entender las decisiones del modelo.

---

## Objetivo general
1. Construir un pipeline de preprocesamiento y clasificación usando `RandomForestClassifier` en PySpark.  
2. Evaluar el desempeño del modelo con métricas estándar (accuracy, precision, recall, f1, AUC).  
3. Comparar resultados y tiempos de cómputo entre PySpark y scikit-learn.  
4. Analizar la interpretabilidad del modelo mediante explicaciones locales con **LIME**.  

---

## Contexto aplicado
La predicción de **incumplimiento de créditos** es fundamental para entidades financieras, ya que permite:  
- Reducir riesgos en la colocación de préstamos.  
- Identificar clientes con mayor probabilidad de incumplir.  
- Mejorar la toma de decisiones con modelos interpretables.  

El uso de PySpark facilita la escalabilidad en entornos con **grandes volúmenes de datos**, mientras que la comparación con scikit-learn muestra las diferencias en **rendimiento y tiempo de cómputo**.  
Finalmente, con **LIME** se busca dotar al modelo de transparencia, explicando las contribuciones de cada variable en predicciones específicas.

---

## Dataset utilizado
- Fuente: Dataset de créditos (columna `label`: 1 = incumple, 0 = no incumple).  
- Número de registros: ~1000 (en la muestra procesada).  
- Variables principales:  
  - **Demográficas**: edad, historial crediticio.  
  - **Financieras**: ingresos, monto del préstamo, tasa de interés.  
  - **Crediticias**: score FICO, número de cuentas abiertas, deudas previas.  
- Variable objetivo:  
  - `label` (1 = incumple, 0 = no incumple).  

---

## Diseño del notebook
1. **Carga y análisis exploratorio del dataset** (EDA).  
2. **Preprocesamiento y partición train/test** evitando *data leakage*.  
3. **Entrenamiento con Random Forest en PySpark**.  
4. **Comparación con scikit-learn** en métricas y tiempos.  
5. **Interpretabilidad con LIME** para explicar decisiones del modelo.  
6. **Evaluación de resultados y visualizaciones** (matriz de confusión, curva ROC).  
7. **Reflexión crítica y conclusiones**.  
