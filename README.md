# 🏨 Análisis de Alojamientos Turísticos — Gaia Travels
> Proyecto final del Simulador Empresarial · IT Academy Barcelona Activa · Equip 10

---

## 📋 Descripción del proyecto

Este proyecto simula el trabajo real de un **Departamento de Análisis de Datos** dentro de una empresa del sector turístico llamada **Gaia Travels**. A lo largo de cuatro sprints, el equipo realizó un análisis completo del mercado de alojamientos turísticos en España: desde la extracción y limpieza de datos hasta la generación de KPIs, visualizaciones interactivas y un dashboard en Power BI con propuestas de negocio accionables.

El proyecto nació en el marco del **Simulador Empresarial de IT Academy (Barcelona Activa)**, un entorno de aprendizaje que replica las dinámicas de trabajo profesional — reuniones de equipo, gestión ágil con tablero Kanban, roles especializados y presentaciones semanales de resultados.

---

## 🎯 Objetivos

- Aplicar un flujo completo de análisis de datos (ETL → EDA → KPIs → Visualización → Propuestas)
- Analizar el comportamiento de los alojamientos turísticos en España: ocupación, pernoctaciones, perfil del viajero y satisfacción del cliente
- Identificar patrones de estacionalidad, variaciones anuales y procedencia de viajeros
- Construir un dashboard interactivo en Power BI para la toma de decisiones empresariales
- Elaborar propuestas de negocio concretas alineadas con la **Estrategia de Turismo España 2030**

---

## ⚡ Handicaps tecnológicos semanales

Una de las características más diferenciales del simulador fue la introducción de un **handicap tecnológico cada semana**, simulando imprevistos reales del entorno profesional. Al liberar los datos del nuevo sprint, el equipo recibía una restricción técnica adicional que obligaba a replantear el enfoque y buscar soluciones alternativas.

| Semana | Restricción simulada | Solución adoptada |
|---|---|---|
| Sprint 1 | Sin restricción — sprint de arranque | — |
| Sprint 2 | Servidor SQL caído — datos inaccesibles por base de datos | Entrega de datos en CSV · carga directa con pandas |
| Sprint 3 | Licencias de Power BI caducadas | Visualizaciones alternativas con Plotly y matplotlib |
| Sprint 4 | Plazo reducido (entrega el jueves) + requerimiento de benchmarking externo | Integración de datasets del INE · priorización de tareas · coordinación intensiva del equipo |

> El Sprint 4 combinó dos presiones simultáneas: la reducción del plazo de entrega y la petición de la empresa de contrastar los datos internos con datos reales del mercado turístico español. Esto requirió incorporar y cruzar fuentes externas del **Instituto Nacional de Estadística (INE)** para contextualizar los KPIs propios de Gaia Travels dentro del comportamiento real del sector, y así fundamentar las propuestas estratégicas de negocio sobre datos objetivos.

> Este mecanismo entrenó la capacidad del equipo para **adaptarse a entornos con recursos limitados**, tomar decisiones técnicas bajo presión y encontrar soluciones alternativas manteniendo la calidad del análisis — una competencia directamente transferible al entorno profesional real.

---

## 🔄 Metodología: 4 Sprints

Cada sprint giraba en torno a una **pregunta de negocio** planteada por Gaia Travels. El equipo debía responderla con los datos disponibles, respetando el handicap tecnológico de la semana y entregando resultados accionables. El Sprint 1 fue el más exigente al combinar la construcción completa del pipeline ETL con el primer análisis exploratorio. A partir del Sprint 2, la ETL se mantenía o actualizaba únicamente si los datos del nuevo sprint introducían cambios estructurales, lo que permitió al equipo centrarse progresivamente en el análisis y las conclusiones de negocio.

### Sprint 1 — ETL + EDA General *(el más exigente)*
**Pregunta de negocio:** ¿Cuál es el estado actual del mercado de alojamientos turísticos en España y qué variables explican mejor el comportamiento de la oferta?

Construcción del pipeline ETL completo: conexión a la base de datos MySQL (`Tourist_Accommodation`) con SQLAlchemy y pandas, limpieza y transformación de variables (`bathrooms`, `bedrooms`, `beds`), imputación de nulos por medianas agrupadas. Sobre el dataset resultante se realizó el EDA general con primeras exploraciones estadísticas y visuales con matplotlib y seaborn. Este sprint estableció la base de datos limpia de la que partirían todos los sprints siguientes.

### Sprint 2 — Análisis por Departamentos
**Pregunta de negocio:** ¿Qué insights específicos puede extraer cada área de negocio (marketing, operaciones, experiencia del cliente) para mejorar su toma de decisiones?

Cada analista respondió la pregunta desde su área de especialización, profundizando en las variables relevantes para su dominio. La ETL se actualizó puntualmente para incorporar los nuevos datos entregados en CSV tras la caída del servidor SQL (handicap de la semana).

### Sprint 3 — KPIs e Indicadores de Negocio
**Pregunta de negocio:** ¿Cuáles son los indicadores clave de rendimiento de Gaia Travels y cómo evolucionan?

Definición y cálculo de los KPIs principales: tasa de ocupación mensual, índice de satisfacción general, ciudad con mayor ocupación e ítem con mayor valoración. Ante la caducidad de las licencias de Power BI (handicap), se generaron dashboards interactivos alternativos en HTML con Plotly (`fig1_ocupacion`, `fig2_satisfaccion`, `fig3_ciudad`, `fig4_item`).

### Sprint 4 — Benchmarking Externo y Propuestas Estratégicas
**Pregunta de negocio:** ¿Cómo se posiciona Gaia Travels frente al mercado turístico real español y hacia dónde debería dirigir su estrategia?

La empresa solicitó contrastar los datos internos con el comportamiento real del sector. Se integraron datasets del **INE** (viajeros, pernoctaciones, estancia media, variaciones anuales por comunidades autónomas y país de residencia) para contextualizar los KPIs propios dentro del mercado real. Las conclusiones fundamentaron las propuestas estratégicas de negocio alineadas con la **Estrategia de Turismo España 2030**. Todo ello entregado bajo plazo reducido (handicap de la semana).

---

## 📊 Stack tecnológico

| Herramienta | Uso |
|---|---|
| **Python** | Análisis, limpieza y visualización de datos |
| **pandas** | Manipulación y transformación de DataFrames |
| **matplotlib / seaborn** | Visualizaciones estáticas y EDA |
| **Plotly Express** | Gráficos interactivos exportados en HTML |
| **SQLAlchemy** | Conexión y consulta a base de datos MySQL |
| **MySQL** | Base de datos principal (`Tourist_Accommodation`) |
| **Power BI** | Dashboard interactivo final |
| **Jupyter Notebook** | Entorno de desarrollo y documentación |
| **Git / GitLab** | Control de versiones y colaboración en equipo |

---

## 📁 Datos utilizados

Los datos son **ficticios**, generados para el simulador con estructura realista basada en el mercado de alojamientos turísticos español.

**Cobertura geográfica:** Barcelona · Girona · Madrid · Mallorca · Menorca · Sevilla · Valencia

- **Base de datos MySQL**: tabla `Tourist_Accommodation` con información de apartamentos turísticos (id, nombre, descripción, tipo de habitación, barrio, host, baños, dormitorios, camas, precio, valoraciones, etc.)
- **Datasets INE (Instituto Nacional de Estadística)**:
  - Viajeros y pernoctaciones por comunidades autónomas y provincias
  - Viajeros y pernoctaciones por puntos turísticos
  - Viajeros y pernoctaciones según país de residencia
  - Coeficiente de variación de viajeros y pernoctaciones
  - Variación anual de estancia media, establecimientos, ocupación y empleados

---

## 📈 Resultados principales

- Dashboard en **Power BI** con páginas dedicadas a ocupación, satisfacción del cliente, perfil del viajero y variaciones temporales
- **KPIs tracked**: tasa de ocupación mensual, índice de satisfacción general, rankings por ciudad e ítem
- **Propuestas de negocio** documentadas con recomendaciones estratégicas para Gaia Travels
- Análisis de tendencias alineado con la **Estrategia de Turismo España 2030**
- Benchmarking externo con fuentes INE para validar los datos internos frente al mercado real
- Gráficos Plotly interactivos en HTML listos para integrar en presentaciones o web

---

## 👥 Equipo — Equip 10

| Rol | Área |
|---|---|
| **Analista de Experiencia del Cliente + Data Steward** ⬅️ *mi rol* | Satisfacción, puntuaciones y reviews · ETL centralizado y preparación de datasets para todos los departamentos |
| Analista de Marketing y Comunicación | Segmentación, posicionamiento, tendencias |
| Analista de Perfil del Cliente | Comportamiento, valoraciones, tipología |
| Analista de Operaciones | Gestión de inventario, capacidad, eficiencia |
| Analista de Finanzas y Riesgo | Variaciones, KPIs económicos |
| Responsable de Calidad del Repositorio *(rol rotativo)* | Revisión, merge, estándares de código |
| **Mentora / Directora del Departamento** | Facilitación y orientación técnica |

### 🔧 Mi contribución específica

Además de las responsabilidades de análisis de experiencia del cliente, asumí el rol transversal de **Data Steward** del equipo. El dataset original contenía un volumen elevado de columnas y variables, y cada sprint los distintos departamentos requerían subconjuntos distintos. Me encargué de coordinarlo al inicio de cada sprint: identificando qué variables necesitaba cada área, ejecutando la limpieza y selección, y entregando datasets optimizados listos para el análisis. Esto evitó que cada analista cargara y procesara el dataset completo de forma redundante, reduciendo tiempos y garantizando coherencia en los datos de partida para todo el equipo.

---
<sub><img src="https://flagcdn.com/16x12/us.png" alt="US"> English summary</sub>

**Tourism Accommodation Analysis — Gaia Travels**
Final project of the IT Academy Business Simulator (Barcelona Activa). A four-sprint data analysis project simulating a real Data Analytics Department within a fictional tourism company.

**What we built:** Each sprint was structured around a business question posed by Gaia Travels. Sprint 1 was the most demanding — it combined building the full ETL pipeline from scratch (MySQL + CSV) with the initial exploratory analysis. From Sprint 2 onwards, the ETL was only updated when incoming data required it, allowing the team to focus increasingly on analysis and business conclusions: department-level insights → KPI tracking → external benchmarking against real market data → Power BI dashboard and strategic proposals aligned with Spain's Tourism Strategy 2030.

**What made it challenging:** Each sprint introduced a simulated real-world constraint (SQL server down, expired BI licences, shortened deadline + external benchmarking requirement). Sprint 4 required integrating INE (Spanish National Statistics Institute) datasets to benchmark internal KPIs against real market data, all under a reduced deadline.

**My role:** Customer Experience Analyst + team Data Steward — responsible for centralised ETL and weekly dataset preparation for all departments, ensuring each team received clean, scoped data ready for their specific analysis.

**Stack:** Python · pandas · matplotlib · seaborn · Plotly · SQLAlchemy · MySQL · Power BI · Jupyter · Git

---

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE) © 2025 Isanagui Rojas.

---

*Proyecto desarrollado en IT Academy · Barcelona Activa · Simulador Empresarial · 2025*
