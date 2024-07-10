# **📊 Memoria del Análisis Exploratorio de Datos 📊**

## **ÍNDICE**
1. [📌 Introducción](#introducción)
2. [📌 Descripción del Proyecto](#descripción-del-proyecto)
3. [📌 Fuentes de Datos](#fuentes-de-datos)
4. [📌 Técnicas Utilizadas](#técnicas-utilizadas)
5. [📌 Exploración de Datos Descriptiva](#exploración-de-datos-descriptiva)
6. [📌 Análisis Bivariado](#análisis-bivariado)
7. [📌 Visualización de Datos](#visualización-de-datos)
8. [📌 Resultados y Conclusiones](#resultados-y-conclusiones)
9. [📌 Recomendaciones](#recomendaciones)
10. [📌 Referencias](#referencias)

## **📌 Introducción**
En esta memoria se documenta el proceso y los resultados del Análisis Exploratorio de Datos (EDA, por sus siglas en inglés) realizado en el proyecto **Optimizando la Eficiencia en Transacciones Portuarias: Un Enfoque Basado en Análisis de Datos**. El EDA es una etapa crucial en el proceso de análisis de datos, que permite comprender mejor el conjunto de datos, identificar patrones, tendencias y anomalías, y orientar el enfoque del análisis posterior.

## **📌 Descripción del Proyecto**
En base al histórico proporcionado por Xnova Internacional sobre todas las transacciones portuarias en USA, se pretende analizar los retrasos de las mercancías y encontrar patrones que puedan generar diferentes hipótesis para aplicar soluciones a dichos problemas y mejorar la eficiencia.

## **📌 Fuentes de Datos**
Las fuentes de datos incluyen:
- Datos proporcionados por Xnova Internacional en un archivo `.csv` con todas las transacciones.
- Información extraída de la web SeaRates para obtener las coordenadas y los puertos de USA mediante web scraping y regex.
- Gráficas del precio del petróleo desde el 2020 hasta el 2024 extraídas de TradingView.
- Consideración del Año Nuevo Chino, que comienza a inicios de febrero y conlleva un mes de vacaciones, afectando significativamente las transacciones portuarias.

## **📌 Técnicas Utilizadas**
- **Lenguajes y Bibliotecas:** Python, Pandas, Numpy, Regex
- **Web Scraping:** BeautifulSoup
- **Visualización de Datos:** Matplotlib, Seaborn, Pyplot, Folium
- **Dashboard:** Looker Studio

## **📌 Exploración de Datos Descriptiva**
- Resumen estadístico de las variables clave. Las variables más relevantes para el análisis han sido: `loading_port`, `unloading_port`, `weight`, `estimate_arrival_date` y `complete_date`. Con las dos últimas, se creó una nueva variable `delay_time` para representar el tiempo total de retrasos en cada transacción.
- Visualización de distribuciones de datos mediante histogramas y gráficos de densidad.
- Identificación y manejo de valores atípicos y datos faltantes.

## **📌 Análisis Bivariado**
- Relación entre columnas para el análisis:
  - `delay_time`/`weight`
  - `loading_port`/`delay_time`
  - `shipper_name`/`delay_time`
  - `consignee_name`/`delay_time`

## **📌 Visualización de Datos**
- Uso de gráficos de dispersión y barras para representar diferentes aspectos de los datos.
- Mapas para visualizar datos geoespaciales o categóricos.

## **📌 Resultados y Conclusiones**
### **Resultados:**
Tras el cruce de datos y el análisis del mercado, se encontraron los siguientes resultados:
- USA tiene dificultades para recibir mercancía portuaria en el oeste del país debido a la infraestructura insuficiente de los puertos de Long Beach y Los Ángeles para abarcar el mercado asiático.
- El precio del petróleo influye directamente en los retrasos de la mercancía.
- Se observaron complicaciones con los contenedores más pesados.
- La mayoría de las recepciones se realizan justo en el día 30 antes de que pase un mes.
- El Año Nuevo Chino, que comienza a inicios de febrero y conlleva un mes de vacaciones, también afecta significativamente las transacciones portuarias.

### **Conclusiones, Limitaciones y Desafíos:**
- El precio del petróleo es complejo de predecir, pero se pueden identificar tendencias basadas en la época del año, carga de la mercancía y precio del petróleo.
- La geopolítica es difícil de predecir, pero afecta significativamente al mercado.

## **📌 Recomendaciones**
- Es importante manejar adecuadamente los datos para que sean más relevantes y permitan realizar predicciones o análisis precisos.
- Añadir datos climáticos podría mejorar el análisis.
- Realizar un seguimiento del precio del petróleo.
- Generar rutas alternativas a los puertos en base a predicciones de retraso.

## **📌 Referencias**
- Datos proporcionados por Xnova Internacional.
- Recopilación de coordenadas: [SeaRates](https://www.searates.com/es/maritime/united_states)
- Datos del precio del petróleo: [TradingView](https://www.tradingview.com)

