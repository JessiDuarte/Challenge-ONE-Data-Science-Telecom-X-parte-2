# Análisis de Cancelación de Clientes

## Descripción
Este proyecto analiza los factores que influyen en la cancelación de clientes utilizando técnicas de **Machine Learning**. Se desarrollaron modelos predictivos y se identificaron las variables más relevantes para proponer estrategias de retención.

## Objetivo
- Predecir la probabilidad de cancelación de clientes.
- Identificar las variables que más impactan en la decisión de cancelar.
- Proponer estrategias de retención basadas en los resultados.

## Datos
El dataset incluye información de clientes con variables como:  
- Datos demográficos: `Genero`, `AdultoMayor`, `Pareja`, `Dependientes`.  
- Información de contrato y servicios: `TipoContrato`, `FacturacionSinPapel`, `MetodoPago`, `ServicioInternet`, `StreamingTV`, `LineasMultiples`, entre otros.  
- Variables económicas: `CargoMensual`, `CargoTotal`.  
- Resultado objetivo: `Evasion` (0 = activo, 1 = canceló).

## Modelos
Se implementaron dos modelos principales:  
1. **Regresión Logística:** Permite interpretar cómo cada variable influye en la cancelación.  
2. **Random Forest:** Modelo más potente que captura relaciones no lineales y calcula la importancia de cada variable.

## Preprocesamiento
- Variables categóricas transformadas a formato numérico mediante **One-Hot Encoding**.  
- Aplicación de **SMOTE** para balancear la clase minoritaria (`Evasion = 1`).  
- Eliminación de columnas irrelevantes como `IDCliente`.  

## Métricas de evaluación
Se evaluaron los modelos utilizando:  
- Exactitud (Accuracy)  
- Precisión  
- Recall  
- F1-score  
- Matriz de confusión

## Resultados principales
- **Random Forest**: mejor desempeño general, predicción más precisa de cancelaciones.  
- **Regresión Logística**: útil para interpretar la influencia de cada variable.  
- Variables críticas: `TiempoClienteMeses`, `CargoTotal`, `TipoContrato`, `FacturacionSinPapel`, `LineasMultiples`.

## Estrategias de retención
- Incentivar la renovación de contratos cortos o recientes.  
- Ofrecer planes personalizados a clientes con cargos altos.  
- Promover el uso de servicios adicionales para clientes con bajo uso.  
- Dar soporte o incentivos a clientes con facturación digital.

## Uso
1. Abrir el cuaderno `analisis_cancelacion.ipynb` en Google Colab.  
2. Ejecutar las celdas en orden para reproducir el análisis y resultados.  
3. Modificar o agregar nuevos modelos según sea necesario.

## Repositorio
Este proyecto se encuentra disponible en GitHub para colaboración y seguimiento del análisis.

