# Confiabilidad - Escenario 01 - Correcto funcionamiento de las incidencias

**Fuente:** El cliente o el trabajador que detecta una incidencia

**Estímulo:** La incidencia que debe ser reportada

**Artefacto:** El microservicio de gestión de incidencias será el encargado de recibir, registrar y comunicar las incidencias detectadas.

**Ambiente:** El sistema opera en un entorno de producción en tiempo real

**Respuesta:**
El sistema debe:

- Registrar la incidencia en un almacenamiento persistente con los detalles necesarios.
- Notificar en tiempo real a los gestores de rutas
- Permitir visualización y consulta de incidencias en un dashboard para los gestores.

**Medidas de respuesta:**
- Tolerancia al fallo: El sistema debe registrar la incidencia con una tasa de éxito del 99.9%, incluso en casos de alta carga o errores en servicios dependientes.
- Latencia de notificación: La incidencia debe notificarse a los gestores en un tiempo no mayor a 2 segundos tras ser detectada.
- Disponibilidad: El microservicio de gestión de incidencias debe mantener una disponibilidad de al menos el 99.95%.
