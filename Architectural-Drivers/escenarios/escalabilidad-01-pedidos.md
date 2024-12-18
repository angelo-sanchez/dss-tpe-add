# Escalabilidad - Escenario 01 - Escalado de componente de Pedidos

**Estímulo:** El sistema experimenta un incremento del 400% en la cantidad de pedidos por hora debido a una promoción especial.

**Fuente:** Usuarios legítimos (clientes) realizando pedidos de manera masiva durante la promoción.

**Ambiente:** Tiempo de ejecución en el entorno de producción, durante un evento de alta demanda.

**Respuesta esperada:** El sistema debe escalar automáticamente el microservicio de Pedidos para gestionar la carga adicional y asegurar que cada pedido pase por sus fases, sin demoras significativas.

**Medidas de respuesta:**

- Escalabilidad automática: El sistema debe activar la escalabilidad automática, añadiendo nuevas instancias del microservicio de Pedidos en menos de 30 segundos al detectar el aumento de carga.
- Integridad en el procesamiento de pedidos: Cada pedido debe ser procesado correctamente y sin duplicados en cada una de las fases.
- Registro de eventos y monitoreo: El sistema debe registrar todos los pedidos procesados y cada ajuste de escalabilidad, permitiendo al equipo de soporte monitorear el rendimiento en tiempo real.
