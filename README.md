# sprint7-final-project

Proyecto final del Sprint 7 enfocado en análisis exploratorio de datos (EDA) para ConnectaTel, una empresa de telecomunicaciones.  
El objetivo principal es analizar patrones de uso de llamadas y mensajes, segmentar usuarios y generar insights accionables para el negocio.

---

# Objetivo del proyecto

Analizar el comportamiento de los usuarios de ConnectaTel a partir de sus registros de uso y datos demográficos para:

- Identificar segmentos de clientes.
- Detectar patrones de consumo.
- Encontrar valores atípicos (outliers).
- Comparar comportamiento entre planes Básico y Premium.
- Generar recomendaciones comerciales basadas en los datos.

---

# Datasets utilizados

## users_latam
Información demográfica y de suscripción de los usuarios.

Columnas principales:
- user_id
- age
- city
- reg_date
- plan
- churn_date

---

## usage
Registros de actividad de llamadas y mensajes.

Columnas principales:
- id
- user_id
- type
- date
- duration
- length

---

## plans
Información de los planes telefónicos disponibles.

Columnas principales:
- plan_name
- messages_included
- gb_per_month
- minutes_included
- usd_monthly_pay

---

# Etapas del análisis

## 1. Exploración de datos
- Revisión de estructura y tipos de datos.
- Identificación de valores nulos.
- Detección de inconsistencias.

## 2. Limpieza y transformación
- Conversión de columnas a tipo fecha.
- Tratamiento de sentinels y datos inválidos.
- Validación de fechas fuera de rango.
- Unificación de categorías inconsistentes.

## 3. Análisis exploratorio (EDA)
- Estadísticas descriptivas.
- Histogramas y distribuciones.
- Detección de outliers.
- Comparación por tipo de plan.

## 4. Ingeniería de variables
Creación de variables agregadas por usuario:
- cant_mensajes
- cant_llamadas
- cant_minutos_llamada

Creación de segmentos:
- grupo_uso
- grupo_edad

## 5. Insights de negocio
- Identificación de clientes de alto valor.
- Análisis de patrones de consumo.
- Recomendaciones comerciales.

---

# Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

---

# Cómo ejecutar el proyecto

## Opción 1: Google Colab

1. Descargar el archivo `.ipynb`.
2. Abrir Google Colab:
   https://colab.research.google.com/
3. Subir el notebook.
4. Ejecutar las celdas en orden.

---

## Opción 2: Jupyter Notebook

### Instalar dependencias

```bash
pip install pandas numpy matplotlib seaborn
```

### Ejecutar notebook

```bash
jupyter notebook
```

Abrir el archivo `.ipynb` y ejecutar todas las celdas.

---

# Guía rápida de reproducción

1. Cargar los datasets.
2. Ejecutar limpieza y transformación de datos.
3. Generar estadísticas descriptivas.
4. Crear visualizaciones.
5. Realizar segmentación de usuarios.
6. Analizar insights finales.

---

# Principales hallazgos

- El plan Básico concentra la mayor cantidad de usuarios.
- La mayoría de clientes pertenece al segmento de uso medio.
- Existen usuarios con patrones de consumo intensivo relevantes para estrategias premium.
- Se detectaron inconsistencias como sentinels, fechas futuras y valores inválidos.
- Los outliers encontrados aportan valor para identificar usuarios de alto consumo.

