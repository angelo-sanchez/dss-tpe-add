# Modificabilidad - Escenario 01 - Optimizacion de Algoritmos de rutas.

**Estimulo:** La incorporación del nuevo algoritmo de optimización requiere que el microservicio de Reparto y rutas sea actualizado para utilizar este algoritmo de manera eficiente.

**Fuente:** El cambio es solicitado por el equipo de operaciones logísticas de la empresa, debido a la necesidad de mejorar la precisión y eficiencia del sistema de reparto.

**Ambiente:** Este cambio se implementará en tiempo de desarrollo, con pruebas iniciales en un entorno de staging antes de su despliegue en producción.

**Respuesta esperada:** El equipo de desarrollo debe poder modificar el componente de Reparto y rutas para incluir el nuevo algoritmo sin que esto requiera cambios en otros microservicios que interactúan con él, como los de Incidencias y Estadísticas. Además, el cambio debe realizarse de manera que no interrumpa el funcionamiento del sistema en producción y pueda ser desplegado de manera independiente.

**Medidas de respuesta:**

- Tiempo de implementación: La actualización debe completarse en un plazo inferior a 3 semanas.
- Esfuerzo de desarrollo: El cambio debe realizarse con un esfuerzo inferior a 100 horas de trabajo.
- Despliegue independiente: El microservicio de Reparto y rutas debe poder desplegarse de manera autónoma, sin interrumpir los servicios dependientes.
- Interfaces estables: Las interfaces de este microservicio deben mantenerse consistentes, de modo que otros servicios, como Incidencias y Estadísticas, puedan seguir consumiendo datos sin necesidad de adaptación adicional, minimizando el acoplamiento.
