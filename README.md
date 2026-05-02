# 📊 Panel de Auditoría de Base de Datos

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Backend-Python%203.10%2B-blue.svg)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-FF4B4B.svg)](https://streamlit.io/)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791.svg)](https://www.postgresql.org/)

> **Panel de Auditoría de Base de Datos** es una solución interactiva que permite el monitoreo en vivo de transacciones y la auditoría detallada de bases de datos relacionales en PostgreSQL. Diseñado con una interfaz web ágil, incorpora características avanzadas como la generación de scripts de reversión (rollbacks) y el análisis histórico mediante archivos CSV. Desarrollado como proyecto académico para la Escuela Profesional de Ingeniería de Sistemas de la Universidad Privada de Tacna.

---

## 📋 Descripción

Este sistema proporciona una plataforma centralizada para administrar y auditar eventos de la base de datos. Construido con **Python** y el framework **Streamlit**, el aplicativo se conecta a la base de datos utilizando **Psycopg2** para capturar cambios y ofrece módulos para la carga e inspección de reportes de auditoría exportados.

### ✨ Características Principales

| Módulo | Descripción |
|:-------|:------------|
| 📡 **Monitoreo en Vivo** | Seguimiento en tiempo real de las operaciones y transacciones de la base de datos mediante la vista `1_Monitoreo_Vivo.py`. |
| 📁 **Cargador de CSV** | Importación y análisis de reportes de auditoría históricos mediante `2_Cargador_CSV.py`, utilizando la librería Pandas para el manejo de datos. |
| ⏪ **Generación de Rollbacks** | Funcionalidad para la creación automatizada de scripts de reversión SQL, permitiendo deshacer cambios no deseados o alteraciones a nivel lógico. |
| 🔌 **Gestor de Conexión** | Módulo dedicado (`database.py`) para administrar las conexiones y ejecutar consultas de forma modular. |

---

## 🛠️ Tecnologías Utilizadas

El proyecto define sus dependencias en el archivo `requirements.txt`:

*   **Lenguaje:** Python 3.10+
*   **Framework Web:** `streamlit`
*   **Manipulación de Datos:** `pandas`
*   **Controlador de Base de Datos:** `psycopg2-binary` (Driver para PostgreSQL)

---

## 🚀 Ejecución del Sistema

El proyecto está diseñado para un despliegue rápido y sencillo utilizando el servidor integrado de Streamlit.

### 1. Instalar dependencias
Asegúrate de tener Python instalado y ejecuta el siguiente comando en la raíz del proyecto para instalar las librerías necesarias:
```bash
pip install -r requirements.txt

---
## Iniciar la aplicación
Ejecuta el archivo principal app.py con el motor de Streamlit:
streamlit run app.py

---
###📁 Estructura del Proyecto
La organización del repositorio separa la lógica principal, las vistas de la interfaz, los datos de prueba y la documentación:
proyecto-auditoria-bd/
├── 📄 app.py                  # Punto de entrada de la aplicación Streamlit
├── 📄 database.py             # Lógica de conexión y ejecución de sentencias SQL
├── 📄 requirements.txt        # Dependencias del proyecto (streamlit, pandas, psycopg2)
│
├── 📂 pages/                  # Vistas secundarias del panel
│   ├── 📄 1_Monitoreo_Vivo.py # Dashboard de auditoría en tiempo real
│   └── 📄 2_Cargador_CSV.py   # Módulo de carga y lectura interactiva de reportes
│
├── 📂 CSV-tests/              # Archivos de prueba para el módulo de carga CSV
│   ├── 📄 reporte_auditar_prueba.csv
│   ├── 📄 reporte_auditar_prueba_2.csv
│   └── 📄 testbd.csv
│
├── 📂 docs/                   # Documentación formal del proyecto
│   ├── 📄 FD01 a FD06 (Informes de Factibilidad, Visión, Requerimientos, Arquitectura, Proyecto Final)
│
└── 📂 media/                  # Recursos gráficos
    └── 🖼️ logo-upt.png        # Logotipo institucional de la universidad

---
##👥 Equipo de Desarrollo
###Integrantes:
-Colque Quispe, Rodrigo Sídney (2023077078)
-Ramos Atahuachi, Fabricio Farid Edmilson (2023076798)
Docente: Mag. Patrick Cuadros Quiroga — Curso: Calidad y Pruebas de Software / Base de Datos
Universidad Privada de Tacna — Facultad de Ingeniería — Escuela Profesional de Ingeniería de Sistemas
