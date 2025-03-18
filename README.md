# proyecto_gv


2. Materiales y Métodos

2.1. Diseño del Estudio
Se realizó un estudio observacional, longitudinal y prospectivo en pacientes con insuficiencia renal crónica (IRC) en programa de hemodiálisis crónica (HDC). El diseño incluyó mediciones ecocardiográficas transtorácicas bidimensionales y Doppler, realizadas en condiciones basales pre-diálisis (<2 horas antes de la sesión) y post-diálisis (dentro de los 30 minutos posteriores a la finalización), para evaluar cambios hemodinámicos agudos asociados a la ultrafiltración. El protocolo fue aprobado por el Comité de Ética Institucional (número de registro: [insertar]), y todos los participantes firmaron consentimiento informado.

2.2. Población de Estudio
Criterios de inclusión:

Criterios de exclusión:

2.3. Variables y Mediciones
2.3.1. Variables Ecocardiográficas:
Las mediciones se realizaron siguiendo las guías de la Sociedad Europea de Cardiología (ESC) y la Asociación Americana de Ecocardiografía (ASE), utilizando equipos [marca/modelo] con transductores de 2.5-3.5 MHz. Se analizaron 52 parámetros agrupados en:

Sobrecarga volumétrica:

Índice de volumen auricular izquierdo (AI Vol Index).
Colapso de la vena cava inferior (VCImin, %Colapso VCI).
Presión venosa central estimada (NAGUE+).
Función ventricular izquierda:

Fracción de acortamiento (FAC), fracción de eyección (FEVI, método Simpson biplanar).
Relación E/e' promedio (EEPRIM), índice de Tei (TEI).
Función ventricular derecha:

Excursión sistólica del plano anular tricuspídeo (TAPSE), strain longitudinal del VD (STISVD).
Diámetro telediastólico del VD (VD3dil).
Hemodinámica pulmonar y rigidez arterial:

Presión sistólica arterial pulmonar (PSAP), velocidad de la onda de pulso carotídea (VEL IT), índice de distensibilidad (ID).
Dinamismo hemodinámico:

Velocidades sistólica/diastólica supraaórtica (Ssup, Dsup), relación S/D (SFF).
2.3.2. Covariables Clínicas:
Se registraron datos demográficos (edad, sexo), comorbilidades (HTA, DBT, DLP), tratamiento farmacológico (IECA, ARA II, betabloqueantes), y parámetros dialíticos (Kt/V, balance hídrico).

2.4. Manejo de Datos y Análisis Estadístico
2.4.1. Preprocesamiento:

Valores faltantes: Mediante análisis multivariado (Missing Completely at Random, MCAR), se evaluó la asociación de datos faltantes con variables clínicas clave (hipertensión, diabetes, sexo, dislipidemia) usando pruebas χ² (categóricas) y t-test (continuas). Variables con >30% faltantes en cualquier momento (pre/post) se excluyeron del análisis longitudinal.
Normalización: Variables con unidades no directamente interpretables (e.g., índices ecocardiográficos derivados) se estandarizaron mediante escalado Z.
2.4.2. Análisis Estadístico:

Normalidad: Evaluada con prueba de Shapiro-Wilk (α=0.05).
Comparaciones pre-post: t-test pareado (datos normales) o prueba de Wilcoxon (no paramétricos), aplicados a datos estandarizados para homogenizar escalas.
Tamaño del efecto: Cohen’s d en escala estandarizada (d=0.2: pequeño; d=0.5: moderado; d≥0.8: grande).
Concordancia: Modelos de regresión lineal con IC 95% y gráficos de Bland-Altman (límites de acuerdo: ±1.96 DE).
Visualización: Histogramas superpuestos, diagramas de caja con swarmplots, y análisis de tendencia.
2.4.3. Consideraciones Éticas y Software:
Los datos se anonimizaron asignando identificadores únicos no vinculables. El análisis se implementó en Python 3.10 (SciPy v1.11, pandas v2.0.3, statsmodels v0.14), con visualización en matplotlib v3.7.1 y seaborn v0.12.2. El código cumple estándares FAIR y está disponible en [https://github.com/bitazaratustra/proyecto_gv ].

2.5. Consideraciones Éticas y Reproducibilidad
El estudio cumplió con la Declaración de Helsinki (revisión 2013). La reproducibilidad ecocardiográfica se aseguró mediante:

Mediciones duplicadas por dos operadores independientes (coeficiente de correlación intraclase >0.85).
Protocolo estandarizado de adquisición de imágenes (ángulo apical de 4 cámaras, promedio de 3 ciclos cardíacos).
Los datos brutos y los scripts de análisis están depositados en [DOI/repositorio], garantizando transparencia metodológica.

Este apartado proporciona una base metodológica robusta para la evaluación crítica de los resultados, cumpliendo con los estándares STROBE para estudios observacionales.
