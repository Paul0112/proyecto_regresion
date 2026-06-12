# Proyecto de Regresión: USGS Earthquakes 2024

Este proyecto analiza, con enfoque descriptivo-explicativo, cómo se asocia la magnitud reportada de eventos sísmicos USGS durante 2024 con profundidad, localización y características técnicas del registro.

## Fuente y alcance

- Fuente: U.S. Geological Survey, Earthquake Catalog API.
- Periodo: eventos registrados durante 2024.
- Filtro metodológico: magnitud al menos 4.
- Unidad de observación: evento sísmico.

## Ejecución

Se recomienda un entorno Python 3.13 con las versiones fijadas en `requirements.txt`:

    python3.13 -m venv .venv
    source .venv/bin/activate
    python -m pip install -r requirements.txt

1. Abrir `avance_proyecto_corregido.ipynb` desde `Final/` o desde la raíz del proyecto.
2. Ejecutar todas las celdas en orden.
3. El notebook genera la base procesada, figuras, tablas, pruebas, diagnósticos y validaciones.

## Estructura

- `avance_proyecto_corregido.ipynb`: limpieza, EDA, modelos e inferencia.
- `usgs_earthquakes_2024_mag4_raw.csv`: datos crudos.
- `usgs_earthquakes_2024_mag4_model_ready.csv`: base procesada.
- `outputs/`: copias de trabajo.
- `Plantilla_informe/main.tex`: informe LaTeX.
- `Plantilla_informe/figures/` y `Plantilla_informe/tables/`: insumos generados por el notebook.

## Compilación

Desde `Final/Plantilla_informe/`:

    latexmk -C
    latexmk -xelatex -interaction=nonstopmode -file-line-error main.tex

Repositorio: https://github.com/Paul0112/proyecto_regresion

El análisis no busca predecir terremotos futuros ni emitir alertas. Las conclusiones corresponden a asociaciones dentro de la muestra truncada a magnitud mayor o igual a 4.
