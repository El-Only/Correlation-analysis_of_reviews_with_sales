# Correlation-analysis_of_reviews_with_sales
Análisis de correlación de ventas de videojuegos con reseñas de usuarios.

# ¿Las ventas de consolas dependen de reseñas de usuarios y critica?

Partiendo del fenómeno titulado, realizamos un análisis exploratorio de datos (EDA) sobre una dataset del 2016 sobre de ventas de videojuegos de la empresa distribuidora "ICE"

## Descripción del Proyecto

En este proyecto realizamos una limpieza de la base para la uniformidad de columnas y tipos de datos correctos para la lectura y análisis. Utilizando multiples gráficos para visualizar las distribuciones de los datos como histogramas, barras, lineas, diagramas de dispersión y gráficos de caja. El conjunto de datos utilizado es `games.csv`, que contiene información sobre juegos vendidos, reseñas de los mismos en diferentes regiones: (NA (Norteamerica), EU (Europa), JP (Japon))

## Descripción de datos:

— Name (Nombre)
— Platform (Plataforma)
— Year_of_Release (Año de lanzamiento)
— Genre (Género) 
— NA_sales (ventas en Norteamérica en millones de dólares estadounidenses) 
— EU_sales (ventas en Europa en millones de dólares estadounidenses) 
— JP_sales (ventas en Japón en millones de dólares estadounidenses) 
— Other_sales (ventas en otros países en millones de dólares estadounidenses) 
— Critic_Score (máximo de 100) 
— User_Score (máximo de 10) 
— Rating (ESRB)

--

# Procesos del EDA

Con la limpieza de datos realizada procedimos con el análisis en enfoque de Distribución Binomial. 
Revisamos:
Análisis poblacional

- Población(1) Ventas totales por año.
- Población(1.2) Ventas totales según la plataforma.
- Población(1.2.1) Plataforma según mejor relación de ventas.
- Población(1.2) Life time de plataforma según ventas anuales.

Análisis muestrario

- Muestra(1) Ventas anules de plataformas en 10 años.
- Muestra(1.2) Top 5 plataformas, ventas por año.
- Muestra(1.2.1) de plataforma PS2 (Distribución de Reseñas)
- Correlación de muestra con población de plataformas.
- Muestras(1.2.2) Distribución ventas por genero.

Correlación Regional

- Muestra(1.2.3) Ventas NA. y cuota de mercado.
- Muestra(1.2.4) Ventas EU. y cuota de mercado.
- Muestra(1.2.5) Ventas JP. y cuota de mercado.
- Muestra(1.2.2.1) Top 5 géneros por region.
- Muestra(1.2.6) Clasificación ESRB por NA, EU, JP.

Pruebas de Hipótesis nula (H0) y relativa (H1).

- Conclusiones.


### Características Principales:
- Visualizaciones extensas de gráficos y correlaciones.
- Análisis Exploratorio de Datos (**EDA**) detallado usando Python.
- Información y proceso de análisis para Distribución binomial.
- Comulaciones detalladas de cada proceso.

---

## Requisitos

Este proyecto fue desarrollado en un entorno Jupyter Notebook para realizar el análisis exploratorio de datos (EDA) y la aplicación de conceptos de probabilidad y estadística. Las siguientes herramientas y librerías fueron utilizadas:

- Python 3.x (recomendado: 3.8 o superior)
- pandas – Manipulación y limpieza de datos tabulares.
- numpy – Funciones matemáticas y estadísticas básicas.
- matplotlib.pyplot – Generación de gráficos estáticos para visualización.
- seaborn – Visualizaciones estadísticas avanzadas y personalizadas.
- sidetable – Cálculo rápido de tablas de frecuencia y porcentajes.
- from scipy import stats – Funciones para distribuciones de probabilidad, estimaciones y estadística - inferencial.
- Jupyter Notebook – Entorno interactivo para la ejecución, visualización.

## Cómo Ejecutar la Aplicación Localmente:

- **Clonar repositorio:**
```bash
# 1. Clona el repositorio en tu máquina local
git clone https://github.com/El-Only/Correlation-analysis_of_reviews_with_sales.git

# 2. (Opcional) Crea y activa un entorno virtual
python -m venv env
source env/bin/activate   # En Windows: env\Scripts\activate

# 3. Instala las dependencias necesarias
pip install -r requirements.txt

# 4. Inicia Jupyter Notebook
jupyter notebook

```
--

## Estructura del Proyecto

```bash
├── README.md                      # Descripción del proyecto e instrucciones
├── Correlation_analysis.ipynb     # Notebook de Análisis Exploratorio de Datos (EDA)
└── datasets/                      # Carpeta de base de datos
    ├── games.csv                  # Base de datos original (cruda)
    └── clean_games.csv            # Base de datos actualizada (limpia)
