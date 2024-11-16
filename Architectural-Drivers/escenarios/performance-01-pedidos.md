# Performance - Escenario 01 - Tiempos de respuesta degradados en alta concurrencia

**Fuente:** Usuarios del sistema.

**Estimulo:** El volumen de pedidos incrementa considerablemente.

**Artefacto:** Microservicio de Pedidos.

**Ambiente:** Durante una campaña de marketing, tiempos de respuesta degradados.

**Respuesta:**
- Se produce un escalado horizontal del microservicio de pedidos.
- El balanceo de carga permite restablecer el modo de operación normal.

**Medida de Respuesta:**
- La latencia en el pico de carga no debe superar los 5 segundos.
- El periodo de degradación del servicio no debe superar los 2 minutos.
