## Cada módulo está diseñado como un microservicio basado en su criticidad e independencia funcional:

* **Servicio de Gestión de Clientes (Customer Service)**: Gestiona datos sensibles de los clientes (como información personal y de pago) y requiere controles
de acceso estrictos, lo que lo convierte en un componente crítico e independiente.

* **Servicio de Pedidos (Order Service)**: Maneja un alto volumen de tráfico con una cadena de procesamiento de pedidos en múltiples pasos. Aislarlo permite
escalarlo de manera independiente y gestionar de forma fluida los flujos de trabajo relacionados con los pedidos.

* **Servicio de Entregas (Delivery Service)**: Incluye la gestión de flotas de transporte y enrutamiento, y tiene requisitos críticos de rendimiento debido a
la optimización de rutas en tiempo real y las actualizaciones de entrega

* **Servicio de Estadísticas (Statistics Service)**: Proporciona información analítica que puede operar de manera independiente sin afectar las funcionalidades
centrales

* **Servicio de Gestión de Incidentes (Incident Management Service)**: Separado para garantizar la gestión en tiempo real de incidentes sin interrumpir otras
funcionalidades del sistema

* **Servicio de Pagos (Payment Service)**: Aislado para una interacción segura con la pasarela de pagos externa de MercadoLibre, manteniendo el cumplimiento y
la seguridad estrictos.

* **Servicio de Gestión de Órdenes (Order Management Service)**: Coordina los pedidos y los incidentes, facilitando la gestión central del ciclo de vida de las
órdenes y vinculando múltiples servicios para proporcionar una visión integral del estado de los pedidos.
