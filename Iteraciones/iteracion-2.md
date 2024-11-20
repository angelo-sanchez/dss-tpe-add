# Iteración 2: Sistema de Pedidos

Para resolver el diseño del Sistema de Pedidos, lo más importante a nivel arquitectónico era plantear una clara separación entre las tres fases del pedido. Utilizamos la herramienta ArchMind, que nos ayudó a proponer alternativas de patrones, le dimos el contexto global del problema (el cual estaba definido en el enunciado) y los requerimientos específicos relacionados con este sistema. Aunque la herramienta fue útil para sugerir patrones, notamos cierta inconsistencia, ya que en ocasiones ofrecía diferentes alternativas como "mejor opción" dependiendo de cómo hacíamos nuestras consultas.

Entre las opciones sugeridas por ArchMind, exploramos el patrón Pipeline & Filters, pero no encontramos una manera orgánica de encajar este problema dentro de ese marco. Adaptar el procesamiento de tres etapas a este patrón se sentía forzado y poco natural, aunque en varias ocasiones ArchMind lo señaló como la mejor opción.

Posteriormente, evaluamos State Machine, un enfoque que se ajustaba mucho más a la arquitectura que queríamos plantear. Concebir cada etapa como un “estado” del pedido resultaba intuitivo y encajaba perfectamente con nuestro modelo. Este patrón también fue sugerido por ArchMind en algunas ocasiones como la opción más adecuada.

Por otro lado, consideramos brevemente Chain of Responsibility, pero entendimos que este patrón es más adecuado para problemas síncronos, por lo que decidimos no profundizar en él.

Finalmente, exploramos Domain-Driven Design (DDD), un enfoque que era completamente nuevo para nosotros. Investigamos cómo se había aplicado en el ejemplo de Farmacy Food y analizamos el razonamiento detrás de esta arquitectura. Descubrimos que se ajustaba bien a nuestro problema, y junto con el uso de State Machine, fue la solución que finalmente elegimos.

## Domain-Driven Design (DDD)

Domain-Driven Design es un enfoque diseñado para problemas en los que el modelo de negocio se centra en los elementos que componen el sistema y sus relaciones, reflejando objetos y comportamientos del mundo real. [(Domain-Driven Design: Principios y Beneficios)](https://medium.com/@jonathanloscalzo/domain-driven-design-principios-beneficios-y-elementos-primera-parte-aad90f30aa35).

En nuestro caso, los elementos que definen el dominio son el pedido, sus etapas y los sistemas externos, los cuales interactúan de manera orgánica para completar el procesamiento del pedido.

## Integración de State Machine y DDD

Aplicar el patrón State Machine dentro de un diseño orientado al dominio fue relativamente sencillo. Cada pedido atraviesa una secuencia definida de etapas, y cada etapa debía completarse completamente antes de pasar a la siguiente. Esto corresponde prácticamente a la definición de una máquina de estados: un pedido es la entidad central, y el cumplimiento de una etapa actúa como transición entre estados.

Además, esta solución permite implementar las etapas como microservicios independientes. El bajo acoplamiento y la alta cohesión entre las etapas hacen que cada microservicio sea responsable de validar el pedido en su estado actual y garantizar que cumple los requisitos para avanzar a la siguiente etapa. Esto también habilita un despliegue escalable y modular, mejorando tanto la mantenibilidad como la performance del sistema.

## Resultados de la Iteración 2
- [ADR 002: Domain-Driven Design con Máquina de Estados para el Sistema de Pedidos](/Architectural-Decision-Records/ADR-002.md)
- [Diagrama del dominio de pedidos](/Architectural-Decision-Records/imagenes/ADR-002-ddd-microservicio-pedidos.md)
