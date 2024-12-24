# Prediccion de churn de empresa de telecomunicaciones

Este repositorio contiene un proyecto de análisis y predicción de "churn" (tasa de abandono) para una compañía de telecomunicaciones. El objetivo principal es identificar patrones y desarrollar un modelo predictivo para anticipar qué clientes tienen mayor probabilidad de cancelar el servicio. También se realizan recomendaciones a partir de los insights para la retención de consumidores.

## Objetivo del proyecto
El objetivo es desarrollar un sistema que permita:
- Comprender las características clave que influyen en el churn de los clientes.
- Construir un modelo predictivo para clasificar clientes con alta probabilidad de abandono.
- Optimizar estrategias de retención mediante insights obtenidos a partir de los datos.

## Análisis de datos
Se realizó un análisis exploratorio para entender las características de los datos y su relación con el churn. Algunas de las tareas incluidas fueron:
- Visualización de distribuciones de datos y relaciones entre variables clave.
- Tratamiento de valores nulos y limpieza de datos.
- Conversión de variables categóricas en formatos adecuados para el modelado.

### Variables principales
El dataset incluye variables como:
- `gender`, `SeniorCitizen`, `Partner`, `Dependents`.
- Información del servicio: `InternetService`, `Contract`, `PaymentMethod`.
- Métricas financieras: `MonthlyCharges`, `TotalCharges`.
- La variable objetivo: `Churn`.

## Modelado predictivo
Se desarrollaron y evaluaron varios modelos de clasificación, incluyendo:
- **Regresión Logística**: Un modelo base para establecer una línea de referencia.
- **Random Forest**: Para capturar interacciones complejas entre características.
- **Gradient Boosting Classifier**: Por su proteccion al sobreajuste y flexibilidad.

A partir de estos modelos se entreno un Voting Classifier combinando las fortalezas de los 3 modelos para obtener mejores predicciones

### Métricas de Evaluación
Se utilizaron métricas como:
- Precisión.
- Recall.
- F1-score.
- AUC-ROC.

## Resultados
Adquirir un nuevo consumidor puede costar hasta 5 veces de lo que cuesta retener a uno. A partir de este analisis conseguimos un modelo capaz de identificar cuales son nuestros clientes con mayor riesgo de cambiar de firma y poder accionar acordemente para retenerlos. Tambien pudimos identificar las variables que mayor impacto tienen sobre el churn:
* Acorde a los visto en el analisis exploratorio, el servicio de fibra optica es un gran predictor de churn, esto puede estar relacionado a la calidad del servicio, por lo que sera necesario informar a los responsables de fibra optica y que investiguen las causas. De la mano de esto tambien podemos ver como los contratos sin servicio de internet y los contratos de telefono tienden a retener clientes, esto refuerza la hipotesis de que hay un problema de calidad en servicio de internet.
* Los contratos de mes a mes tambien tienen un gran impacto, deberiamos llevar a cabo un plan para ver si es posible la implementacion de ofertas en los planes de año o 2 años. Como podemos ver, los contratos de 2 años tienden a retener al cliente en gran medida.
* Podemos ver que el tenure es la variable que mas ayuda a retener clientes, esto indica que los clientes de mucho tiempo estan contentos con el servicio, es muy importante mantener esta relacion con los clientes de muchos años
* Vemos que los montos totales tambien tienen un gran impacto sobre el churn, esto podria estar relacionado al servicio de fibra optica que usualmente es el mas caro. Si un servicio es caro y su calidad no refleja el precio es esperable que las personas cambien de firma.
Recomiendo ver el notebook del proyecto donde se ve en detalle lo aqui expuesto
