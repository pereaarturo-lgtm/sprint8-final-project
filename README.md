# Sprint 8 Final Project — NovaRetail+

Proyecto de análisis de datos enfocado en explorar las relaciones estadísticas entre variables de comportamiento de clientes de **NovaRetail+**, con especial atención a **suscripciones** y **ventas**.

## Objetivo

El propósito del proyecto es identificar y describir asociaciones entre variables numéricas, binarias y categóricas del comportamiento de los clientes, utilizando métodos de correlación adecuados según el tipo de variable.

El análisis es **correlacional** y no busca establecer relaciones causales.

## Dataset

El proyecto utiliza:

`data/novaretail_comportamiento_clientes_2024.csv`

El dataset contiene **15,000 registros** de clientes e incluye variables de comportamiento, actividad comercial, suscripción y abandono.

Entre las variables analizadas se encuentran:

- `edad`
- `nivel_ingreso`
- `visitas_mes`
- `compras_mes`
- `gasto_publicidad_dirigida`
- `satisfaccion`
- `ingreso_anual`
- `miembro_premium`
- `abandono`
- `tipo_dispositivo`
- `region`

## Metodología

El análisis incluye:

1. Exploración de la estructura y tipos de variables.
2. Revisión de calidad de datos.
3. Estadísticas descriptivas.
4. Visualización de relaciones mediante:
   - Heatmap
   - Pairplot
   - Scatterplots
5. Cálculo de:
   - Pearson
   - Spearman
   - Correlación punto-biserial
   - V de Cramér
6. Interpretación de hallazgos desde una perspectiva de negocio.
7. Revisión de limitaciones y próximos pasos.

## Principales hallazgos

- `compras_mes` e `ingreso_anual` presentan una asociación positiva muy alta.
- `visitas_mes` y `gasto_publicidad_dirigida` muestran una asociación positiva moderada.
- `visitas_mes` también presenta asociaciones positivas con `compras_mes` e `ingreso_anual`, aunque de menor magnitud.
- La mayoría de las asociaciones entre variables binarias/categóricas y métricas de ventas son de magnitud baja.
- `miembro_premium` y `abandono` presentan una asociación categórica detectable, pero débil.

> **Nota:** correlación no implica causalidad. Los resultados describen asociaciones observadas en este conjunto de datos.

## Estructura del repositorio

```text
sprint8-final-project/
├── S8_Student_Version_Project_NovaRetail.ipynb
├── README.md
├── .gitignore
└── data/
    └── novaretail_comportamiento_clientes_2024.csv
```

## Cómo ejecutar el notebook

### Jupyter Notebook / JupyterLab

1. Clona o descarga este repositorio.
2. Abre `S8_Student_Version_Project_NovaRetail.ipynb`.
3. Ejecuta las celdas en orden.

### Google Colab

1. Abre el notebook desde GitHub o súbelo a Google Colab.
2. Asegúrate de que la carpeta `data/` esté disponible en el entorno.
3. Ejecuta las celdas en orden.

El notebook utiliza una ruta relativa para cargar el dataset:

```python
df = pd.read_csv("data/novaretail_comportamiento_clientes_2024.csv")
```

## Dependencias principales

```text
pandas
numpy
matplotlib
seaborn
scipy
```

## Autor

**Arturo Perea García**

Proyecto desarrollado como parte del bootcamp de Data Analytics de TripleTen.
