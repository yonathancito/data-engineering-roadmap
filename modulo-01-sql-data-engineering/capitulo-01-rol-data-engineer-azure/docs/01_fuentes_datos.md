Fuente	            Tipo de dato	                        ¿Qué información aporta?

SQL Server	        ¿Estructurado?	                        estructurado
API de pagos	    ¿Estructurado o semiestructurado?	    semiestructurado
CSV	                ¿Estructurado?	                        estructurado
ERP	                Depende de su sistema	                estructurado
Eventos web	        ¿Qué tipo de información?	            semiestructurado


¿Cuál de estas fuentes utilizarías para conocer los pedidos?

SQL Server, porque contiene el registro principal de los pedidos.
La API de pagos se utilizaría para consultar las transacciones
relacionadas con esos pedidos.

¿Cuál consultarías para conocer si un pedido fue pagado?

api de pagos

¿Qué información obtendrías del CSV de inventario?

los productos, la fecha de ingreso

¿Por qué sería importante integrar las cinco fuentes?

para poder tener un mejor panorada de los datos y hacer una amalgama de ellos para poder 
sacar mejores conclusiones y resultados.

respuesta: La integración de las fuentes de datos permite centralizar información procedente de diferentes sistemas empresariales, relacionar los registros y obtener una visión más completa del negocio. Esto facilita el análisis, mejora la disponibilidad de información y permite construir reportes confiables para la toma de decisiones.

## Integración y consistencia entre pedidos y pagos

**Objetivo:** Identificar por qué algunos pedidos aparecen como pendientes de pago.

**Fuentes relacionadas:**
- SQL Server: contiene los pedidos y sus datos.
- API de pagos: contiene las transacciones y sus estados.

**Campo de relación:** id_pedido.

**Escenarios que debemos identificar:**
- Pago aprobado.
- Pago rechazado.
- Pago pendiente.
- Sin transacción encontrada.

**Controles de calidad:**
- Verificar pedidos sin transacciones relacionadas.
- Detectar transacciones duplicadas o múltiples intentos de pago.
- Revisar retrasos de sincronización.
- Comprobar paginación y filtros de consulta de la API.

**Regla:** No eliminar pedidos ni asumir un estado de pago cuando no existe
una transacción coincidente. Se debe investigar y conservar la trazabilidad.