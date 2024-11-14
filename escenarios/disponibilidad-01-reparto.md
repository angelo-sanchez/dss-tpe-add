# Desplegabilidad - Escenario 01 - Sensor secundario en los camiones de reparto

El sensor principal de GPS deja de emitir datos de ubicación, por lo que el sistema cambia automáticamente al sensor secundario, que tiene menor precisión, para poder mantener el seguimiento de los camiones en reparto. Durante la falla, el sistema debe registrar en tiempo real todos los errores detectados en los sensores y generar un reporte de fallas detallado. El sistema tiene un tiempo máximo de 5 minutos para intentar reiniciar el sensor primario y restablecer la precisión del seguimiento.

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