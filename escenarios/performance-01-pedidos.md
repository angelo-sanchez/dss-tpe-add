# Performance - Escenario 01 - Gestión de pedidos en alta concurrencia

Durante una campaña de marketing, el volumen de pedidos se incrementa considerablemente, por lo que el microservicio de pedidos debe poder escalar horizontalmente, manteniendo una latencia máxima de 5 segundos durante el pico de demanda. El tráfico debe balancearse para que, al superar el 75% de carga del clúster, el escalado horizontal ocurra en menos de 2 minutos. El sistema debe mantener una tasa de éxito superior al 95% y habilitar reintentos automáticos en caso de fallo.

**Fuente:** Usuarios del sistema.

**Estimulo:** El volumen de pedidos incrementa considerablemente.

**Artefacto:** Microservicio de Pedidos.

**Ambiente:** Durante una campaña de marketing, sistema bajo mucha carga.

**Respuesta:**
- Se produce un escalado horizontal del microservicio de pedidos.
- El tráfico se balancea de manera que las instancias del microservicio no dejen de responder.
- Si algún pedido no se pudo procesar correctamente, se habilita el reintento.

**Medida de Respuesta:**
- El escalado horizontal se realiza al llegar a un 75% de carga en el cluster.
- La instancia nueva está lista para recibir solicitudes en menos de 2 minutos.
- La tasa de pedidos procesados sin falla es mayor a un 95%.
- La latencia en el pico de carga no debe superar los 5 segundos.