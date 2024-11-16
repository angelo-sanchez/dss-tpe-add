# Desplegabilidad - Escenario 01 - Migración de un componente a microservicio

El equipo de DevOps debe desplegar un nuevo microservicio, anteriormente parte del monolito, en los entornos de pruebas y producción y sin afectar al sistema en funcionamiento. En caso de fallo, el despliegue debe permitir un rollback inmediato, sin interrupción de los servicios. Al menos el 90% de los despliegues deben ser exitosos en el primer intento, sin impacto en la disponibilidad del sistema. En caso de rollback, el estado anterior debe restaurarse en un máximo de 10 minutos.

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
