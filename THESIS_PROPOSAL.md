# Propuesta Base de Tesis

## Titulo tentativo

Marco reutilizable para la priorizacion y el monitoreo de reclamaciones mediante analitica de metadatos y validacion temporal.

## Problema

Las organizaciones reciben grandes volumenes de reclamaciones y solicitudes. Aunque existen metadatos operativos asociados a esos casos, con frecuencia no se aprovechan para apoyar la priorizacion y el seguimiento sistematico de la atencion. Se requiere un enfoque reproducible y adaptable que permita transformar datos administrativos en informacion util para la gestion.

## Pregunta de investigacion

Como disenar y evaluar un pipeline analitico reproducible, basado en metadatos de reclamaciones, que permita priorizar y monitorear casos de manera reusable a traves del tiempo?

## Objetivo general

Desarrollar y evaluar un pipeline reproducible de analitica de reclamaciones basado en metadatos operativos, utilizando cortes temporales y validacion con datos actualizados.

## Objetivos especificos

1. Caracterizar la estructura temporal y operacional de un dataset publico de reclamaciones.
2. Construir un corte fijo de entrenamiento que garantice reproducibilidad metodologica.
3. Entrenar un modelo baseline para una tarea operativa, como puntualidad de respuesta o categoria de reclamacion.
4. Evaluar el comportamiento del pipeline con datos posteriores al corte inicial.
5. Proponer lineamientos para adaptar la metodologia a otros contextos organizacionales.

## Aporte esperado

- una metodologia reproducible
- una validacion temporal realista
- un pipeline reutilizable
- una base para extender el proyecto luego a texto libre, drift o dashboards

## Conexion con este repositorio

- `scripts/download_cfpb.py`: descarga del dataset base
- `scripts/register_local_raw.py`: alternativa para cargar un CSV descargado manualmente
- `scripts/freeze_snapshot.py`: congelamiento del corte temporal
- `scripts/train_metadata_baseline.py`: modelo baseline
- `scripts/evaluate_update.py`: validacion con datos posteriores
