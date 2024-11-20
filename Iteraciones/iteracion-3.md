# Iteración 3 Cálculo de rutas dinámico

Una vez resuelto el Sistema de pedidos, procedimos a evaluar los inputs y prioridades, para establecer los objetivos de la iteración, decidiendo así, refinar el microservicio de rutas de la aplicación, catalogado como parte crítica del sistema, y siendo este además, alcanzado por múltiples Atributos de calidad.

Una de las características más importantes del componente, era la capacidad de poder calcular la ruta con distintos algoritmos basados en un criterio. Si bien el enunciado plantea dos algoritmos, y un criterio, nosotros entendimos qué, esto está sujeto a potenciales cambios, por lo qué optamos por evaluar conceptos qué nos permitieran desacoplar la implementación interna del microservicio, de los algoritmos o criterios seleccionados. 

Los conceptos más relevantes qué encontramos, fueron “Strategy Pattern”, “Template method Pattern”, “Caching”, “Dependency injection”. Para dar con ellos, hicimos uso de herramientas generativas como ArchMind, y CHAT GPT, ade

Finalmente, terminamos decidiendo qué, las mejores opciones son, Strategy, Template, y Caching.

## Strategy
La idea sería qué, el patrón strategy nos permitiera desacoplar al manejador de las request, del algoritmo con el cual tener qué hacerlo, para así poder seleccionar entre los algoritmos existentes, y potencialmente nuevos algoritmos, de manera natural.

## Template method
El objetivo es qué, los algoritmos existentes, tengan qué implementar este patrón, con el objetivo de definir pasos a completar, facilitando la incorporación de nuevos algoritmos

## Caching
Decidimos incorporar una caché de corta duración, qué permitiera guardar cálculos para no tener qué volver a calcularlos en periodos de tiempo cortos, para no sacrificar la fidelidad de los mismos.

Una vez decididos los patrones y tácticas a utilizar, procedimos a instanciarlo a nuestro problema, generando así, un diagrama de clases, mostrando como estas implementan los patrones, y un diagrama de secuencia, mostrando la interacción de las mismas en una secuencia normal.

## Resultados de la Iteración 3
[ADR-003](./Architectural-Decision-Records/ADR-003.md)

[ADR-003 Diagrama de clases](./Architectural-Decision-Records/imagenes/ADR-003-diagrama-de-clases.md)

[ADR-003 Diagrama de secuencia](./Architectural-Decision-Records/imagenes/ADR-003-diagrama-de-secuencia.md)
