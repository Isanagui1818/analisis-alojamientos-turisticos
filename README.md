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

## 🗂️ Estructura del repositorio

El trabajo está organizado dentro de la carpeta `Equip_10`, dividida en tres áreas principales que reflejan las fases del análisis: los datos de origen, los scripts de procesamiento agrupados por sprint y los resultados finales entregables.
