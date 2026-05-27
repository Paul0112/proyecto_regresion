# Avance Proyecto de Regresión: USGS Earthquakes 2024

Este avance analiza, con enfoque descriptivo-explicativo, cómo se asocia la magnitud reportada (`mag`) de eventos sísmicos USGS durante 2024 con profundidad, localización geográfica y características técnicas del registro.

## Fuente de datos

- Fuente: U.S. Geological Survey, Earthquake Catalog API.
- Periodo: eventos registrados durante 2024.
- Filtro de muestra: magnitud al menos 4.
- Unidad de observación: evento sísmico.
- Archivo crudo: `usgs_earthquakes_2024_mag4_raw.csv`.

## Cómo ejecutar

1. Abrir `avance_proyecto_regresion.ipynb` desde la carpeta `Avance/` o desde la raíz del proyecto.
2. Ejecutar todas las celdas en orden.
3. El notebook genera la base `usgs_earthquakes_2024_mag4_model_ready.csv`, las figuras y las tablas del informe.

## Estructura

- `avance_proyecto_regresion.ipynb`: limpieza, EDA, modelos preliminares y diagnósticos.
- `usgs_earthquakes_2024_mag4_raw.csv`: datos crudos.
- `usgs_earthquakes_2024_mag4_model_ready.csv`: base procesada generada por el notebook.
- `outputs/figures/` y `outputs/tables/`: copias de trabajo.
- `Plantilla_informe/main.tex`: avance en LaTeX.
- `Plantilla_informe/figures/`: figuras leídas por LaTeX.
- `Plantilla_informe/tables/`: tablas leídas por LaTeX.

## Compilación del informe

Compilar `Plantilla_informe/main.tex` con XeLaTeX desde la carpeta `Avance/Plantilla_informe/`:

```bash
latexmk -C
latexmk -xelatex -interaction=nonstopmode -file-line-error main.tex
```

Las figuras y tablas se generan desde el notebook y se cargan con rutas relativas.

## Repositorio

https://github.com/Paul0112/proyecto_regresion

## Nota metodológica

El análisis no busca predecir terremotos futuros ni emitir alertas. Las conclusiones se interpretan como asociaciones estadísticas dentro de la muestra truncada a magnitud >= 4.
