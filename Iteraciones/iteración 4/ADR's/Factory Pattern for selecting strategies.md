# Registro de Decisión Arquitectónica 8 (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios

Utilizando el patrón strategy previamente, nuestro servicio de Entrega ahora puede manejar múltiples algoritmos de optimización de rutas de manera independiente, 
lo que nos permite cambiar dinámicamente entre ellos. Sin embargo, aún necesitamos un método para seleccionar la estrategia apropiada según los retrasos actuales
de los camiones y otros datos en tiempo de ejecución. Esto requiere un patrón que pueda instanciar y configurar dinámicamente la estrategia correcta según condiciones
específicas, como umbrales de retraso u otras métricas sensibles al contexto, sin codificar rígidamente la lógica de decisiones dentro del servicio de Entrega.

### Decision Principal
Elegimos el patrón de Factory porque nos permite encapsular la lógica para seleccionar e instanciar la estrategia apropiada según los datos en tiempo de ejecución.
Este Patrón permite que un componente centralizado (la "Fábrica de Estrategias") tome la decisión deselección, haciendo que el sistema sea más modular y más fácil
de mantener. De esta manera, el servicio de Entrega no necesita conocer las condiciones específicas de cada algoritmo y simplemente puede solicitar la estrategia 
apropiada a la fábrica.

### Decisiones alternativas
•	Service Locator Pattern
•	Sentencias condicionales en la lógica principal

### Pros:
o	Encapsulación de la lógica de selección
o	Flexibilidad y escalabilidad
o	Facilidad de mantenimiento

### Contras:
o	Aumento de complejidad
o	Posible aunmento de Overhead si se realizan muchos cambios en las estrategias en tiempo de ejecución
