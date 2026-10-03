# Análisis Exploratorio de Datos y Segmentación - ConnectaTel

## Objetivo del Proyecto
El objetivo principal de este proyecto es analizar el comportamiento de los usuarios de la empresa de telecomunicaciones ConnectaTel, identificando patrones de uso (llamadas y mensajes), detectando inconsistencias o datos anómalos en la base de datos, y realizando una segmentación de clientes basada en variables demográficas y de consumo para entregar recomendaciones estratégicas de negocio.

## Datasets Utilizados
* **`users`**: Contiene datos demográficos y de suscripción de los clientes (`user_id`, `age`, `city`, `reg_date`, `plan`, `churn_date`).
* **`usage`**: Registra el consumo detallado de los usuarios (`id`, `user_id`, `type`, `date`, `duration`, `length`).
* **`plans`**: Define las tarifas, límites incluidos e hiper-consumos de los planes (*Basico* y *Premium*).

## Etapas del Análisis Realizadas
1. **Exploración Inicial:** Inspección de estructuras, conteo de filas, columnas y verificación de tipos de datos.
2. **Limpieza y Preprocesamiento de Datos:**
   * Imputación de edades inválidas (`-999`) utilizando la mediana del grupo.
   * Tratamiento de valores faltantes y caracteres especiales (`?`) en la variable de ciudad.
   * Manejo de registros atípicos de fechas futuras (`reg_date > 2024`).
3. **Segmentación de Clientes:**
   * Clasificación por nivel de uso (`Bajo uso`, `Uso medio`, `Alto uso`).
   * Clasificación demográfica por edad (`Joven`, `Adulto`, `Adulto Mayor`).
4. **Visualización e Insights:** Generación de gráficos para analizar la distribución por segmento e identificar outliers de consumo.
5. **Conclusiones Ejecutivas:** Elaboración de propuestas comerciales y recomendaciones operativas para la toma de decisiones.

## Cómo Ejecutar el Notebook
1. Clona este repositorio o descarga el archivo `.ipynb`.
2. Abre el archivo directamente en **Google Colab** o en un entorno local con **Jupyter Notebook**.
4. Asegúrate de tener instaladas las bibliotecas necesarias:
   ```bash
   pip install pandas matplotlib seaborn

## Guía de Reproducción
1. Carga los datasets originales (users.csv, usage.csv, plans.csv) en el mismo directorio donde se ejecuta el cuaderno.
2. Ejecuta el pipeline completo desde la celda 1 para aplicar los pasos de filtrado de outliers y la imputación de la mediana en la columna de edad.
