Ahora quiero que pienses como un profesional.

Selecciona una herramienta para cada necesidad:

Necesidad	                    Herramienta seleccionada

Base de datos relacional	                Azure SQL Database
Ingesta de datos	                        Azure Data Factory
Almacenamiento	                            Azure Data Lake Storage Gen2
Procesamiento distribuido	                Azure Databricks 
Analítica y Data Warehouse	                Azure Synapse Analytics (Podríamos incorporarlo si el proyecto necesitara capacidades específicas de SQL Analytics o un Data Warehouse.)
Plataforma integrada	                    Microsoft Fabric (Podríamos elegirlo como una alternativa integrada para reducir la cantidad de servicios separados.)
Visualización	                            Power BI

Herramientas disponibles en tus diapositivas:
- Azure SQL Database.
- Azure Data Factory.
- Azure Data Lake Storage Gen2.
- Azure Databricks.
- Azure Synapse Analytics.
- Microsoft Fabric.
- Power BI.

Después justifica tres decisiones:

**1. ¿Por qué utilizaría Azure Data Factory?**

Porque permite realizar la ingesta y orquestación de datos
desde múltiples fuentes, automatizando los procesos de
extracción y carga mediante pipelines.

**2. ¿Por qué utilizaría Azure Data Lake Storage Gen2?**

Porque permite almacenar grandes volúmenes de datos de
diferentes fuentes y organizarlos en las capas Bronze,
Silver y Gold, conservando los datos originales y sus
versiones transformadas.

**3. ¿Por qué utilizaría Databricks o Synapse?**

Utilizaría Azure Databricks cuando necesite procesamiento
distribuido, limpieza, integración y transformación de
grandes volúmenes de datos mediante Apache Spark.

Utilizaría Azure Synapse Analytics cuando el requerimiento
esté orientado principalmente a consultas SQL analíticas
y soluciones de Data Warehouse.

La elección dependerá de las necesidades técnicas y
analíticas del proyecto.

No es necesario utilizar todas las herramientas en una misma solución. Puedes proponer una arquitectura con las que realmente necesitas.

### 1. Azure Data Factory
Se utilizará para realizar la ingesta y orquestación de datos
desde las diferentes fuentes de TecnoStore Perú, permitiendo
crear pipelines que automaticen la extracción y carga de información.

### 2. Azure Data Lake Storage Gen2
Se utilizará como repositorio central para almacenar grandes
volúmenes de datos provenientes de distintas fuentes. Permitirá
organizar la información mediante las capas Bronze, Silver y Gold,
manteniendo los datos originales y las versiones transformadas.

### 3. Azure Databricks
Se utilizará para procesar y transformar los datos mediante
procesamiento distribuido. Permitirá limpiar, integrar y enriquecer
la información para construir las capas Silver y Gold.

### 4. Power BI
Se utilizará para consumir los datos preparados en la capa Gold
y construir dashboards que permitan analizar las ventas,
los productos, los clientes y el inventario.

Necesidad	Herramienta
Ingerir datos	Azure Data Factory
Almacenar datos	ADLS Gen2
Procesar grandes volúmenes	Azure Databricks
Analizar mediante SQL y Data Warehouse	Azure Synapse Analytics
Visualizar información	Power BI

## Arquitectura seleccionada para TecnoStore Perú

Para este proyecto se seleccionan cuatro herramientas principales:

1. Azure Data Factory: ingesta y orquestación de datos.
2. Azure Data Lake Storage Gen2: almacenamiento de datos
   mediante las capas Bronze, Silver y Gold.
3. Azure Databricks: procesamiento distribuido y transformación
   de los datos.
4. Power BI: visualización y elaboración de dashboards.

### Herramientas alternativas

Azure Synapse Analytics podría incorporarse si se requiere
una solución específica de SQL Analytics o Data Warehouse.

Microsoft Fabric podría utilizarse como una plataforma
integrada que reúne capacidades de ingeniería y analítica.

Azure SQL Database podría utilizarse para almacenar información
relacional operativa, si el proyecto requiere implementar
una base de datos transaccional propia.

No es necesario implementar todas las herramientas.
La selección depende de los requerimientos, volumen de datos,
costos y necesidades del negocio.