El microservicio ‘Payment Service’ interactúa con una pasarela de pagos externa, como MercadoLibre, para procesar transacciones. Sin embargo, este servicio externo puede experimentar períodos de inactividad, alta latencia u otros problemas que podrían causar fallos o demoras en el procesamiento de pagos. Si estos problemas no se abordan correctamente, pueden afectar la experiencia del usuario y provocar interrupciones en todo el sistema.

## Decisión Principal

Implementar el **Patrón Circuit Breaker** para mejorar la resiliencia del Servicio de Pagos al interactuar con la pasarela de pagos externa. El Circuit Breaker monitorizará el estado de salud de la pasarela de pagos, y si detecta un fallo (como múltiples solicitudes fallidas consecutivas dentro de un período de tiempo predefinido), detendrá temporalmente las nuevas solicitudes. Esto previene fallos en cascada y asegura que el sistema permanezca estable. El Circuit Breaker proporcionará respuestas alternativas o mecanismos de reintento para manejar problemas de inactividad o latencia de manera controlada.

## Decisiones Alternativas

- Lógica de Reintentos con Timeout
- Rate Limiting

## Pros

- Mayor tolerancia a fallos.
- El sistema puede ofrecer mecanismos de respaldo, como mensajes de error amigables para el usuario o métodos de pago alternativos.
- Prevención de fallos en cascada a otros componentes del sistema.

## Contras

- Complejidad adicional
- Overhead de monitoreo: Requiere una configuración adecuada, monitoreo y ajustes para garantizar que el sistema funcione de manera óptima.
