# TelecomX - Parte 2

Este repositorio contiene el análisis, procesamiento de datos y modelado predictivo para el proyecto **TelecomX**, enfocado en predecir la tasa de abandono de clientes (*Churn*).

## Contenido
- Limpieza y normalización de datos.
- Análisis exploratorio de datos (EDA).
- Modelos de predicción (Regresión Logística, Árboles, Random Forest, etc.).
- Comparación de métricas (Accuracy, Precision, Recall, F1-Score, ROC-AUC).

## Herramientas utilizadas
- Python 3
- Google Colab
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn

## Ejecución
Para correr este proyecto en Google Colab:
1. Clona este repositorio.
2. Abre el notebook `.ipynb` en Google Colab.
3. Ejecuta las celdas en orden.

## Conclusiones del Análisis de Churn

Distribución de la variable objetivo
El conjunto de datos inicial mostraba que aproximadamente el 26,5% de los clientes habían cancelado el servicio (churn = 1) y el 73,5% lo mantenían (churn = 0). Esto evidenció un claro desbalance de clases, lo que nos llevó a considerar técnicas como SMOTE para equilibrar el conjunto y mejorar el rendimiento de los modelos.

Modelos evaluados

Regresión Logística (con normalización): obtuvo un ROC-AUC de 0.83, con un buen desempeño en recall para clientes que cancelaron (0.80), lo que la hace útil para detectar casos de churn, aunque con menor precisión (0.49) en esta clase.

Random Forest (sin normalización): alcanzó un ROC-AUC de 0.81 y un mejor equilibrio entre precisión y recall para ambas clases, con una exactitud global del 78%. Resultó más robusto en la predicción de clientes que permanecen.

Variables más relevantes

En Regresión Logística, las variables con mayor influencia positiva en la probabilidad de churn fueron account_charges_total, internet_internetservice y account_paperlessbilling. La antigüedad del cliente (customer_tenure) tuvo un fuerte efecto negativo, indicando que clientes más antiguos tienden a permanecer.

En Random Forest, las más importantes fueron account_charges_total, customer_tenure, account_cuentas_diarias y account_charges_monthly, lo que refuerza la importancia de la facturación y la duración de la relación con el cliente.

Hallazgos clave

Clientes con cargos totales y mensuales altos muestran mayor probabilidad de churn, posiblemente por percepción de alto costo.

Clientes nuevos (menor customer_tenure) presentan más riesgo de cancelar, lo que sugiere la necesidad de estrategias de retención temprana.

Algunos métodos de pago, como Electronic Check, aparecen asociados a mayor probabilidad de churn.

Recomendaciones

Implementar un programa de retención temprana para clientes con poca antigüedad.

Revisar planes y precios para clientes con cargos altos, evaluando descuentos o beneficios.

Analizar la experiencia de clientes que usan métodos de pago asociados a alto churn, buscando barreras o fricciones.

## Autor
Enrique Alfaro - [GitHub](https://github.com/EnriqueAlfaro77)

