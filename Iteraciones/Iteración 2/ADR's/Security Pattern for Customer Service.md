# Registro de Decisión Arquitectónica (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios

### El microservicio de Customer Service gestiona datos sensibles de los clientes, incluyendo información personal y de pago 
Debido a la naturaleza crítica de estos datos, requiere mecanismos de seguridad robustos para garantizar la confidencialidad, integridad y control de acceso.
Como parte de una arquitectura de microservicios, el servicio se accede a través de un API Gateway, que sirve como punto de entrada para los usuarios externos.
Necesitamos asegurarnos de que solo los usuarios autorizados puedan acceder a los datos de los clientes, manteniendo la escalabilidad y el rendimiento.

### Decision principal

Decidimos implementar Autenticación basada en JWT y Control de Acceso Basado en Roles (RBAC), utilizando el API Gateway para cumplir con 
la seguridad de manera centralizada.
•	Autenticación JWT: Cada solicitud será autenticada mediante un token JWT que será validado en el API Gateway antes de ser enviado al microservicio Customer
Service. Este enfoque asegura una autenticación sin estado y elimina la necesidad de gestionar sesiones en el lado del servidor.
•	RBAC: En un principio se tendrán dos roles, usuario y administrador para gestionar tareas administrativas), y a futuro se podrías añadir nuevos. Esto permite
diferentes niveles de acceso a los datos de los clientes.

### Alternativas consideradas
•	API Key Authentication
•	Session-Based Authentication

### Pros:
•	Stateless Authentication
•	Seguridad centralizada 
•	Escalabilidad
### Cons:
•	Mayor complejidad en el acceso a datos
•	Overhead en el API Gateway
