# Iteración 5: Seguridad del Sistema de Clientes

En esta iteración, abordamos el escenario de seguridad implementando un sistema externo para la autenticación de usuarios, separado del sistema de pagos. Una técnica ampliamente adoptada en la industria es el uso de servicios de autenticación basados en OpenID Connect, OAuth2 y JWT.

Además, considerando la base de datos dedicada a los datos de clientes (DB per service), evaluamos la posibilidad de implementar una base específica para almacenar logs de auditoría. Este enfoque es comúnmente soportado por bases de datos documentales, y seleccionamos ElasticSearch como motor de búsqueda.

También exploramos el principio de “Limit exposure”, y determinamos que el API Gateway ya unifica y expone los endpoints externos para los clientes, lo que reduce la necesidad de agregar una solución adicional. Para cubrir la necesidad, se puede configurar el Gateway con módulos que gestionen validaciones de tokens de acceso, limitación de requests por ventana temporal y otras medidas específicas. De forma similar, el patrón Gatekeeper no se consideró necesario, ya que sus responsabilidades pueden integrarse eficientemente en los componentes actuales, evitando redundancia y sobrecarga operativa.

Para la comunicación entre microservicios, consideramos necesario el uso de redes internas siempre que sea posible. En plataformas como Kubernetes, OpenShift o entornos en la nube (AWS, por ejemplo), estas redes internas se configuran fácilmente para limitar la exposición de los servicios a actores externos.

## OAuth2 y JWT

OAuth2 es un protocolo de autorización que otorga acceso controlado a servicios y recursos. Aunque define el uso de Access Tokens, no especifica su formato, más allá de requerir un tiempo de vida limitado. Un formato común es JWT, ya que permite incluir una carga útil dentro del propio token, firmada con claves RSA o ECDSA, lo que permite a los servicios validar su autenticidad sin consultar directamente al emisor. Sin embargo, también existen otros formatos como SAML, SWT y Opaque Tokens. Sabemos que en el mercado existen servicios empresariales que implementan estos mecanismos como Auth0, y también soluciones on-premise como Keycloak, que es de código abierto.

### Enlaces de referencia
- [OAuth2](https://auth0.com/intro-to-iam/what-is-oauth-2)
- [JWT](https://jwt.io/introduction)

## ElasticSearch

ElasticSearch es un motor distribuido para búsqueda, vectorización y analíticas, optimizado para entornos de alta carga. Su integración con Kibana lo convierte en una herramienta poderosa para monitoreo, búsqueda y visualización de datos. Optamos por ElasticSearch debido a su extensa documentación, amplia comunidad y flexibilidad para implementaciones on-premise y en la nube.

Consideramos que ElasticSearch es ideal para gestionar auditorías de acceso a datos de clientes, gracias a su capacidad para detectar patrones y realizar búsquedas rápidas en grandes volúmenes de datos. Sin embargo, debe emplearse con precaución al manejar datos sensibles o confidenciales, asegurando que los registros cumplen con regulaciones vigentes y políticas de privacidad.

## Resultados de la Iteración 5
- [ADR 005: Sistema de Clientes con IDP externo y Arquitectura de Tres Capas Internas.](/Architectural-Decision-Records/ADR-005.md)
- [Diagrama del Microservicio de Clientes](/Architectural-Decision-Records/imagenes/ADR-005-microservicio-clientes.md)
