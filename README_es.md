**🌐 Idioma:** [English](README_en.md) · Español

# 🏨 Análisis de alojamiento turístico — Gaia Travels
> Proyecto final del Simulador de Empresa · IT Academy Barcelona Activa · Equipo 10

---

## 📋 Visión general del proyecto

Este proyecto simula el trabajo real de un **Departamento de Data Analytics** dentro de una empresa turística ficticia llamada **Gaia Travels**. A lo largo de cuatro sprints, el equipo llevó a cabo un análisis integral del mercado español de alojamiento turístico: desde la extracción y limpieza de datos hasta la generación de KPIs, las visualizaciones interactivas y un dashboard en Power BI con propuestas de negocio accionables.

El proyecto se desarrolló en el marco del **Simulador de Empresa de IT Academy (Barcelona Activa)**, un entorno de aprendizaje que replica las dinámicas de trabajo profesionales — reuniones de equipo, gestión ágil con un tablero Kanban, roles especializados y presentaciones semanales de resultados.

---

## 🎯 Objetivos

- Aplicar un flujo completo de análisis de datos (ETL → EDA → KPIs → Visualización → Propuestas)
- Analizar el comportamiento de los alojamientos turísticos en España: ocupación, pernoctaciones, perfil del viajero y satisfacción del cliente
- Identificar patrones de estacionalidad, variaciones anuales y origen del viajero
- Construir un dashboard interactivo en Power BI para apoyar la toma de decisiones de negocio
- Desarrollar propuestas de negocio concretas alineadas con la **Estrategia de Turismo de España 2030**

---

## ⚡ Hándicaps tecnológicos semanales

Una de las características más distintivas del simulador fue la introducción de un **hándicap tecnológico cada semana**, simulando restricciones inesperadas del mundo real. Al publicarse los datos de un nuevo sprint, el equipo recibía una restricción técnica adicional que obligaba a replantear el enfoque y a encontrar soluciones alternativas.

| Semana | Restricción simulada | Solución adoptada |
|---|---|---|
| Sprint 1 | Sin restricción — sprint inicial | — |
| Sprint 2 | Servidor SQL caído — datos inaccesibles por base de datos | Datos entregados como CSV · carga directa con pandas |
| Sprint 3 | Licencias de Power BI caducadas | Visualizaciones alternativas con Plotly y matplotlib |
| Sprint 4 | Plazo reducido (entrega el jueves) + requisito de benchmarking externo | Integración del dataset del INE · priorización de tareas · coordinación intensiva del equipo |

> El Sprint 4 combinó dos presiones simultáneas: un plazo de entrega acortado y la petición de la empresa de comparar los datos internos con datos reales del mercado turístico español. Esto requirió incorporar y cruzar fuentes externas del **Instituto Nacional de Estadística (INE)** para contextualizar los KPIs de Gaia Travels dentro del comportamiento real del sector, fundamentando las propuestas estratégicas de negocio sobre datos objetivos.

> Este mecanismo entrenó la capacidad del equipo para **adaptarse a entornos con recursos limitados**, tomar decisiones técnicas bajo presión y encontrar soluciones alternativas sin comprometer la calidad del análisis — una habilidad directamente transferible a un entorno profesional real.

---

## 🔄 Metodología: 4 Sprints

Cada sprint se estructuró en torno a una **pregunta de negocio** planteada por Gaia Travels. El equipo debía responderla utilizando los datos disponibles, respetando el hándicap tecnológico de la semana y entregando resultados accionables. El Sprint 1 fue el más exigente, combinando la construcción completa del pipeline ETL con el primer análisis exploratorio. A partir del Sprint 2, el ETL se mantuvo o se actualizó solo cuando los datos del nuevo sprint introducían cambios estructurales, lo que permitió al equipo centrarse progresivamente en el análisis y las conclusiones de negocio.

### Sprint 1 — ETL + EDA general *(el más exigente)*
**Pregunta de negocio:** ¿Cuál es el estado actual del mercado español de alojamiento turístico y qué variables explican mejor el comportamiento de la oferta?

Construcción completa del pipeline ETL: conexión a la base de datos MySQL (`Tourist_Accommodation`) mediante SQLAlchemy y pandas, limpieza y transformación de variables (`bathrooms`, `bedrooms`, `beds`), imputación de nulos por medianas agrupadas. El dataset resultante se utilizó para el EDA general con una primera exploración estadística y visual usando matplotlib y seaborn. Este sprint estableció el dataset limpio sobre el que se construirían todos los sprints posteriores.

### Sprint 2 — Análisis por departamentos
**Pregunta de negocio:** ¿Qué insights específicos puede extraer cada área de negocio (marketing, operaciones, experiencia de cliente) para mejorar la toma de decisiones?

Cada analista abordó la pregunta desde su área de especialización, profundizando en las variables relevantes para su dominio. El ETL se actualizó para incorporar los nuevos datos entregados como CSV tras la caída del servidor SQL (hándicap de la semana).

### Sprint 3 — KPIs e indicadores de negocio
**Pregunta de negocio:** ¿Cuáles son los indicadores clave de rendimiento de Gaia Travels y cómo evolucionan?

Definición y cálculo de los principales KPIs: tasa de ocupación mensual, índice global de satisfacción, ciudad con mayor ocupación e ítem mejor valorado. Dadas las licencias de Power BI caducadas (hándicap), se generaron dashboards interactivos alternativos en HTML con Plotly (`fig1_ocupacion`, `fig2_satisfaccion`, `fig3_ciudad`, `fig4_item`).

### Sprint 4 — Benchmarking externo y propuestas estratégicas
**Pregunta de negocio:** ¿Cómo se compara Gaia Travels con el mercado turístico español real y hacia dónde debe dirigir su estrategia?

La empresa solicitó comparar los datos internos con el comportamiento real del sector. Se integraron datasets del **INE** (viajeros, pernoctaciones, estancia media, variaciones anuales por comunidad autónoma y país de residencia) para contextualizar los KPIs internos dentro del mercado real. Los hallazgos sustentaron propuestas estratégicas de negocio alineadas con la **Estrategia de Turismo de España 2030**, todo ello entregado bajo un plazo reducido (hándicap de la semana).

---

## 📊 Stack tecnológico

| Herramienta | Uso |
|---|---|
| **Python** | Análisis, limpieza y visualización de datos |
| **pandas** | Manipulación y transformación de DataFrames |
| **matplotlib / seaborn** | Visualizaciones estáticas y EDA |
| **Plotly Express** | Gráficos interactivos exportados como HTML |
| **SQLAlchemy** | Conexión y consulta de la base de datos MySQL |
| **MySQL** | Base de datos principal (`Tourist_Accommodation`) |
| **Power BI** | Dashboard interactivo final |
| **Jupyter Notebook** | Entorno de desarrollo y documentación |
| **Git / GitHub** | Control de versiones y colaboración del equipo |

---

## 📁 Estructura del repositorio

```
Equip_10/
├── Data/        datasets por sprint (ver Data/README_es.md)
├── Scripts/     notebooks por sprint: ETL, EDA, KPIs (ver Scripts/README_es.md)
└── Results/     presentaciones y entregables por sprint (ver Results/README_es.md)
```

## 📁 Fuentes de datos

Los datos son **ficticios**, generados para el simulador con una estructura realista basada en el mercado español de alojamiento turístico.

**Cobertura geográfica:** Barcelona · Girona · Madrid · Mallorca · Menorca · Sevilla · Valencia

- **Base de datos MySQL**: tabla `Tourist_Accommodation` con datos de apartamentos turísticos (id, nombre, descripción, tipo de habitación, barrio, anfitrión, baños, dormitorios, camas, precio, valoraciones, etc.)
- **Datasets del INE (Instituto Nacional de Estadística)**:
  - Viajeros y pernoctaciones por comunidad autónoma y provincia
  - Viajeros y pernoctaciones por punto turístico
  - Viajeros y pernoctaciones según país de residencia
  - Coeficiente de variación de viajeros y pernoctaciones
  - Variación anual de estancia media, establecimientos, ocupación y empleados

---

## 📈 Resultados principales

- **Dashboard en Power BI** con páginas dedicadas a ocupación, satisfacción del cliente, perfil del viajero y variaciones temporales
- **KPIs monitorizados**: tasa de ocupación mensual, índice global de satisfacción, rankings de ciudad e ítem
- **Propuestas de negocio** documentadas con recomendaciones estratégicas para Gaia Travels
- Análisis de tendencias alineado con la **Estrategia de Turismo de España 2030**
- Benchmarking externo con fuentes del INE para validar los datos internos frente a cifras reales del mercado
- Gráficos interactivos en HTML con Plotly listos para incrustar en presentaciones o páginas web

---

## 👥 Equipo — Equipo 10

| Rol | Área |
|---|---|
| **Analista de Experiencia de Cliente + Data Steward** ⬅️ *mi rol* | Satisfacción, valoraciones y reseñas · ETL centralizado y preparación de datasets para todos los departamentos |
| Analista de Marketing y Comunicación | Segmentación, posicionamiento, tendencias |
| Analista de Perfil de Cliente | Comportamiento, valoraciones, tipología |
| Analista de Operaciones | Gestión de inventario, capacidad, eficiencia |
| Analista de Finanzas y Riesgo | Variaciones, KPIs económicos |
| Responsable de Calidad del Repositorio *(rol rotativo)* | Revisión, merge, estándares de código |
| **Mentor / Director del Departamento** | Facilitación técnica y guía |

### 🔧 Mi contribución específica

Además de mis responsabilidades de análisis de experiencia de cliente, asumí el rol transversal de **Data Steward** del equipo. El dataset original contenía un gran número de columnas y variables, y cada sprint los distintos departamentos requerían subconjuntos diferentes. Coordiné esto al inicio de cada sprint: identificando qué variables necesitaba cada área, ejecutando la limpieza y la selección, y entregando datasets optimizados y listos para el análisis. Esto evitaba que cada analista cargara y procesara el dataset completo de forma redundante, reduciendo el tiempo de procesamiento y garantizando la consistencia de los datos de partida en todo el equipo.

---

*Proyecto desarrollado en IT Academy · Barcelona Activa · Simulador de Empresa · 2025*
