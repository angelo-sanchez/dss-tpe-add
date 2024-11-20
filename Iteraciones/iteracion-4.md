# Iteración 4 Integracion de pagos

Una vez completada la iteración de rutas dinámicas, evaluamos los inputs y prioridades para definir los objetivos de la siguiente etapa. En esta iteración, nos enfocamos en la integración del microservicio de pagos con la pasarela de MercadoPago, catalogado como un componente crítico del sistema debido a su impacto directo en la seguridad de los datos y la experiencia del usuario.
La integración con una pasarela de pagos externa introduce desafíos relacionados con el desacoplamiento y la extensibilidad, ya que el sistema debe ser capaz de manejar potenciales cambios en la API de MercadoPago o incluso la incorporación de nuevas pasarelas en el futuro. Por este motivo, se optó por identificar y evaluar conceptos que garantizaran un diseño robusto y flexible.

Entre las opciones consideradas, encontramos los siguientes patrones y tácticas arquitectónicas:
- Gateway Proxy: Proveer una capa de abstracción que gestione todas las interacciones con la API externa.
- Adapter Pattern: Diseñar un adaptador que permita abstraer las dependencias específicas de MercadoPago.
- Event-Driven Design (EDD): Basar la integración en eventos para capturar, procesar y monitorear transacciones de manera flexible.
- ACL (Anti-Corruption Layer): Introducir una capa que traduzca las solicitudes entre el dominio interno del sistema y la pasarela externa, protegiendo la lógica interna de cambios o inconsistencias en la API externa.

Para identificar las mejores prácticas, hicimos uso de herramientas generativas como ArchMind y ChatGPT, lo que nos permitió comparar enfoques basados en atributos de calidad clave, como seguridad, mantenibilidad y extensibilidad.
Finalmente, optamos por un diseño basado en Gateway Proxy combinado con un Adapter Pattern.

## Gateway Proxy 
Actuará como la capa principal para desacoplar el sistema interno de la API de MercadoPago, asegurando que cualquier cambio en la API externa no afecte directamente al microservicio de pagos. Esto también facilitará futuras integraciones con otras pasarelas.
## Adapter Pattern
Permitirá abstraer las diferencias en la implementación de distintas pasarelas de pago, ofreciendo un diseño agnóstico al proveedor seleccionado.

Una vez definidos los patrones y tácticas, procedimos a instanciarse en el diseño, generando una vista y sin mayores complicaciones, generando una vista asociada, la cual muestra al microservicio de pedidos, interactuando con el servicio externo de forma indirecta a través del gateway proxy, y un Adapter internamente en le microservicio.

## Resultados de la Iteración 4
[ADR-004](./Architectural-Decision-Records/ADR-004.md)

[ADR-004 vista estatica de pagos](./Architectural-Decision-Records/imagenes/ADR-004-vista-estatica-pagos.md)
