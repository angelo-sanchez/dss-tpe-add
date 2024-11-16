# Seguridad - Escenario 01 - Componente de Clientes (Proteccion de datos personales)

El sistema debe garantizar la seguridad de los datos personales de los clientes, que incluyen información sensible como nombres, direcciones y detalles de pago.

**Estimulo**: Un atacante intenta acceder a los datos personales de los clientes mediante un ataque.

**Fuente**: Actor malintencionado externo (atacante).

**Ambiente**: Tiempo de ejecución, en el entorno de producción.

**Respuesta esperada**: El sistema debe detectar y bloquear el intento de ataque, registrando el incidente en el sistema de monitoreo de seguridad, sin comprometer los datos de clientes ni afectar el funcionamiento del microservicio de Clientes.

**Medidas de respuesta**:

- El ataque debe ser detectado en menos de 1 segundo.
- El sistema debe registrar el evento y alertar al equipo de seguridad automáticamente.
- El servicio debe mantenerse estable y no permitir acceso no autorizado a los datos.
