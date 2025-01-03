# Registro de Decisión Arquitectónica 2 (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios

### El microservicio Management of personal and payment data for clients se encarga de gestionar de forma segura y eficiente los datos sensibles de los clientes
Este servicio asegura el acceso controlado y la manipulación adecuada de estos datos críticos, garantizando la protección y privacidad de la información. Además, 
debe cumplir con altos estándares de seguridad y rendimiento debido a la naturaleza confidencial de los datos que maneja, y ser capaz de integrarse con otros servicios, 
como el gateway de pagos externo y las operaciones CRUD de clientes.

### Decisión Principal
El patrón DAO permitirá una separación clara entre la lógica de negocio y el acceso a datos, mejorando la modularidad y escalabilidad del sistema. Sin embargo, 
no cubre de manera explícita los aspectos críticos de seguridad y rendimiento, que requieren atención adicional.

### Decisiones Alternativas
  • Event Sourcing: Un enfoque alternativo al patrón DAO podría ser el uso de event sourcing, lo que permitiría una capa de acceso a datos más flexible y escalable.
  • Patrón de Repositorio: Otra alternativa podría ser usar el patrón de repositorio, que proporcionaría una capa de acceso a datos más robusta y mantenible.


### Pros
  • El patrón DAO proporciona una clara separación de responsabilidades entre la lógica de negocio y la capa de acceso a datos.
  • El patrón DAO puede usarse para desacoplar la capa de acceso a datos de la lógica de negocio, lo que permite una arquitectura más modular y escalable.


### Contras
  • El patrón DAO puede no ser capaz de proporcionar suficiente seguridad para los datos personales y de pago.
  • El patrón DAO puede no ser capaz de manejar los requisitos de rendimiento y escalabilidad del sistema.
  • Se podrían necesitar medidas adicionales de seguridad, optimización y desacoplamiento para implementar el patrón DAO de manera efectiva.
