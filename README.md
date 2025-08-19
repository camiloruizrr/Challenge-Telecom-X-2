# Challenge-Telecom-X-2
Parte 2 del challenge telecom x

Análisis de Churn de Clientes – TelecomX

Este proyecto realiza un análisis de churn (cancelación de clientes) para una compañía de telecomunicaciones, utilizando técnicas de preprocesamiento de datos, visualización y modelado predictivo en Python.

1. Descripción del Dataset

El dataset contiene información de clientes con las siguientes variables principales:

customerID: Identificación única del cliente

Churn: Indica si el cliente canceló (Yes) o permaneció (No)

gender: Género del cliente

SeniorCitizen: Si el cliente es mayor de 65 años

Partner y Dependents: Estado civil y dependientes

tenure: Meses de contrato

Servicios contratados: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies

Facturación: Contract, PaperlessBilling, PaymentMethod, Charges.Monthly, Charges.Total

2. Preprocesamiento

Se identificaron y manejaron valores nulos, especialmente en Charges.Total.

Se eliminaron columnas irrelevantes para la predicción.

Se convirtieron variables categóricas a numéricas mediante One-Hot Encoding.

Se aplicó SMOTE para balancear las clases (churn vs no churn).

3. Análisis Exploratorio

Distribución de Churn: ~27% de clientes cancelaron.

Variables relacionadas con churn:

tenure: Clientes con contratos cortos tienden a cancelar más.

Charges.Total: Clientes con menor gasto total tienen mayor probabilidad de churn.

TechSupport y PaperlessBilling muestran correlaciones con cancelación.

Se generaron boxplots y scatterplots para identificar tendencias y patrones.

4. Modelos Predictivos

Se entrenaron los siguientes modelos:

Árbol de Decisión

Accuracy: 0.73

F1-score (churn): 0.53

Random Forest

Accuracy: 0.77

F1-score (churn): 0.58

Mejor desempeño que el árbol simple, mayor capacidad de generalización.

5. Conclusiones

Random Forest es el modelo más adecuado para predecir churn en este dataset.

Aún existen desafíos para predecir clientes que cancelan debido a la clase minoritaria.

Recomendaciones:

Ajustar hiperparámetros del Random Forest

Explorar modelos boosting (XGBoost, LightGBM)

Agregar nuevas variables derivadas y métricas de interacción entre servicios y gastos

Implementar estrategias de retención enfocadas en clientes nuevos o con bajo gasto.
