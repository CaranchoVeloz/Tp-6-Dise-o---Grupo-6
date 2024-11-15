# Registro de Decisión Arquitectónica (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios

### El micro servicio Payment Service tiene la responsabilidad de interactuar de forma segura con un metedo de pago externo a la hora de realizar un pago

### Decisión Principal

Se elige el Patrón de Integración de Pasarelas de Pago (PGIP) como la decisión principal para abordar los requisitos de procesamiento de pagos.
La implementación del PGIP separará la lógica de procesamiento de pagos del resto de la aplicación, garantizando seguridad, escalabilidad y mantenibilidad.

### Decisiones Alternativas 

* API Gateway: Se puede usar un API Gateway para gestionar las solicitudes y respuestas de la API, pero esto podría añadir complejidad adicional a la implementación.

### Pros

* Seguridad: La implementación del PGIP asegura la seguridad en el procesamiento de pagos.

* Escalabilidad: La implementación del PGIP garantiza la escalabilidad de la funcionalidad de procesamiento de pagos.

* Mantenibilidad: La implementación del PGIP facilita el mantenimiento de la funcionalidad de procesamiento de pagos.

* Compatibilidad: La implementación del PGIP asegura la compatibilidad de los pagos con la pasarela de pago externa (MercadoLibre).

### Contras

* Complejidad Adicional: La implementación del PGIP puede introducir una complejidad adicional en la arquitectura de microservicios existente.

* Costos Adicionales: La implementación del PGIP podría requerir recursos y costos adicionales para el desarrollo y mantenimiento.

* Flexibilidad Limitada: La implementación del PGIP podría limitar la flexibilidad de la funcionalidad de procesamiento de pagos.
