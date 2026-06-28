# Metodología Ágil - Scrumban

Para proyectos de desarrollo de software unipersonales, la aplicación estricta de metodologías ágiles puras como *Scrum* genera una sobrecarga y ceremonias artificiales (por ejemplo, *Daily Standups* o *Retrospectives grupales*).

Por otro lado, un enfoque puramente continuo como *Kanban* puede carecer de hitos temporales que fuercen la entrega periódica de incrementos y el control del avance de cara a los plazos académicos.

Considerando que el proyecto **AguaraVet** es llevado a cabo por un único desarrollador y en un marco académico, se ha adoptado un modelo de trabajo híbrido denominado *Scrumban* que combina lo mejor de ambos mundos:

- Mantiene la disciplina de trabajar en iteraciones de tiempo fijo (*sprints*), lo que provee estructura, fechas límite claras y metas a corto plazo para evitar la procrastinación.
- Adopta la visualización del flujo de trabajo mediante un tablero (implementado en *Jira*)
- Contempla la limitación del *Trabajo en Progreso*, evitando la dispersión de esfuerzos provocado por el desarrollo simultáneo de múltiples tareas.

Para visualizar el estado del proyecto en *Jira*, se utiliza un tablero con las siguientes columnas:

- **Backlog:** Lista priorizada de todas las historias de usuario de las épicas pendientes de desarrollo.
- **To Do:** Historias seleccionadas para el sprint activo.
- **In Progress:** Tareas técnicas en ejecución activa.
- **Testing:** Historias que están siendo validadas mediante la suite de pruebas (Pest) y pruebas de interfaz.
- **Done:** Tareas completamente terminadas y probadas.

Considerando que el proyecto es unipersonal, se eliminan las reuniones grupales pero se mantiene la disciplina/ceremonias de manera personal:

- Planificación del *Sprint* (2 semanas):
    - Al inicio de cada iteración.
    - Seleccionar un conjunto de historias de usuario del backlog para desarrollar.
    - Definir la meta del *Sprint*.
- Monitoreo diario, se debe hacer un auto-chequeo rápido frente al tablero:
    - ¿Qué hice ayer?
    - ¿En qué voy a trabajar hoy?
    - ¿Tengo algún bloqueo técnico?
- Autorevisión y Retrospectiva:
    - Al finalizar cada sprint.
    - Ejecutar y verificar que el software realmente cumpla con los criterios de aceptación de las historias de usuario del sprint.
    - Evaluar qué herramientas o flujos técnicos funcionaron bien y cuáles causaron retrasos.
    - Ajustar estimaciones de esfuerzo para el siguiente sprint.

El análisis y monitoreo del flujo de trabajo se plantea utilizando dos métricas clave de Kanban:

- **Cycle Time:** Mide cuánto tiempo pasa una historia desde que entra a *In Progress* hasta que llega a *Done*. El objetivo es mantener este tiempo bajo dividiendo tareas complejas en subtareas pequeñas.
- **Sprint Velocity:** Cantidad de puntos de historia completados en cada sprint de 2 semanas. Ayuda a planificar con precisión realista las capacidades de los futuros sprints y asegurar que se cumpla con el plan de entrega de la tesis.
