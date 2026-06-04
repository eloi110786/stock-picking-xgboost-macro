# 📈 IA Stock Picking: Estrategia Macro-Técnica con XGBoost

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Resumen del Proyecto
Este repositorio contiene la implementación técnica del **Trabajo de Final de Máster (TFM)** titulado: *"Optimización de Carteras mediante Aprendizaje Supervisado: Un enfoque híbrido basado en XGBoost con indicadores macroeconómicos y técnicos (2015-2025)"*.

El objetivo principal es diseñar un sistema automatizado de asignación de activos que supere al índice de referencia mediante un **clasificador ternario basado en XGBoost**, integrando dinámicamente indicadores técnicos de mercado con variables macroeconómicas estructurales y un filtro de confianza avanzado (*Gatekeeper*).

## 📊  Métricas Clave

### Rendimiento del Backtesting (Periodo Out-of-sample, Fricciones del 0.25%):
* **ROI de la Cartera IA Top 10:** **70.04%** (superando significativamente al índice de referencia).
* **Generación de Alfa:** **+20%** de Alfa respecto al mercado.
* **Gestión del Riesgo:** Mitigación de caídas mediante la asignación dinámica de liquidez (*Cash*) en entornos de alta volatilidad macroeconómica controlados por el filtro *Gatekeeper*.


## 🏗️ Estructura del Pipeline de Código
El archivo principal `tfm_predictive_model_final.ipynb` unifica las siguientes fases de desarrollo de software e ingeniería financiera:

1. **Universo de acciones:** Se escogen 50 acciones estratrificadas por sectores del SP500.
2. **Feature Engineering:** Construcción de features macroeconómicas (Bono 10Y, Inflación, Curva de Tipos, VIX) y técnicas (RSI, MACD, Distancia a SMA 200) e inflación.
3. **Alineación Temporal de Datos:** Sincronización cronológica exhaustiva de fuentes de datos de distinta frecuencia.
4. **Modelado Predictivo:** Configuración de un clasificador ternario (XGBoost) optimizado y acoplado a un filtro probabilístico (*Gatekeeper > 45%*) para el filtrado de señales de compra redundantes o ruidosas.
5. **Simulador Financiero:** Motor de backtesting con cálculo e impacto explícito de comisiones bancarias por operación (0.25%).

## 📁 Estructura del Repositorio
```text
├── README.md                                    <- Manual de usuario e instrucciones del proyecto.
├── TFM_Eloi_Arjona_Guimera_Memoria_Final.pdf    <- Memoria del proyecto.
├── tfm_predictive_model_final.ipynb             <- Pipeline de código unificado en Python.
├── requirements.txt                             <- Dependencias y librerías requeridas (incluye SHAP).
└── Datos/                                       <- Carpeta de almacenamiento de datos e imágenes.
    ├── universo_tfm.csv                         <- Histórico base de los 50 activos.
    ├── tabla_maestra_tfm.csv                    <- Dataset integrado con todas las features.
    ├── predicciones_modelo.csv                  <- Outputs y etiquetas del clasificador.
    ├── dataset_tfm_dashboard.csv                <- Datos procesados para el cuadro de mando.
    ├── grafico_sectores_tfm.png                 <- Gráfico de distribución de activos.
    └── dashboard.png                            <- Captura del panel de control analítico.
