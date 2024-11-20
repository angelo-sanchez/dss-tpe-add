# Iteración 4: Integracion de pagos

Una vez completada la iteración sobre rutas dinámicas, evaluamos los inputs y prioridades para definir los objetivos de la siguiente etapa. En esta iteración, nos enfocamos en la integración del microservicio de pagos con la pasarela de MercadoPago, un componente crítico del sistema debido a su impacto directo en la seguridad de los datos y la experiencia del usuario.

La integración con una pasarela de pagos externa introduce desafíos relacionados con el desacoplamiento y la extensibilidad, ya que el sistema debe ser capaz de manejar posibles cambios en la API de MercadoPago, así como la incorporación de nuevas pasarelas en el futuro. Por este motivo, se optó por identificar y evaluar conceptos que garantizaran un diseño robusto y flexible.

Entre las opciones consideradas, los siguientes patrones y tácticas arquitectónicas fueron los más relevantes:

- Gateway Proxy: Proveer una capa de abstracción que gestione todas las interacciones con la API externa.
- Adapter Pattern: Diseñar un adaptador que permita abstraer las dependencias específicas de MercadoPago.
- Event-Driven Design (EDD): Basar la integración en eventos para capturar, procesar y monitorear transacciones de manera flexible.
- ACL (Anti-Corruption Layer): Introducir una capa que traduzca las solicitudes entre el dominio interno del sistema y la pasarela externa, protegiendo la lógica interna de cambios o inconsistencias en la API externa.

Para identificar las mejores prácticas, hicimos uso de herramientas generativas como ArchMind y ChatGPT, lo que nos permitió comparar enfoques basados en atributos de calidad clave, como seguridad, mantenibilidad y extensibilidad.

Finalmente, decidimos adoptar un diseño basado en Gateway Proxy, combinado con Adapter Pattern.

## Gateway Proxy

Este patrón nos ayuda a crear una capa para desacoplar el sistema interno de la API de MercadoPago, asegurando que cualquier cambio en la API externa no afecte directamente al microservicio de pagos. Además, facilitará futuras integraciones con otras pasarelas de pago.

## Adapter Pattern

Este patrón nos permitirá abstraer las diferencias en la implementación de distintas pasarelas de pago, ofreciendo un diseño agnóstico al proveedor seleccionado.

Una vez definidos los patrones y tácticas, procedimos a implementarlos en el diseño, generando una vista asociada que muestra cómo el microservicio de pedidos interactúa con el servicio externo de manera indirecta a través del Gateway Proxy, con un Adapter internamente en el microservicio.

## Resultados de la Iteración 4

- [ADR-004](/Architectural-Decision-Records/ADR-004.md)
- [ADR-004 vista estatica de pagos](/Architectural-Decision-Records/imagenes/ADR-004-vista-estatica-pagos.md)
