# 🚗 Predicción de Ventas BMW con Machine Learning

## 📌 Problema de negocio

Las grandes marcas de automoción necesitan anticipar su demanda por modelo y región para planificar producción, optimizar inventario y distribuir recursos comerciales eficientemente. Sin una herramienta predictiva, estas decisiones se toman de forma reactiva, generando costes evitables.

**¿Puede un modelo de Machine Learning estimar con precisión las ventas mensuales de BMW por modelo y región geográfica usando datos históricos?**

## 🎯 Objetivo

Desarrollar un modelo predictivo de regresión capaz de estimar el volumen de ventas mensual de vehículos BMW, por modelo y región, con un margen de error inferior al 10%.

## 📊 Dataset

- **Fuente:** Kaggle — BMW Global Sales
- **Período:** 2018–2025
- **Volumen:** 3.072 registros mensuales
- **Variables clave:** Region, Model, Avg_Price_EUR, Revenue_EUR, Units_Sold

## 🔧 Proceso técnico

| Fase | Descripción |
|------|-------------|
| Exploración | Revisión de estructura, tipos de datos y calidad del dataset |
| Limpieza | Normalización de formatos monetarios, sin valores nulos detectados |
| Transformación | One-Hot Encoding sobre variables categóricas Region y Model |
| Modelado | Regresión Lineal (scikit-learn), división 80/20, random_state=42 |
| Evaluación | Métricas MAE, RMSE y R² sobre conjunto de prueba |

## ✅ Resultados

| Métrica | Valor | Interpretación |
|---------|-------|----------------|
| R² | 0,952 | El modelo explica el 95,2% de la variabilidad de ventas |
| MAE | 481,76 unidades | Error medio del 6% sobre una media de ~7.980 unidades/mes |
| RMSE | 690,13 unidades | Penalización controlada de errores extremos |

## 💼 Valor para el negocio

Un modelo con estas características permite a una organización:
- Planificar producción e inventario de forma anticipada
- Optimizar recursos comerciales por región y modelo
- Detectar desviaciones respecto a objetivos de ventas con antelación
- Mejorar la precisión de previsiones financieras trimestrales

## 🛠️ Stack tecnológico

`Python` `pandas` `NumPy` `scikit-learn` `Matplotlib` `Google Colab`

## 📁 Estructura del repositorio

- README.md
- data/ → bmw_global_sales_2018_2025.csv
- notebooks/ → Reto4_Script.py
- outputs/ → Predicciones_Reto4.csv
- docs/ → Informe_Proyecto.pdf y Presentacion_Proyecto.pptx

## 🔮 Líneas de mejora futuras

- Implementar Random Forest o Gradient Boosting para capturar relaciones no lineales
- Incorporar variables macroeconómicas: GDP_Growth, Fuel_Price_Index, BEV_Share
- Aplicar validación cruzada temporal para evaluar robustez ante ciclos económicos
