# Registro de Decisión Arquitectónica (ADR)
## Arquitectura basada en Microservicios para la Empresa de Productos Alimenticios

### El Servicio de Entrega debe seleccionar dinámicamente los algoritmos de optimización de rutas según las condiciones de retraso de los camiones.
Actualmente, se requieren dos algoritmos principales, pero en el futuro se podrían agregar nuevos tipos de algoritmo de optimización. Esta selección debe gestionarse
en tiempo real para asegurar una gestión eficiente y adaptable de las entregas.El desafío es implementar un patrón que permita un cambio sin problemas entre algoritmos
según las condiciones en tiempo de ejecución, garantizando que el sistema cumpla con los requisitos de rendimiento y flexibilidad.

### Decisión principal
Elegimos el Patrón Strategy porque proporciona una solución clara y escalable para gestionar múltiples algoritmos de optimización de 
rutas. Este patrón permite que cada algoritmo se encapsule en una clase separada, haciendo que el código sea más modular y mantenible.
También facilita la extensión si en el futuro se requieren nuevos algoritmos, satisfaciendo nuestras necesidades de flexibilidad y 
rendimiento. 

### Decisiones alternativas
•	Sentencias condicionales simples
•	Factory Pattern con lógica condicional

### Ventajas
o Mejora la mantenibilidad 
o Escalabilidad 

### Desventajas
o Aumenta ligeramente la complejidad inicial debido a la necesidad de crear múltiples clases para cada algoritmo.
