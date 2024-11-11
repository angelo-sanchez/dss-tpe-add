# QA-2 - Desplegabilidad

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