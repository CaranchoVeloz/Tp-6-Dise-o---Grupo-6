# Registro de Decisión Arquitectónica 1 (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios


  ### El microservicio para operaciones CRUD de clientes se encargará de gestionar el acceso y manipulación de los datos personales y de pago de los clientes.
  Este servicio permitirá crear, leer, actualizar y eliminar registros de clientes de manera eficiente, asegurando la seguridad de la información sensible. Además,
  se diseñará para ser escalable y modular, facilitando su mantenimiento y adaptación a futuros requerimientos del sistema mientras soporta un alto volumen de
  solicitudes.


### Decisión Principal

 Se ha decidido implementar una combinación de arquitectura de microservicios y el Patrón de Repositorio para manejar las operaciones CRUD de clientes y gestionar
 la lógica de negocio. Aunque es un buen enfoque inicial, puede que no cubra todas las necesidades del sistema, requiriendo tecnologías adicionales para gestionar
 correctamente la complejidad y las restricciones del negocio

### Decisiones Alternativas

  • Implementar CQRS (Command Query Responsibility Segregation)
  • Utilizar una arquitectura de eventos con Event-Driven Microservices
  • Implementar Patrón Facade

### Pros

  • Mejora la mantenibilidad y escalabilidad del sistema
  • Proporciona una clara separación de responsabilidades entre la lógica de negocio y el almacenamiento de datos
  • Permite una arquitectura más escalable y flexible
  • Puede manejar la lógica de negocio compleja y las restricciones del sistema


### Contras

  • Puede aumentar la complejidad del sistema, incrementando el riesgo de errores y los costos de mantenimiento
  • Puede no ser adecuado para el módulo de incidencias de entrega, que requiere una arquitectura más compleja y desacoplada
  • Requiere decisiones de seguimiento adicionales, como la definición de interfaces y contratos para el Patrón de Repositorio y la elección de una tecnología de
  almacenamiento de datos adecuada
