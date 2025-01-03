# DRIVERS
## Requerimientos funcionales

### Gestión de Clientes (Crítico):
  • Operaciones CRUD para clientes (crear, actualizar, eliminar, ver).
  • Gestión de datos personales y de pagos de los clientes.

### Gestión de Pedidos (Semi-crítico):
  • Permitir a los clientes realizar pedidos, limitados a 3 intentos por cliente.
  • Procesamiento de pedidos en tres fases secuenciales: preprocesamiento, autorización y aceptación.

### Gestión de Entregas y Rutas (Crítico):
  • Gestionar la entrega de flotas de transporte a los clientes.
  • Implementar enrutamiento de camiones con selección automática de algoritmos de optimización basados en retrasos.

### Estadísticas (No crítico):
  • Proporcionar estadísticas sobre el estado de los pedidos, ubicaciones en tiempo real de los camiones y datos relevantes de los clientes.

### Informes de Incidentes (Semi-crítico):
  • Reporte en tiempo real de incidentes de entrega (por ejemplo, fallos de camiones, envíos no entregados).

### Procesamiento de Pagos (Crítico):
  • Integración con la pasarela de pagos externa de MercadoLibre para garantizar pagos seguros y compatibles.

### Coordinación de Pedidos e Incidentes (Semi-crítico):
  • Gestión centralizada de todas las solicitudes de pedidos e incidentes relacionados con las entregas.


## ATRIBUTOS DE CALIDAD

### Escalabilidad: 
  • El sistema debe soportar la escalabilidad en función del volumen de pedidos y expansión de transporte, manejando cargas aumentadas sin degradar el rendimiento.

### Modificabilidad: 
  • Los componentes del sistema deben ser modulares para permitir actualizaciones fáciles de funcionalidades individuales sin afectar el sistema completo.

### Interoperabilidad: 
  • La nueva arquitectura debe soportar diferentes clientes, como PC y dispositivos móviles, mediante protocolos HTTP/REST estandarizados.

### Seguridad: 
  • Especialmente para los datos de clientes y procesos de pago, es esencial un manejo y comunicación segura de los datos para proteger la información sensible.

### Rendimiento: 
  • Se requiere procesamiento de alto rendimiento para componentes críticos, particularmente para los servicios de Pedidos y Entregas, para garantizar un manejo y entrega de pedidos oportunos.
