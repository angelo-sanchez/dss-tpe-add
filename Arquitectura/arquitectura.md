Esta vista muestra cómo interactúan los diferentes microservicios


![Vista Global de la Arquitectura](./imagenes/arquitectura-detalle.jpg)


## Elementos

### Dominio de Pedidos

El Dominio de Pedidos está compuesto por una máquina de estados, representada por varios microservicios que van a estar conectados de manera que en cada microservicio se procese el pedido según el estado que representa y al finalizar el procesamiento, va a pasar el pedido al siguiente microservicio, siguiendo la cadena de estados.
Utiliza una base de datos MongoDB para almacenar el estado de los pedidos, optimizando la escalabilidad y el rendimiento.

Esta arquitectura está orientada a facilitar la modularidad, el monitoreo y la capacidad de adaptación a un entorno asíncrono.

[ADR-002: Domain-Driven Design con Máquina de Estados para el Sistema de Pedidos](/Architectural-Decision-Records/ADR-002.md)


### Clientes

### Rutas

### Pagos


## Backlog (consultar)