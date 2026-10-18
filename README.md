# ConnectaTel – Análisis de datos de telecomunicaciones

Este repositorio contiene un análisis exploratorio de datos (EDA) del comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones con operaciones en México y Colombia.

El proyecto analiza la información de los clientes, los planes contratados y el uso de los servicios móviles durante el periodo de estudio, con datos registrados hasta 2024. El objetivo es identificar patrones de consumo de llamadas y mensajes, detectar inconsistencias y valores atípicos, segmentar a los usuarios y generar recomendaciones comerciales basadas en los datos.

📂 Contenido del repositorio
notebooks/connectatel_analysis.ipynb: notebook principal con la exploración, limpieza, análisis estadístico, visualizaciones, detección de valores atípicos, segmentación de clientes y conclusiones ejecutivas.
data/: carpeta destinada a los archivos CSV originales del proyecto.
📊 Datasets utilizados
El análisis se basa en tres fuentes de datos:

plans.csv: información de los planes Básico y Premium, incluyendo precios mensuales, minutos y mensajes incluidos, datos móviles y tarifas por consumo adicional.
users_latam.csv: información de los clientes, como edad, ciudad, fecha de registro, plan contratado y fecha de cancelación del servicio.
usage.csv: registros de uso de los servicios móviles, incluyendo identificador del cliente, tipo de evento, fecha, duración de llamadas y longitud de mensajes.
🎯 Objetivos del análisis
Explorar y comprender la estructura de los datasets.
Identificar y tratar valores nulos, sentinels y fechas fuera del periodo establecido.
Validar la consistencia de los datos y estandarizar los tipos de las columnas.
Construir perfiles estadísticos de los clientes según su uso de llamadas y mensajes.
Detectar valores atípicos mediante estadísticas descriptivas, histogramas, diagramas de caja y el método IQR.
Segmentar a los clientes por edad y nivel de uso.
Identificar oportunidades para mejorar los planes, personalizar las ofertas y fortalecer la retención de clientes.
🛠️ Herramientas utilizadas
Python: procesamiento y análisis de datos.
Pandas: limpieza, transformación, agrupación e integración de datasets.
NumPy: operaciones numéricas y creación de segmentos mediante condiciones lógicas.
Matplotlib: elaboración de gráficos.
Seaborn: visualización estadística de distribuciones y valores atípicos.
Jupyter Notebook / Google Colab: desarrollo y documentación del proyecto.
🔄 Etapas del análisis
Carga y exploración: lectura de los archivos CSV, revisión de las primeras filas, dimensiones, tipos de datos y estructura de cada dataset.
Diagnóstico de calidad: identificación de valores nulos, sentinels, inconsistencias entre tipos de eventos y fechas posteriores a 2024.
Limpieza de datos: tratamiento de edades inválidas, ciudades desconocidas y fechas fuera de rango. Los valores nulos de duración y longitud se conservan cuando corresponden al tipo de evento.
Agregación por cliente: cálculo de la cantidad de mensajes, llamadas y minutos de llamada por usuario, integrando estas métricas con la información de los clientes.
Análisis estadístico y visualización: cálculo de estadísticas descriptivas y creación de histogramas para estudiar las distribuciones de edad y uso según el plan contratado.
Detección de valores atípicos: aplicación del método IQR y uso de diagramas de caja para identificar consumos extremos y evaluar su relevancia.
Segmentación de clientes: clasificación por nivel de uso (Bajo uso, Uso medio y Alto uso) y por edad (Joven, Adulto y Adulto Mayor).
Análisis ejecutivo: síntesis de los principales hallazgos y elaboración de recomendaciones comerciales para ConnectaTel.
🔎 Principales hallazgos
Calidad de los datos: se identificaron valores inválidos en la edad (-999), ciudades desconocidas (?), fechas de registro de 2026 y registros con información faltante.
Uso de los servicios: el perfil agregado presenta una media de 5,5 mensajes, 4,5 llamadas y 23,3 minutos de llamada por cliente.
Distribución por plan: el 64,9 % de los usuarios pertenece al plan Básico y el 35,1 % al plan Premium.
Nivel de uso: el 19,5 % de los usuarios se clasifica como de Bajo uso, el 73,6 % como de Uso medio y el 7,0 % como de Alto uso.
Valores atípicos: se identificaron 46 casos en mensajes, 30 en llamadas y 109 en minutos de llamada mediante el método IQR. Se conservaron para no eliminar comportamientos potencialmente legítimos.
Oportunidades comerciales: los segmentos de bajo y alto uso ofrecen oportunidades diferenciadas para desarrollar estrategias de activación, retención y adecuación de los planes.
Los resultados detallados, las visualizaciones y las decisiones de limpieza se encuentran documentados en el notebook.

💡 Recomendaciones para el negocio
Evaluar ofertas de migración al plan Premium para clientes de alto uso que puedan beneficiarse de sus condiciones.
Diseñar campañas de activación para usuarios de bajo uso y estudiar su posible relación con el abandono del servicio.
Priorizar la segmentación basada en el comportamiento de consumo y contrastarla con la edad y el plan contratado.
Mejorar la captura de ciudades y fechas de registro para aumentar la confiabilidad de los análisis.
Investigar los consumos extremos antes de clasificarlos como errores o posibles anomalías.
Analizar las tasas de cancelación (churn) por plan y segmento para orientar las estrategias de retención.
▶️ Cómo abrir el notebook en Google Colab
Haz clic en el siguiente botón para abrir el notebook:

![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)

También puedes seguir estos pasos:

Abre el archivo connectatel_analysis.ipynb desde el repositorio de GitHub.
Selecciona Open in Colab o abre Google Colab y carga el notebook.
Asegúrate de tener disponibles los tres archivos CSV.
Ejecuta las celdas en orden para reproducir el análisis.
📘 Cómo reproducir el análisis
Clona o descarga este repositorio.
Coloca los archivos plans.csv, users_latam.csv y usage.csv en la carpeta data/, o ajusta las rutas de lectura en el notebook.
Instala las dependencias necesarias si el entorno no las incluye:

pip install pandas numpy matplotlib seaborn jupyter
Abre Jupyter Notebook y ejecuta:

jupyter notebook
Abre notebooks/connectatel_analysis.ipynb y ejecuta las celdas en orden.
Nota: el notebook original utiliza rutas como /datasets/plans.csv, /datasets/users_latam.csv y /datasets/usage.csv. Para reproducir el análisis fuera del entorno original, estas rutas deben ajustarse a la ubicación real de los archivos.

📌 Conclusión
El análisis permite construir una visión estructurada del comportamiento de los clientes de ConnectaTel, mejorar la calidad de los datos y reconocer segmentos con diferentes niveles de consumo. Los resultados constituyen una base para evaluar oportunidades comerciales, optimizar los planes y desarrollar estrategias de retención sustentadas en datos.

🔗 Repositorio del proyecto
Enlace del repositorio: https://github.com/JohanaSalas1978/ConnectaTel-Analysis 

**GitHub:** [ConnectaTel-Analysis](https://github.com/JohanaSalas1978/ConnectaTel-Analysis)

## ▶️ Abrir notebook en Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JohanaSalas1978/ConnectaTel-Analysis/blob/main/S7%20Version%20Final-Estudiante-Project-ConnectaTe....ipynb)
