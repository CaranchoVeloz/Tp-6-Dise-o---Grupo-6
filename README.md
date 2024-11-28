# Trabajo Práctico Especial: Proceso ADD (Grupo 6)
* Dadin Santiago
* Pardo Lautaro
* Perrone Bruno

[Contexto y Restricciones](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Contexto%20y%20Restricciones)

## [Iteración 1](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/tree/main/Iteraciones/Iteraci%C3%B3n%201)

Análisis de la Arquitectura, Descomposición y Drivers del Sistema

* [Diagrama Arquitectura Monolítica](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteración%201/Arquitectura%20Monolítica.png)
* [Diagrama microservicios](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteración%201/Diagrama%20microservicios.png)

## [Iteración 2](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/tree/main/Iteraciones/Iteraci%C3%B3n%202)

En la presente iteración se busca implementar el micro-servicio Customer Service ya que se considera la interacción con el
cliente y su información de nivel crítico para lograr una migración satisfactoria del sistema desde una arquitectura monolítica
a una arquitectura de micro-servicios.

* [ADR 1](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteraci%C3%B3n%202/ADR's/CRUD%20operations%20for%20clients.md)
* [ADR 2](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteraci%C3%B3n%202/ADR's/Management%20of%20personal%20ad%20payment%20dnata%20for%20clients.md)
* [ADR 3](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteraci%C3%B3n%202/ADR's/Security%20Pattern%20for%20Customer%20Service.md)

* [Diagrama Customer Service](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteración%202/Diagrama%20Customer%20Service.png)

## [Iteración 3](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/tree/main/Iteraciones/Iteraci%C3%B3n%203)

En la actual interación se plantea el diseño de la implementación del micro servicio Payment Service debido a su orden en relación
prioridad en el sistema/esfuerzo de desarrollo

* [ADR 4](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteraci%C3%B3n%203/ADR's/Integration%20with%20an%20external%20payment%20gateway.md)
* [ADR 5](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteración%203/ADR's/Circuit%20Breaker%20pattern.md)
* [ADR 6](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteración%203/ADR's/Scalability%20through%20Message%20Queues.md)

* [Diagrama componentes](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/Iteración%203/Diagrama.png)

## [Iteración 4](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/tree/main/Iteraciones/iteraci%C3%B3n%204)

En esta iteración se refinará el microservicio Delivery Service, siendo uno de los componentes de necesidad crítica del sistema original.
Este servicio es clave para garantizar la eficiencia logística y la satisfacción del cliente al gestionar entregas y optimizar rutas.

* [ADR 7](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/iteraci%C3%B3n%204/ADR's/Event-Driven%20Architecture.md)
* [ADR 8](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/iteraci%C3%B3n%204/ADR's/Factory%20Pattern%20for%20selecting%20strategies.md)
* [ADR 9](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/iteraci%C3%B3n%204/ADR's/Strategy%20Pattern%20for%20Dynamic%20Route%20Optimization.md)

* [Diagrama de clase](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/iteración%204/Diagrama%20de%20clase.png)
* [Diagrama event-driven](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/iteración%204/Diagrama%20event-driven.png)
* [Diagrama secuencia eventos](https://github.com/CaranchoVeloz/Tp-6-Dise-o---Grupo-6/blob/main/Iteraciones/iteración%204/Diagrama%20secuencia%20eventos.png)

## Futuras Iteraciones
Para las proximas iteraciones del diseño de la migración deberán tratarse los servicios:
* Servicio de Pedidos (Order Service): Semi Critico
* Servicio de Gestión de Incidentes (Incident Management Service): Semi Critico
* Servicio de Estadísticas (Statistics Service): No Critico
