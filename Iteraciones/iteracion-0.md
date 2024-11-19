# Iteración 0: Inicio del Proyecto y definición de drivers

Antes de empezar con el proceso de ADD, necesitábamos encontrar cuáles eran los principales drivers y buscar la manera de organizar el repositorio para gestionar la documentación de las decisiones.

En esta primera etapa del proceso, definimos primeramente los requisitos funcionales y buscamos en el planteamiento del problema los atributos de calidad que más sobresalieron y los escribimos en [Atributos de Calidad](/Architectural-Drivers/Atributos%20de%20Calidad.md) para luego desarrollar en base a eso.

## Requerimientos Funcionales

En el caso de los requerimientos funcionales, consideramos que salían directos desde la descripción del sistema. Pensamos en plasmarlos como User Stories o como Casos de Uso, pero al final elegimos una estructura resumida de Casos de Uso para documentar las funcionalidades esperadas del sistema.

Pero, ¿Por qué descartar User Stories como formato para los requerimientos funcionales? Bueno, básicamente vimos y entendimos que la descripción de los requerimientos funcionales podrían ser más claros para nosotros como diseñadores del sistema si los planteamos desde un punto de vista más técnico y no tan centrado en el usuario, y que al fin y al cabo serían muchos tipos de usuarios distintos en este sistema como los clientes, administradores o repartidores.

## Requerimientos no Funcionales - Atributos de Calidad

Identificamos los atributos de calidad según la descripción breve de cada uno de los componentes del sistema y el planteamiento del problema en sí mismo, además, en el caso del atributo de calidad de Modificabilidad y de Performance, si bien no había un requisito o una descripción que se ajustara explícitamente al atributo en sí, son atributos que suelen ser buscados siempre y los cuales suelen ser una gran motivación a la hora de salir de una arquitectura monolítica hacia una de microservicios.

## Resultados de esta “Iteración 0”

- [Carpeta de Architectural Drivers](/Architectural-Drivers/escenarios/)
- [Requerimientos Funcionales](/Architectural-Drivers/Requisitos%20Funcionales.md)
- [Restricciones](/Architectural-Drivers/Restricciones.md)
