# Registro de Decisión Arquitectónica 6 (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios

**Payment Service** puede experimentar picos en las solicitudes de pago durante períodos de mucho tráfico (por ejemplo, Black Friday). Manejar estas solicitudes de manera sincrónica podría sobrecargar la pasarela externa o causar retrasos.

## Decisión principal

Integrar una cola de mensajes (por ejemplo, RabbitMQ, Kafka) para el procesamiento asincrónico de las solicitudes de pago. El Servicio de Pagos pondrá las solicitudes de pago en una cola, permitiendo que se procesen en grupos y a una tasa que la pasarela externa pueda manejar.

## Alternativas Consideradas

- Procesar todas las solicitudes de manera sincrónica en tiempo real
- Request pooling mechanism

## Pros

- Mejora la escalabilidad y resiliencia del sistema

## Contras

- Añade complejidad al flujo de trabajo del pago
- Añade latencia al procesamiento de pagos
- Riesgo de pérdida o duplicación de mensajes si no se maneja adecuadamente
