# 🌾Análisis y predicción del rendimiento de la producción mundial de arroz

Este proyecto analiza datos globales de **producción de arroz por país**, con el objetivo de **comprender los factores que influyen en el rendimiento agrícola** y construir modelos de **machine learning** para predecir el rendimiento del arroz (kg/hectárea).

El trabajo integra **análisis exploratorio profundo (EDA)**, **limpieza avanzada de datos**, **feature engineering**, **selección de características** y **modelado predictivo**, en un contexto de **seguridad alimentaria y agricultura global**.

---

## 🗺️Contexto del problema

El arroz es uno de los cultivos más importantes del mundo y un pilar clave de la seguridad alimentaria.  
Analizar su producción permite:

- comparar eficiencia agrícola entre países
- identificar factores asociados al alto rendimiento
- apoyar decisiones en políticas agrícolas y planificación productiva
- explorar el potencial de modelos predictivos en agricultura

---

## 🎯Objetivos

- Analizar estadísticamente la producción mundial de arroz
- Explorar relaciones entre producción, superficie cultivada y rendimiento
- Detectar patrones y outliers en datos agrícolas
- Crear nuevas variables explicativas (feature engineering)
- Seleccionar las características más relevantes
- Entrenar y comparar múltiples modelos de regresión
- Predecir el **rendimiento del arroz (kg/hectárea)**

---

## 📊Dataset

**Fuente:** Rice Production by Country  
El dataset contiene información por país sobre producción y consumo de arroz.

### Variables principales
- `Country`
- `Rice Production (Tons)`
- `Rice Production Per Person (Kg)`
- `Rice Acreage (Hectare)`
- `Rice Yield (Kg / Hectare)` *(variable objetivo)*
- Rankings de producción, superficie y rendimiento

---

## 🧹Limpieza y preparación de datos

- Reemplazo de valores inconsistentes (`NaN`, `N/A`, `?`)
- Conversión de unidades con sufijos (`K`, `M`)
- Conversión de valores numéricos con separadores
- Eliminación de duplicados
- Imputación:
  - variables numéricas → media
  - variables categóricas → moda
- Tratamiento de valores atípicos mediante **IQR**
- Escalado de variables numéricas
- Codificación de variables categóricas (Label Encoding)

---

## 🔍Análisis exploratorio (EDA)

### Análisis univariante
- Boxplots para detección de outliers
- Distribuciones de variables numéricas
- Análisis de variables categóricas

### Análisis multivariante
- Matriz de correlación
- Mapas de calor con correlaciones relevantes (|r| > 0.5)
- Evaluación de multicolinealidad

---

## 🧠Feature engineering

Se crearon variables derivadas para capturar mejor la dinámica productiva:

- Población total estimada
- Superficie cultivada per cápita
- Producción per cápita ajustada
- Eficiencia de superficie
- Scores de eficiencia de rendimiento
- Rankings normalizados

Estas variables mejoran la capacidad explicativa de los modelos.

---

## 🎯Selección de características

- Método de filtrado **F-regression**
- Evaluación del impacto estadístico de cada variable
- Selección de features con mayor poder predictivo
- Reducción de multicolinealidad

---

## 🤖Modelado predictivo

### Tipo de problema
- **Regresión supervisada**

### Modelos evaluados
- Linear Regression
- Lasso, Ridge, ElasticNet
- KNN Regressor
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting
- AdaBoost Regressor
- **XGBoost Regressor**

### Evaluación
- Validación cruzada (CV = 5)
- Métricas:
  - R²
  - RMSE
  - MAE

---

## 📈Resultados

- Los modelos basados en **ensemble y boosting** muestran mejor desempeño
- XGBoost captura relaciones no lineales entre variables agrícolas
- El rendimiento está fuertemente influenciado por:
  - eficiencia de superficie
  - superficie cultivada
  - rankings de producción y rendimiento
- La ingeniería de variables mejora significativamente el poder predictivo

---

## 📊Visualizaciones

- Boxplots antes y después del tratamiento de outliers
- Mapas de calor de correlación
- Gráficos de importancia de variables
- Comparación valores reales vs. predichos

---

## 🛠️Tecnologías utilizadas

- **Python**
- **pandas, numpy**
- **matplotlib, `seaborn**`
- **scikit-learn**
- **XGBoost**
- **scipy, statsmodels**

---

## 📂Estructura del repositorio

├── rice_production_by_country.csv
├── produccion_arroz.py
├── README.md


---

## 🚀Próximos pasos

- Optimización de hiperparámetros (Grid / Random Search)
- Interpretabilidad del modelo (SHAP)
- Análisis por regiones geográficas
- Incorporación de variables climáticas
- Deploy del modelo como herramienta analítica

---

## 👤Autor

**Flavia Hepp**  
Data Scientist en formación  
