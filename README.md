# Brecha del Producto e Inflación en el Perú

Este repositorio contiene un análisis econométrico aplicado que estudia la relación entre la brecha del producto (output gap) y la inflación en el Perú, utilizando datos trimestrales y herramientas estándar de macroeconometría.

## 📌 Objetivo
Evaluar empíricamente si una economía operando por encima de su producto potencial genera presiones inflacionarias, en línea con la Curva de Phillips, incorporando además la persistencia inflacionaria.

## 📊 Datos
- **Producto Bruto Interno (PBI) trimestral** – BCRP  
- **Índice de Precios al Consumidor (IPC)** – BCRP  
- Periodo de análisis: **2000–2024**

## 🧠 Metodología
- Transformación del PBI en logaritmos
- Estimación del producto potencial mediante el **Filtro Hodrick–Prescott (λ = 1600)**
- Construcción de la brecha del producto (componente cíclico)
- Estimación de una **Curva de Phillips dinámica** mediante regresión múltiple
- Corrección por autocorrelación usando **errores robustos de Newey–West (HAC)**

Modelo estimado:
\[
\pi_t = \beta_0 + \beta_1 (y_t - y_t^*) + \beta_2 \pi_{t-1} + \varepsilon_t
\]

## 📈 Resultados principales
- Alta **persistencia inflacionaria** (coef. ≈ 0.90, p < 0.01)
- Impacto **positivo y significativo** del output gap sobre la inflación (p < 0.10)
- Buen poder explicativo del modelo (R² ≈ 0.82)

Los resultados son consistentes con la evidencia macroeconómica para economías con metas de inflación creíbles.

## 📂 Contenido del repositorio
- `Output_Gap_e_Inflacion_Evidencia_para_el_Peru.pdf` → Documento final
- `*.ipynb` / scripts → Código del análisis
- `PBI.xlsx`, `IPC MENSUAL.xlsx` → Datos utilizados

## 🛠️ Herramientas
- Python
- pandas, numpy
- statsmodels
- matplotlib

## 👤 Autor
**David Carruitero Castillo**  
Econometría Aplicada
