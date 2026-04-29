# 📈 IA Stock Picking: Estrategia Macro-Técnica con XGBoost

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Resumen del Proyecto
Este repositorio contiene la implementación técnica de mi **Trabajo de Final de Máster (TFM)**. El objetivo es crar una cartera que supere al índice S&P 500 mediante un modelo de clasificación **XGBoost** que no solo analiza el precio, sino que entiende el contexto macroeconómico (Inflación, VIX, Tipos de Interés).

### Métricas Clave (Comisiones 0.25%):
- **ROI IA Top 10:** ~68% (Frente al 49% del S&P 500)
- **Alpha Generado:** $+1,800 aprox. en el periodo evaluado.
- **Gestión de Riesgo:** El modelo aumenta la liquidez (Cash) en periodos de alta volatilidad macro.

## 🏗️ Estructura del Pipeline
1. **Ingestión:** Conexión con Yahoo Finance y FRED (Federal Reserve Economic Data).
2. **Procesamiento:** Cálculo de indicadores técnicos (RSI, MACD, Medias) y alineación de series macro.
3. **Modelado:** Clasificación binaria con XGBoost para predecir la probabilidad de superar la mediana del mercado.
4. **Backtesting:** Simulación mensual con costes de transacción realistas (0.25%).

## 🛠️ Cómo ejecutar
1. Clona este repositorio.
2. Sube el archivo `.ipynb` a **Google Colab**.
3. Sigue las instrucciones de la primera celda sobre el **Reinicio de Sesión**.

---
**Autor:** Eloi Arjona  
**Tutor:** Rafael Luque Ocaña  
**Institución:** Universitat Oberta de Catalunya (UOC)
