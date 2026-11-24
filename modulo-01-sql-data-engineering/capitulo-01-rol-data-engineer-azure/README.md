# Chapter 01 — Rol del Data Engineer y Arquitectura de Datos con Azure

## Descripción del proyecto

Este proyecto desarrolla una propuesta conceptual de arquitectura de datos para una empresa ficticia de comercio electrónico llamada **TecnoStore Perú**.

El objetivo es diseñar una solución que permita integrar información procedente de diferentes fuentes, procesarla y organizarla para facilitar el análisis y la toma de decisiones empresariales.

## Objetivos

- Identificar y clasificar las fuentes de datos.
- Diseñar una arquitectura moderna de datos en Azure.
- Aplicar el enfoque Medallion Architecture.
- Seleccionar herramientas adecuadas para la ingesta, almacenamiento, procesamiento y visualización.
- Documentar decisiones técnicas y criterios de calidad de datos.

## Arquitectura propuesta

La arquitectura considera el siguiente flujo:

**Fuentes de datos → Azure Data Factory → Azure Data Lake Storage Gen2 → Databricks → Power BI**

Se utiliza el enfoque Medallion:

- **Bronze:** almacenamiento de datos originales.
- **Silver:** limpieza, estandarización y validación.
- **Gold:** información preparada para el análisis y consumo empresarial.

Consulta el diagrama de arquitectura en `diagrams/`.

## Tecnologías seleccionadas

| Tecnología | Responsabilidad |
|---|---|
| Azure Data Factory | Ingesta y orquestación |
| Azure Data Lake Storage Gen2 | Almacenamiento |
| Azure Databricks | Procesamiento y transformación |
| Power BI | Visualización y análisis |

## Estructura del proyecto

```text
capitulo-01-rol-data-engineer-azure/
├── README.md
├── .gitignore
├── diagrams/
│   └── arquitectura_tecnostore.drawio
└── docs/
    ├── 01_fuentes_datos.md
    ├── 02_capas_medallion.md
    └── 03_seleccion_herramientas.md
```

## Documentación

- [Fuentes de datos](docs/01_fuentes_datos.md)
- [Capas Medallion](docs/02_capas_medallion.md)
- [Selección de herramientas](docs/03_seleccion_herramientas.md)

## Alcance

Este proyecto es una propuesta conceptual y documentada. No representa una implementación desplegada en una suscripción real de Azure.

## Autor

Proyecto desarrollado como parte de mi ruta de aprendizaje en **Data Engineering**.
