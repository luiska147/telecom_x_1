# Análisis de Retención y Fuga de Clientes (Churn) - Telecom X 📊📉

## 📌 Descripción del Proyecto
Este proyecto de Data Science se centra en el análisis exploratorio de datos (EDA) para identificar y comprender las variables que influyen en la decisión de los clientes de cancelar sus servicios (Churn) en la empresa de telecomunicaciones **Telecom X**. A través del procesamiento de datos y la visualización interactiva, se busca descubrir patrones de comportamiento y proporcionar planes de acción estratégicos para mejorar la retención de clientes.

## 🛠️ Tecnologías y Herramientas Utilizadas
- **Lenguaje:** Python
- **Manipulación y Análisis de Datos:** Pandas (Aplanamiento de JSON, limpieza, *One-Hot Encoding*, transformación de variables categóricas).
- **Visualización de Datos:** Plotly Express & Plotly Graph Objects (Histogramas, Boxplots, Gráficos con paneles iterativos).
- **Entorno de Desarrollo:** Google Colab / Jupyter Notebook

## 🗂️ Estructura del Proyecto

1. **Extracción y Normalización de Datos:**
   - Consumo de datos desde una API en formato JSON.
   - Uso de `pd.json_normalize()` para aplanar diccionarios anidados (ej. `customer`, `phone`, `internet`, `account`) en un DataFrame estructurado.

2. **Auditoría y Limpieza (Data Cleaning):**
   - Estandarización de nombres de columnas a formato `snake_case` y traducción al español.
   - Eliminación de registros atípicos o vacíos en columnas críticas como `Churn` y `Cargos Totales`.
   - Conversión de variables de texto binarias ("Yes"/"No") a valores booleanos/numéricos (1 y 0).

3. **Análisis Exploratorio de Datos (EDA):**
   - **Análisis Demográfico y de Estructura Familiar:** Relación del Churn con el segmento de adultos mayores y clientes sin dependientes.
   - **Análisis de Servicios:** Evaluación crítica del servicio de Fibra Óptica y la retención generada por servicios adicionales (Soporte Técnico, Seguridad en Línea).
   - **Análisis Financiero y de Permanencia:** Cruce de variables numéricas como Meses de Contrato, Método de Pago, Cargos Mensuales y el desarrollo de la métrica `Cuentas diarias`.

4. **Conclusiones y Recomendaciones Ejecutivas:**
   - Planes de acción basados en datos para la mitigación del Churn (Estrategias de *Bundling*, incentivos de migración de contratos y auditorías de servicio).

## 🚀 Cómo ejecutar este proyecto

1. Abre el notebook directamente en Google Colab a través del siguiente enlace:
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1fXBC-QuLYT1lTAsuH0uQXbuOmC6Otqt2?usp=sharing)
2. Asegúrate de ejecutar la primera celda que importa las librerías (`pandas`, `plotly.express`, etc.) y descarga el dataset crudo en formato JSON desde su repositorio original.
3. Ejecuta las celdas de forma secuencial para observar el proceso de limpieza y la generación de los gráficos interactivos.

## 💡 Hallazgos Destacados
- Los **contratos mes a mes** concentran la gran mayoría de las cancelaciones, especialmente cuando el método de pago es manual (Cheque Electrónico).
- El servicio de **Fibra Óptica** presenta anomalías de fuga durante los primeros meses de instalación.
- Los clientes que **no cuentan con servicios de valor agregado** (protección o soporte técnico) son altamente vulnerables a abandonar la empresa.
