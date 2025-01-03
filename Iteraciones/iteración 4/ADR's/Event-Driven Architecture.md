# Registro de Decisión Arquitectónica 7 (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios

### El servicio de entrega incluye componentes críticos para gestionar la entrega de flotas de transporte a los clientes y determinar las rutas de los camiones
Este servicio requiere optimización de rutas en tiempo real y actualizaciones de entrega para mantener el rendimiento y la escalabilidad, especialmente durante 
horas picos de entrega. Para asegurar una gestión de flotas eficiente, el sistema debe procesar eventos, como actualizaciones de rutas y cambios en el estado 
de los camiones, en tiempo real. Necesitamos un patrón de arquitectura que permita esta alta capacidad de respuesta y que permita que los componentes se comuniquen 
de forma asincrónica sin introducir retrasos significativos.

### Decision principal
Decidimos aplicar la Arquitectura Basada en Eventos, porque es la que mejor soporta la capacidad de respuesta en tiempo real y la comunicación desacoplada para
requisitos críticos de rendimiento en el Servicio de Entrega. Un enfoque basado en eventos permite que el sistema reaccione a las actualizaciones conforme ocurren, 
manejando eventos de transportes y rutas de forma asincrónica y reduciendo los tiempos de espera para ajustes de rutas y actualizaciones de entrega. Este enfoque 
asegura que cada servicio pueda responder a los eventos relevantes de manera independiente, mejorando la escalabilidad y minimizando las dependencias directas.

### Decisiones alternativas
•	REST-based Polling
•	Message Queue with Direct Request/Response Pattern

### Pros
•  Capacidad de respuesta en tiempo real
•  Escalabilidad
•  Modularidad y bajo acoplamiento
•  Mayor tolerancia a fallos

Contras
•  Mayor complejidad
•  Aumento de lantecia
