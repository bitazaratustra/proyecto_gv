# 🔬 Análisis Pre-Post de Variables Ecocardiográficas en Pacientes en Hemodiálisis

Este repositorio contiene el código, pipeline estadístico y herramientas gráficas implementadas para analizar el impacto de la hemodiálisis en variables ecocardiográficas, clínicas y hemodinámicas. El enfoque se basa en un diseño pareado longitudinal, con procesamiento dual en escala natural y estandarizada (z-score), garantizando tanto la interpretación clínica como la comparabilidad estadística.

---

## 📍 Contexto

- **Institución**: Hospital General de Agudos Dr. Cosme Argerich (Buenos Aires, Argentina)
- **Diseño**: Observacional, prospectivo, longitudinal pareado
- **Muestra**: 38 pacientes con enfermedad renal crónica estadio V
- **Observaciones**: 76 registros (pre y post diálisis)
- **Variables**: 82 (ecocardiográficas, clínicas, de laboratorio, demográficas y farmacológicas)

---

## 🧪 Metodología

### 📊 Análisis Numérico

- Procesamiento dual: escala natural y z-score
- Validación de supuestos:
  - Normalidad (Shapiro-Wilk)
  - Simetría (skewness test)
  - Homocedasticidad (Levene, opcional)
- Selección adaptativa de pruebas:
  - t-test pareado
  - Wilcoxon
  - Bootstrap BCa
- Estimación del efecto:
  - Cohen’s d
  - Intervalos de confianza no paramétricos
  - Potencia observada
- Modelos lineales mixtos:
  - Efectos aleatorios por paciente
  - β POSDIAL con IC95% y p-valor

### 🧩 Análisis de Valores Faltantes

- Exclusión adaptativa por umbral
- Prueba de Little para MCAR
- Asociaciones univariadas (χ² y t-test)
- Reporte de pacientes con mediciones incompletas

---

## 🧠 Organización del Código

| Módulo / Función                | Propósito |
|--------------------------------|-----------|
| `prepare_data()`               | Selección y clasificación de variables |
| `scale_variables()`            | Estandarización Z-score |
| `check_assumptions()`          | Validación de supuestos estadísticos |
| `select_paired_test()`         | Elección del test adecuado |
| `compute_effect_size()`        | Cálculo de Cohen’s d |
| `run_mixed_model()`            | Ajuste de modelo lineal mixto |
| `bootstrap_bca_ci()`           | Intervalos BCa para diferencia media |
| `paired_analysis_full()`       | Pipeline completo para una variable |
| `run_full_numerical_analysis()`| Loop completo para múltiples variables |

---

## 📈 Visualizaciones generadas

- Histograma con KDE (pre y post)
- Boxplot + swarmplot
- Concordancia (identidad vs regresión)
- Bland-Altman
- Q-Q plot de residuos
- Residuos vs valores ajustados

---

## 📦 Requisitos

```bash
python>=3.8
pandas
numpy
scipy
matplotlib
seaborn
statsmodels
