# Sistema de productos alimenticios

### Requerimentos

Los requerimientos del sistema fueron recopilados a partir del enunciado provisto, complementados con algunas suposiciones realizadas para completar información faltante. Estos se encuentran en: 
  
  - [Atributos de Calidad](./Architectural-Drivers/Atributos%20de%20Calidad.md)
  - [Requisitos Funcionales](./Architectural-Drivers/Requisitos%20Funcionales.md)
  - [Restricciones](./Architectural-Drivers/Restricciones.md)
  - [Escenarios de Calidad](./Architectural-Drivers/escenarios)

### Proceso ADD

Para el diseño del sistema, implementamos el método Attribute-Driven Design (ADD), llevando a cabo varias iteraciones en las que seguimos rigurosamente los pasos definidos por el método.

Una explicación detallada de cada iteración, incluyendo los pasos realizados y los resultados obtenidos, está documentada en la sección [Iteraciones del Proceso](./Iteraciones)

Cabe recalcar, que fueron realizadas en el tiempo, siendo cada iteracion, el resultado de una Reunion de equipo. 
Esto ultimo no se ve reflejado en el historial de commits del GIT, ya que los archivos de las iteraciones fueron subidos todos juntos, pero si se ve reflejado en el historial de los [ADRs](./Architectural-Decision-Records) 

### Resultado Final

El proceso de diseño mediante el método ADD produjo los siguientes resultados:

- Conjunto de Architecture Decision Records (ADRs): Documentos que explican las decisiones arquitectónicas clave tomadas durante el diseño. [ADRs](./Architectural-Decision-Records)
- Diagramas asociados a cada ADR: Estos diagramas detallan aspectos específicos de las decisiones tomadas. [diagramas](./Architectural-Decision-Records/imagenes)
- Diagrama Final: Una vista integrada basada en una arquitectura de microservicios que unifica las decisiones tomadas. Este diagrama describe los distintos elementos del sistema y proporciona enlaces a los ADRs para obtener información detallada de cada componente. [diagrama final](./Arquitectura/arquitectura.md)

La aplicación del método ADD permitió estructurar el diseño del sistema de manera sistemática y basada en los atributos de calidad clave. A través de iteraciones, logramos tomar decisiones arquitectónicas fundamentadas,
reflejadas en los ADRs y respaldadas por diagramas detallados. 
