# 🚖 Recopilación y Almacenamiento de Datos

> Análisis de compañías de taxis, barrios con más finalizaciones de viaje  
> y efecto de las condiciones climáticas en la duración de los trayectos.  

---

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" />
  <img src="https://img.shields.io/badge/Pandas-Análisis%20de%20Datos-150458?logo=pandas" />
  <img src="https://img.shields.io/badge/Matplotlib-Visualización-11557c" />
  <img src="https://img.shields.io/badge/SciPy-Pruebas%20Estadísticas-8CAAE6?logo=scipy" />
  <img src="https://img.shields.io/badge/Estado-Proyecto%20Académico-success" />
</p>

---

## 🎯 Objetivos

- Analizar los viajes por empresa de taxis  
- Identificar los barrios con mayor número de finalizaciones  
- Evaluar la concentración del mercado  
- Visualizar patrones de movilidad  
- Probar estadísticamente el impacto del clima en la duración de los viajes  

---
## 📌 Descripción del proyecto

Este proyecto analiza datos reales de viajes en taxi con los siguientes objetivos principales:

- 🚕 Estudiar el **número de viajes por compañía de taxis** (15 y 16 de noviembre de 2017).  
- 🗺️ Identificar los **10 barrios con mayor número de finalizaciones** de viaje en noviembre de 2017.  
- 🌧️ Evaluar si **las condiciones climáticas (Good vs Bad)** afectan la **duración promedio** de los trayectos.  

## 🛠️ Herramientas Utilizadas

- 🐍 Python  
- 🧮 Pandas  
- 📊 Matplotlib  
- 📈 Análisis estadístico  
- 🧪 SciPy  
- 🧹 Limpieza de datos  
- 📐 Visualización de datos  

## 📂 Fuentes de Datos

### 📄 Dataset 1: Compañías de Taxis (Noviembre 15 y 16 - 2017)

| Campo | Descripción |
|--------|-------------|
| company_name | Nombre de la empresa |
| trips_amount | Número de viajes |

### 📄 Dataset 2: Promedio de viajes por barrio (Noviembre 2017)

| Campo | Descripción |
|--------|-------------|
| dropoff_location_name | Nombre del barrio |
| average_trips | Promedio de finalizaciones |

### 📄 Dataset 3: Condiciones climáticas

| Campo | Descripción |
|--------|-------------|
| start_ts | Fecha y hora |
| weather_conditions | Estado del clima |
| duration_seconds | Duración del viaje |

## 🔍 Exploración Inicial de los Datos

### ✅ Inspección de los datasets

- Revisión de filas iniciales
- Revisión de estructura (`info()`)
- Estadísticas descriptivas (`describe()`)
- Búsqueda de valores nulos
- Verificación de duplicados

### ✅ Resultados:

✔️ No se encontraron valores nulos  
✔️ No existen datos duplicados  
✔️ Tipos de datos correctos  
✔️ Datasets limpios y confiables  

## 📊 Visualizaciones Realizadas

## 1️⃣ Empresas de Taxis y Número de Viajes

### 🧾 Conclusiones:
- El mercado se encuentra altamente concentrado.
- Pocas empresas lideran gran parte de los viajes.
- Las compañías pequeñas atienden nichos específicos.
- El tamaño de flota y cobertura son clave.

### 📘 Explicación:
Este gráfico evidencia que la mayor parte de los usuarios elige siempre las mismas empresas, lo que indica una alta dependencia de proveedores líderes del mercado.

## 2️⃣ Top 10 Barrios por Finalización de Viajes

### 🧾 Conclusiones:
- Zonas como **Loop** y **River North** concentran la mayor actividad.
- La movilidad no es uniforme.
- Estos barrios son estratégicos.
- Representan centros comerciales y turísticos.

### 📘 Explicación:
Este gráfico permite identificar zonas "calientes" donde termina la mayoría de los viajes y donde sería conveniente ubicar más vehículos.

## 🧪 Prueba de Hipótesis

## 🧠 Pregunta

> ¿La duración promedio de los viajes cambia los sábados lluviosos?

## 📐 Hipótesis

### Hipótesis nula (H₀):
La duración promedio de los viajes **no cambia** con clima lluvioso.

**μBad = μGood**

### Hipótesis alternativa (H₁):
La duración promedio de los viajes **sí cambia** con clima lluvioso.

**μBad ≠ μGood**

## ⚙️ Metodología Estadística

### ✅ Pasos realizados:

- Separación de muestras:  
  - `Bad` → clima lluvioso  
  - `Good` → clima normal  

- Prueba de normalidad (Shapiro-Wilk)
- Prueba de igualdad de varianzas (Levene)
- Prueba t de Student ajustada (Welch)
- Nivel de significancia: **α = 0.05**

## 📈 Resultados

- p-value = **0.0000**
- Resultado: ✅ Se rechaza H₀
- Conclusión:  
  > La duración promedio de los viajes cambia significativamente cuando llueve.

## 🧾 Interpretación

Durante lluvias:
- Hay mayor congestión
- Disminuye la velocidad promedio
- Aumentan los tiempos de viaje

Esto afecta directamente la experiencia de usuario y la planificación operativa de las empresas.

## ✅ Conclusiones Generales

✔️ El mercado está dominado por pocas empresas  
✔️ La demanda se concentra en zonas estratégicas  
✔️ El clima impacta directamente la duración  
✔️ Los datos confirman patrones urbanos reales  
✔️ La estadística respalda la toma de decisiones

## 🚀 Recomendaciones

- Ubicar más taxis en zonas clave como Loop
- Ajustar tarifas considerando clima
- Optimizar flota los fines de semana
- Incorporar análisis en tiempo real
