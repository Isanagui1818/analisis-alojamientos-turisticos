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

## 🗂️ Estructura del repositorio

El trabajo está organizado dentro de la carpeta `Equip_10`, dividida en tres áreas principales que reflejan las fases del análisis: los datos de origen, los scripts de procesamiento agrupados por sprint y los resultados finales entregables.

```
analisis-alojamientos-turisticos/
├── Equip_10/
│   ├── Data/                  # Datasets originales (CSV, fuentes INE)
│   ├── Scripts/
│   │   ├── Sprint_1/          # ETL + EDA general, EDA por áreas
│   │   ├── Sprint_2/          # Análisis especializado por departamento
│   │   ├── Sprint_3/          # KPIs, visualizaciones interactivas (Plotly)
│   │   ├── Sprint_4/          # Variaciones anuales, pernoctaciones, Power BI
│   │   └── README.md
│   └── Results/
│       ├── Sprint_1/          # Primeros resultados y dashboard inicial
│       ├── Sprint_2/          # Presentaciones y análisis por rol
│       ├── Sprint_3/          # Gráficos interactivos HTML
│       └── Sprint_4/          # Dashboard BI final + propuestas de negocio
├── Guia Git i GitHub.pdf
├── LICENSE
└── README.md
```

---

## 🔄 Metodología: 4 Sprints

### Sprint 1 — ETL + EDA General
Conexión a la base de datos MySQL (`Tourist_Accommodation`), carga de datos con SQLAlchemy y pandas, limpieza y transformación de variables (`bathrooms`, `bedrooms`, `beds`), imputación de nulos por medianas agrupadas y primeras exploraciones estadísticas y visuales con matplotlib y seaborn.

### Sprint 2 — Análisis por Departamentos
Análisis especializados según los roles del equipo: marketing y comunicación, experiencia del cliente y operaciones. Cada área profundizó en las variables relevantes para su dominio, generando visualizaciones propias y conclusiones parciales.

### Sprint 3 — KPIs e Indicadores de Negocio
Definición y cálculo de los KPIs principales del proyecto: tasa de ocupación mensual, índice de satisfacción general, ciudad con mayor ocupación e ítem con mayor valoración. Generación de dashboards interactivos en HTML con Plotly (`fig1_ocupacion`, `fig2_satisfaccion`, `fig3_ciudad`, `fig4_item`).

### Sprint 4 — Análisis Macroeconómico y Entregables Finales
Análisis de variaciones anuales de viajeros, pernoctaciones y estancia media. Segmentación por comunidades autónomas, provincias y país de residencia del viajero. Limpieza y exportación de datasets optimizados para Power BI. Entrega del dashboard final (`Presentación BI.pbix`) y documentos de propuestas de negocio.

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
          - Gráficos Plotly interactivos en HTML listos para integrar en presentaciones o web

          ---

          ## 👥 Equipo — Equip 10

          | Rol | Área |
          |---|---|
          | Analista de Marketing y Comunicación | Segmentación, posicionamiento, tendencias |
          | Analista de Perfil del Cliente | Comportamiento, valoraciones, tipología |
          | Analista de Operaciones | Gestión de inventario, capacidad, eficiencia |
          | Analista de Experiencia del Cliente | Satisfacción, puntuaciones, reviews |
          | Analista de Finanzas y Riesgo | Variaciones, KPIs económicos |
          | Responsable de Calidad del Repositorio *(rol rotativo)* | Revisión, merge, estándares de código |
          | **Mentora / Directora del Departamento** | Facilitación y orientación técnica |

          ---

          ## ⚙️ Cómo reproducir el análisis

          1. Clona el repositorio:
             ```bash
                git clone https://gitlab.com/fueAtlas/analisis-alojamientos-turisticos.git
                   ```

                   2. Instala las dependencias principales:
                      ```bash
                         pip install pandas matplotlib seaborn plotly sqlalchemy pymysql jupyter
                            ```

                            3. Navega a la carpeta del equipo:
                               ```bash
                                  cd Equip_10/Scripts/
                                     ```

                                     4. Ejecuta los notebooks en orden de sprint (Sprint_1 → Sprint_4).

                                     > **Nota:** Los notebooks que se conectan a MySQL requieren acceso a la base de datos del proyecto. Para el análisis con CSVs locales, los archivos necesarios están incluidos en cada carpeta de sprint.

                                     ---

                                     ## 📄 Licencia

                                     Este proyecto está bajo la licencia [MIT](LICENSE) © 2026 Isanagui Rojas.

                                     ---

                                     *Proyecto desarrollado en IT Academy · Barcelona Activa · Simulador Empresarial · 2025*