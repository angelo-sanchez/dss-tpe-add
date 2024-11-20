# Iteración 1: Microservicios - Primera aproximación general

En la Iteración 1, partimos de los resultados obtenidos en la Iteración 0, que consistieron en los architectural drivers del sistema: requerimientos funcionales, atributos de calidad y escenarios de calidad. Además, tomamos como referencia la información del sistema monolítico existente que será migrado, y seguimos la restricción que indicaba que la arquitectura resultante debía ser orientada a microservicios.

Con la decisión de adoptar microservicios ya definida por esta restricción, procedimos a explorar algunos patrones de microservicios que nos pudieran ser útiles. Sin entrar en mucho detalle de cada funcionalidad en particular, evaluamos patrones como el Gateway Pattern o Database per Microservice para considerar cómo encajarían en nuestro problema.

Ya habiendo evalueado los patrones de diseño relevantes, los instanciamos en nuestro contexto, lo que nos permitió dibujar una primera versión de la vista general de microservicios.

# Resultados de la Iteración 1
- [ADR 001: Arquitectura basada en microservicios, primera aproximacion](/Architectural-Decision-Records/ADR-001.md)
- [ADR-001 Vista de microservicios](./Architectural-Decision-Records/imagenes/ADR-001-%20arquitectura-general-primera-aproximacion.md)

Habiendo registrado las decisiones, entendimos que los objetivos de la iteración se cumplieron: logramos obtener una primera aproximación de la arquitectura orientada a microservicios.
