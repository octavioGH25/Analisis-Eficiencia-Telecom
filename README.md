# 📡 Análisis de Eficiencia Operativa en Call Center de Telecomunicaciones

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat&logo=python&logoColor=white) ![Tableau](https://img.shields.io/badge/Tableau-Business_Intelligence-E97627?style=flat&logo=tableau&logoColor=white) ![Statistics](https://img.shields.io/badge/Statistics-Mann_Whitney_U-purple)

## 📋 Resumen Ejecutivo
En la industria de Contact Centers, la eficiencia no se mide solo por el volumen de llamadas, sino por la calidad de la atención y la gestión del tiempo.

Este proyecto aborda un problema de negocio crítico: la identificación precisa de **operadores ineficaces**. Utilizando un dataset de **53,900 registros**, desarrollé un modelo analítico en Python que va más allá de los promedios simples, utilizando **pruebas de hipótesis estadísticas** para segmentar el rendimiento del personal y proponer mejoras operativas.

---

## 🎯 El Desafío (Business Problem)
La gerencia necesitaba una metodología objetiva para detectar a los operadores que no cumplían con los estándares de servicio. El reto era traducir el concepto subjetivo de "ineficacia" en métricas cuantificables.

Se definieron tres vectores de ineficiencia:
1.  Alto índice de **Llamadas Perdidas** (Abandono).
2.  Tiempos de **Espera Prolongados** (Customer Friction).
3.  Baja productividad en **Llamadas Salientes**.

---

## ⚙️ Metodología y Enfoque Técnico
Implementé un flujo de trabajo analítico riguroso ("Data-Driven Decision Making"):

1.  **Limpieza y ETL:** Procesamiento de datos crudos, corrección de tipos de datos y manejo de valores nulos críticos (`operator_id`).
2.  **Ingeniería de Características (Feature Engineering):** * Cálculo de `Tiempos de Espera` reales.
    * Creación de flags booleanos para direccionalidad de llamadas.
    * Agregación de métricas por operador (Pivot Tables).
3.  **Definición de Umbrales Estadísticos:** En lugar de usar promedios arbitrarios, utilicé **Cuartiles (Q1 y Q3)** para definir los límites de rendimiento "Alto" y "Bajo".
4.  **Validación Estadística (A/B Testing):** Apliqué la **Prueba U de Mann-Whitney** para confirmar que la diferencia entre operadores "Eficaces" e "Ineficaces" era estadísticamente significativa (p-value < 0.05), descartando el azar.

---

## 🚀 Hallazgos Clave e Impacto

> *El análisis permitió segmentar la fuerza laboral con precisión quirúrgica:*

* **Diagnóstico de Entrada:** Se identificaron **40 operadores críticos** que combinan un alto tiempo de espera con una alta tasa de abandono.
* **Diagnóstico de Salida:** Se detectaron **89 operadores** con una producción de llamadas salientes significativamente inferior al estándar (Q1).
* **Certeza Estadística:** La prueba de hipótesis confirmó con una confianza superior al 95% que estos grupos requieren intervención inmediata (capacitación o revisión).

---

## 📊 Visualización y Dashboard

Para la presentación ejecutiva, los resultados se integraron en un Dashboard interactivo de Tableau y una presentación de alto nivel.

| **Dashboard Interactivo** | **Presentación Ejecutiva** |
| :---: | :---: |
| [![Tableau](https://img.shields.io/badge/Ver_en-Tableau_Public-E97627?style=for-the-badge&logo=tableau)](https://public.tableau.com/views/Dashboard_del_Proyecto_Final_14/Dashboard1?:language=es-ES&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) | [![Gamma](https://img.shields.io/badge/Ver_Presentación-Gamma-purple?style=for-the-badge)](https://gamma.app/docs/Analisis-de-Operadores-de-Telecomunicaciones-mu6u9sn4yl96tlo) |

### Vista Previa del Análisis
![Dashboard Preview](dashboard_telecom.png)
*(Captura de análisis de distribución de llamadas)*

---

## 🛠️ Stack Tecnológico
* **Python:** Manipulación de datos y lógica de negocio.
* **Pandas & NumPy:** Agregación de datos y cálculo vectorial.
* **SciPy (Stats):** Pruebas de hipótesis (Mann-Whitney U).
* **Seaborn / Matplotlib:** Análisis Exploratorio de Datos (EDA).
* **Tableau:** Business Intelligence y Dashboards.

---
**Autor:** Octavio Landa Verde

*Analista de Datos | Especialidad en Finanzas y Control Interno*
