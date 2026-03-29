# Scania Predictive Maintenance Project

Proyecto de grado orientado a la priorizacion de mantenimiento predictivo para fallas en el sistema APS de camiones Scania.

## Objetivo

Desarrollar un pipeline reproducible que:

- caracterice el problema de fallas APS
- compare modelos de clasificacion en un contexto desbalanceado
- incorpore costo de error y seleccion de umbral
- genere una salida de priorizacion util para apoyo a decisiones
- alimente un prototipo ligero de visualizacion

## Estructura principal

```text
complaints_thesis/
  app/
    scania_dashboard.py
  data/
    raw/
    processed/
  notebooks/
    scania_project_pipeline.ipynb
    scania_viability.ipynb
  reports/
    scania_project/
      figures/
      tables/
  requirements.txt
```

## Notebook principal

El notebook principal del proyecto es:

- `notebooks/scania_project_pipeline.ipynb`

Este notebook realiza:

- carga y caracterizacion del dataset
- comparacion de modelos base y avanzados
- evaluacion con metricas para clases desbalanceadas
- analisis de costo de error
- seleccion de umbral
- validacion con el conjunto de prueba oficial
- generacion de una tabla de priorizacion

## Prototipo

La aplicacion ligera del proyecto esta en:

- `app/scania_dashboard.py`

Permite visualizar:

- score de falla
- prioridad operativa
- accion recomendada
- comparacion de modelos
- resultados oficiales
- importancia de variables

## Requisitos

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## Datos

Este repositorio no incluye los datasets crudos pesados.

Se espera que los archivos siguientes esten en `data/raw/`:

- `aps_failure_training_set.csv`
- `aps_failure_test_set.csv`
- `aps_failure_description.txt`

## Ejecucion del notebook

Abrir y ejecutar:

```text
notebooks/scania_project_pipeline.ipynb
```

Esto generara tablas y figuras en:

- `reports/scania_project/tables`
- `reports/scania_project/figures`

## Ejecucion del prototipo

```powershell
streamlit run app/scania_dashboard.py
```

## Estado actual

Actualmente el proyecto ya incluye:

- validacion del dataset
- comparacion de modelos
- seleccion de CatBoost como modelo principal
- calibracion de umbral por costo
- validacion en el test oficial
- salida de priorizacion para una futura capa de aplicacion

## Siguiente trabajo

Los siguientes pasos naturales son:

- redaccion del informe tecnico
- interpretacion de variables con mayor contexto de dominio
- refinamiento del prototipo de apoyo a decision
