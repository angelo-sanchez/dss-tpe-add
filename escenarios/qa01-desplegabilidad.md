# QA-1 - Desplegabilidad

**Fuente:** El equipo de DevOps.

**Estimulo:** Se requiere desplegar un nuevo microservicio.

**Artefacto:** Microservicio a desplegar, Resto del sistema.

**Ambiente:** Entorno de Pruebas, Producción.

**Respuesta:**
- El microservicio se despliega sin afectar a los demás microservicios y/o el resto del sistema que ya esté funcionando.
- Si el despliegue falla, se debe ejecutar un rollback sin interrupción de los servicios a los clientes.

**Medidas de Respuesta:**
- La tasa de despliegues correctos a la primera, es mayor al 90%.
- El despliegue del nuevo microservicio no produce downtime en el resto del sistema.
- En caso de rollback, el estado anterior del sistema se restaura en menos de 10 minutos.
