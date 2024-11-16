# Desplegabilidad - Escenario 01 - Sensor secundario en los camiones de reparto

**Fuente:** Sensor principal de GPS.

**Estímulo:** Deja de emitir datos.

**Artefacto:** Microservicio de gestión de reparto.

**Ambiente:** Operaciones de reparto en tiempo real.

**Respuesta:**
- El camión de reparto continuará transmitiendo la ubicación con el sensor secundario.
- El sistema recibe los eventos en tiempo real en todo momento.

**Medidas de respuesta:**
- El sensor secundario empieza a funcionar a los 10 segundos desde la detección de la falla.
- El sistema genera un reporte de falla en los primeros 5 minutos desde la detección de la falla.
- El sensor principal se restablece en un periodo de 5 minutos o notifica en caso de persistir la falla.
