# Iteración 3: Cálculo de rutas dinámico

Una vez resuelto el Sistema de pedidos, procedimos a evaluar las prioridades para establecer los objetivos de la iteración, decidimos refinar el microservicio de rutas de la aplicación, ya que está catalogado como parte crítica y debe satisfacer varios Atributos de calidad.

Una de las características más importantes del componente, es la capacidad de poder calcular la ruta con distintos algoritmos basados en diferentes criterios. Aunque el enunciado plantea dos algoritmos y un criterio, entendimos que este diseño debe ser flexible frente a cambios futuros. Por lo tanto, evaluamos conceptos que permitieran desacoplar la implementación interna del microservicio de los algoritmos y criterios específicos. 

Los conceptos más relevantes que encontramos, fueron “Strategy Pattern”, “Template method Pattern”, “Caching”, “Dependency injection”. Para dar con ellos, hicimos uso de herramientas generativas como ArchMind, y ChatGPT

Tras analizar las alternativas, seleccionamos Strategy, Template Method y Caching como las opciones más adecuadas para nuestro problema.

## Strategy
Permite desacoplar el manejador de las requests del algoritmo utilizado para el cálculo de rutas. Esto facilita la selección entre algoritmos existentes y la incorporación de nuevos algoritmos de manera natural y modular.

## Template Method
Define los pasos comunes que deben seguir los algoritmos de cálculo, asegurando consistencia y reduciendo la complejidad al incorporar nuevos algoritmos.

## Caching
Decidimos incorporar una caché de corta duración, que permitiera guardar cálculos para no tener que volver a calcularlos en periodos de tiempo cortos sin sacrificar la fidelidad y precisión de los mismos.

Una vez decididos los patrones y tácticas a utilizar, instanciamos estas soluciones a nuestro problema. Por esto desarrollamos un diagrama de clases que muestre cómo las clases implementan los patrones y un diagrama de secuencia que refleja la interacción en una flujo típico.

## Resultados de la Iteración 3
- [ADR-003](./Architectural-Decision-Records/ADR-003.md)
- [ADR-003 Diagrama de clases](./Architectural-Decision-Records/imagenes/ADR-003-diagrama-de-clases.md)
- [ADR-003 Diagrama de secuencia](./Architectural-Decision-Records/imagenes/ADR-003-diagrama-de-secuencia.md)
