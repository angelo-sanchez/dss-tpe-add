# Desplegabilidad - Escenario 02 - Actualización de versión o configuración de un microservicio funcional

El equipo de DevOps debe actualizar la versión o configuración de un microservicio en los entornos de pruebas y producción, sin interrumpir el servicio en funcionamiento. La nueva versión o configuración se implementa luego de superar todas las pruebas automatizadas, manteniendo la disponibilidad del servicio al 99% o más. El proceso de validación automatizada debe completarse en menos de 10 minutos. En caso de que sea necesario un rollback, el sistema debe recuperarse al estado anterior con una tasa de éxito del 100%.

**Fuente:** El equipo de DevOps.

**Estimulo:** Se requiere actualizar la versión o configuración de un microservicio.

**Artefacto:** Microservicio a actualizar.

**Ambiente:** Entorno de Pruebas, Producción.

**Respuesta:**
- La nueva versión o configuración se aplica sin afectar al servicio en funcionamiento.
- La nueva versión o configuración sustituye a la existente luego de pasar todas las pruebas automatizadas.
- La nueva versión o configuración queda desplegada exitosamente.

**Medida de Respuesta:**
- El servicio de cara a los clientes debe permanecer disponible en un 99% de los casos.
- El proceso automatizado de validación de cambios aplicados tarda menos de 10 minutos.
- En caso de rollback, la tasa de recuperación es del 100%.