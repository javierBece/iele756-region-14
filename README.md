# iele756-region-14

# Tarea 0 — Setup & First Contact with All Three Datasets

Resumen
- Proyecto: Tarea 0 (IELE756) — análisis inicial de tres fuentes: Censo 2024, ENO y GRD.
- Equipo: Jose Pino y Javier Becerra
- Región: XIV - Los Ríos
- Notebook principal: Tarea 0 PyAD.ipynb

Datasets utilizados
- Parte 1 (Censo):
	- viviendas_censo2024.parquet
	- personas_censo2024.parquet
	- hogares_censo2024.parquet
- Parte 2 (ENO):
	- 20241218_base_eno_final.csv
- Parte 3 (GRD):
	- GRD_PUBLICO_2024.zip
	- CIE-10.xlsx

Ejecución (VS Code o Google Colab)
- VS Code (recomendado):
	1. Crear y activar un `venv` en la carpeta del proyecto.
	2. Instalar dependencias: `python -m pip install --upgrade pip setuptools wheel` y `python -m pip install pandas matplotlib openpyxl jupyter`.
	3. Abrir `Tarea 0 PyAD.ipynb` y ejecutar las celdas en orden.

- Google Colab:
	- Opción A: Subir los archivos de datos directamente al entorno de Colab (panel izquierdo > Files > Upload).
	- Opción B: Montar Google Drive y colocar los datasets en una carpeta; luego usar `from google.colab import drive; drive.mount('/content/drive')` y ajustar rutas.
	- Instalar paquetes en Colab si faltan: `!pip install openpyxl`.

Requisitos
- Python 3.9+
- Paquetes: `pandas`, `matplotlib`, `openpyxl`, `jupyter`.

Notas técnicas
- En el Censo la columna `region` es numérica (ej.: `14` = Los Ríos). Filtrar con `persona[persona['region']==14]`.
- En el GRD la columna `COMUNA` está en mayúsculas; en el notebook se incluyeron las 12 comunas de la Región de Los Ríos para filtrar con `.isin()`.
- En el ENO la columna `region` es texto (ej.: "Región de Los Ríos"). Filtrar con `eno[eno['region']=="Región de Los Ríos"]`.
- Para gráficos, se usó `matplotlib` con estilos básicos. Se ordenaron los valores para mejorar la visualización.

Contacto
- Autor/es: Jose Pino y Javier Becerra
- Emails: jospinom@udd.cl y jabecerram@udd.cl
- Fecha: 12-03-2026

Enunciado técnico y entregables
- Puntos: 5.
- Objetivo: cargar, inspeccionar y filtrar los tres datasets (Censo, ENO, GRD) para la región asignada. No se requiere análisis profundo.
- Fechas: Released 05-03-2026 — Due 15-03-2026.

Entregables obligatorios
1. PDF exportado del notebook con todas las celdas ejecutadas y salidas visibles.
2. Link público al repositorio GitHub que contenga el notebook y este `README.md`.

Requisitos técnicos del notebook
- Mostrar carga e inspección básica de cada dataset: `.shape`, `.info()`, `.head()`, `.value_counts()`.
- Filtrar Censo por código numérico de `region` (ej.: `persona[persona['region']==14]`).
- Filtrar ENO por texto en `region` (ej.: `eno[eno['region']=="Región de Los Ríos"]`).
- Filtrar GRD por lista de comunas en mayúsculas usando `.isin()` sobre `COMUNA`.
- Incluir los gráficos solicitados en las Partes 2 y 3 (distribución por año, top-5, etc.).

Datasets usados (ubicación esperada o nombre de archivo)
- Parte 1 (Censo): `viviendas_censo2024.parquet`, `personas_censo2024.parquet`, `hogares_censo2024.parquet`.
- Parte 2 (ENO): `20241218_base_eno_final.csv`.
- Parte 3 (GRD): `GRD_PUBLICO_2024.zip`, `CIE-10.xlsx`.

Referencias
- Enunciado completo: `Tarea0.md` (carpeta `Tarea 0`).
- Material adicional: `iele26-1-3datasets.pdf`.
