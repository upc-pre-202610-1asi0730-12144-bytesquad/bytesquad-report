# Conclusiones y Recomendaciones

## Conclusiones

### Sprint 1

* **Propuesta de Valor Basada en IoT:** La propuesta central de SpotTrack no es un sistema de reportes, sino la visibilidad en tiempo real del estado de cada máquina a través de sensores Edge. Esta telemetría pasiva —que no requiere ninguna acción del usuario— transforma directamente la experiencia del cliente en el gimnasio: este puede consultar qué máquinas están libres antes de desplazarse al local, organizar su rutina evitando tiempos de espera y obtener sugerencias de ejercicios alternativos cuando una máquina está ocupada. El mapa de calor interactivo (con indicadores verde/rojo por máquina) es la interfaz que convierte los datos del sensor en valor tangible para el usuario final, y es la razón por la que SpotTrack resuelve un problema que ningún competidor como Fitco, GYMMaster o Virtuagym puede atender sin IoT.
* **La Telemetría como Fundamento:** La telemetría acumulada por los dispositivos Edge es la materia prima de todas las capas superiores del sistema: los patrones de uso histórico alimentan las alertas de mantenimiento predictivo, las estadísticas de ocupación por hora informan las recomendaciones de horario, y los datos de desgaste acumulado sustentan las decisiones de reubicación o reemplazo de activos. Las funcionalidades analíticas y de gestión son extensiones que amplifican el valor del sensor, pero no pueden existir sin él. Esta dependencia refuerza la importancia de priorizar la estabilidad y cobertura del flujo de telemetría como fundamento de todo el sistema.
* **Diseño de Arquitectura (DDD):** La definición de **Bounded Contexts** (Telemetría, Mantenimiento, Activos, Reservas, Rutinas y Analíticas) permitió que los cinco integrantes del equipo trabajaran en áreas delimitadas sin interferencias. El modelado previo mediante **EventStorming** fue determinante para identificar flujos críticos —como la sincronización del estado de una máquina entre el sensor, el mapa de calor y el módulo de reservas— antes de iniciar el desarrollo, lo que redujo la necesidad de refactorizaciones costosas.
* **DevOps y Despliegue Continuo:** La automatización del despliegue de la Landing Page en GitHub Pages garantizó que cada integración a `main` quedara reflejada en producción de forma inmediata y sin intervención manual. Esta práctica, implementada desde el Sprint 1, demostró que configurar el pipeline de despliegue en las etapas tempranas del proyecto elimina la fricción acumulada de los despliegues manuales y sienta las bases para extender esta automatización al backend en sprints posteriores.

### Sprint 2

* **Dualidad de Desarrollo:** El Sprint 2 operó en dos frentes simultáneos: sanear los artefactos pendientes del Sprint 1 (15 tareas CORR + 4 tareas SETUP) e iniciar el desarrollo del frontend **Vue.js con JavaScript** y una Fake API. Esta dualidad permitió avanzar en ambas dimensiones sin bloquear ninguna, pero evidenció que la carga de coordinación entre subequipos es significativamente mayor que en un sprint de un solo frente. La asignación de responsables claros por área fue determinante para mantener el flujo.
* **Validación de Integración con Fake API:** El hecho de contar con la Fake API accesible en una URL pública permitió que todos los integrantes del equipo consumieran el mismo backend simulado independientemente de su entorno local. Esto eliminó la clase de errores de integración más frecuente en proyectos de equipo ("funciona en mi máquina") y validó el flujo de despliegue que se reutilizará para el backend real en el Sprint 3.
* **Estructura de Proyecto Escalable:** Inicializar el proyecto **Vue** con carpetas separadas por contexto (`auth/`, `heatmap/`, `admin/`, `maintenance/`, `equipment/`, `routines/`) demostró que los límites de dominio definidos en el DDD son aplicables también en la capa de presentación. Esta organización facilitó que cada integrante trabajara en su módulo asignado con mínima interferencia sobre el código de los demás.

### Sprint 3

* **Transición Validada de Fake API a Backend Real:** El equipo concretó el paso de JSON Server a un backend real, organizado en Bounded Contexts claramente delimitados (Gym, Equipment, Maintenance, Reservation, Profiles, IAM y Routines) que se comunican entre sí mediante eventos de integración bajo el patrón Anti-Corruption Layer (`TicketCreatedEvent` / `TicketResolvedEvent`). Esto confirmó que el modelado DDD realizado desde el Sprint 1 escala correctamente a un backend real y no solo a una capa de datos simulada.
* **El Contrato de Interfaz Cumplió su Propósito:** Al respetar los mismos paths y estructuras de respuesta documentados desde la Fake API, la integración frontend-backend no requirió modificar ningún componente Vue del Sprint 2; solo fue necesario actualizar la URL base en `environment.ts`. Esto valida directamente la recomendación de Sprint 2 sobre preservar el contrato de interfaz para facilitar la migración.
* **Subestimación de la Amplitud del Dominio:** El equipo reconoció en la retrospectiva que la amplitud del backend fue subestimada en la planificación del Sprint 3, lo que impidió completar a tiempo los Bounded Contexts de Analytics y de IoT/Telemetría. Esto evidenció que dividir el trabajo por Bounded Context no elimina el riesgo de subestimar la complejidad de contextos individuales dentro de un dominio amplio.
* **Arrastre de Correcciones Pendientes:** Solo el 60% de las correcciones indicadas en el Sprint 1 se completó durante el Sprint 2, y la retrospectiva de ese sprint identificó la ausencia de un proceso de QA formal como causa raíz. Esta deuda técnica y de documentación se mantuvo como un riesgo latente que el equipo debió gestionar activamente al planificar el Sprint 3.

### Sprint 4

* **Efecto Cascada de Requisitos No Anticipados:** El alcance real del Sprint 4 superó ampliamente la estimación inicial de 40 Story Points (cerrando en 117). La incorporación de Membership & Billing con Stripe resultó ser una precondición no anticipada para que un administrador pudiera operar la plataforma, arrastrando consigo el onboarding de gimnasios, la gestión de sedes y la lista blanca de clientes. De forma similar, la ampliación de la red de sensores IoT generó la necesidad de un Centro de Alertas unificado no contemplado en el Sprint 3. Esto demuestra que una funcionalidad aparentemente aislada (el cobro de membresías) puede convertirse en un prerrequisito estructural que redefine el alcance completo de un sprint.
* **Resiliencia del Equipo Mediante Bounded Contexts:** La salida de dos integrantes durante el sprint no detuvo el ritmo de entrega gracias a la incorporación oportuna de nuevos miembros y a la arquitectura por Bounded Contexts, que permitió que estos tomaran ownership de módulos delimitados (Monitoring, Alerts, parte de Maintenance y Routines) sin fricción con el código existente. Esto confirma que el diseño DDD adoptado desde el Sprint 1 no solo distribuye el trabajo, sino que también absorbe cambios en la composición del equipo.
* **Mayor Volumen de Entrega del Proyecto:** El Sprint 4 concentró el mayor volumen de trabajo de todo el proyecto (403 commits / 36 Pull Requests en `bytesquad-platform`, 154 commits / 16 Pull Requests en `bytesquad-webapp` y 4 commits / 3 Pull Requests en `bytesquad-website`), reflejando el cierre simultáneo de cuatro frentes: Membership & Billing, IoT Monitoring/Alertas, Mantenimiento/Analítica-ROI e integración final del frontend y Landing Page.
* **Deuda Técnica Reconocida al Cierre:** El equipo identificó que no se implementó cobertura de pruebas automatizadas (unitarias o de integración) para los nuevos Bounded Contexts, ni un pipeline de CI/CD para el repositorio del backend. A diferencia de otros hallazgos del proyecto, esta carencia quedó explícitamente documentada como pendiente para una eventual continuidad del producto, en lugar de resolverse dentro del sprint.

---

## Recomendaciones

### Sprint 1

* **Priorización de Correcciones:** Las 15 tareas de corrección abarcan deficiencias documentales y de despliegue identificadas en la revisión del Sprint 1. En particular, CORR-06 (Diagrama ERD y Diagrama de Clases), CORR-07 (evidencias de ejecución) y CORR-08 (Big Picture EventStorming) tienen impacto directo en la calificación. Se recomienda cerrar estas tareas antes de iniciar la documentación del Sprint Review.
* **UX Centrada en el Valor:** Al diseñar el flujo de navegación de la **SPA en Vue**, el mapa de calor debe ser la pantalla principal inmediatamente después del login. Dado que la disponibilidad de máquinas en tiempo real es el motivo principal de uso, colocarlo como punto de entrada refuerza la propuesta de valor y reduce la fricción de navegación.

### Sprint 2

* **Consistencia de Datos Semilla:** La configuración del `db.json` con datos semilla completos es un requisito técnico que desbloquea el backlog de vistas. Las vistas de autenticación, reservas y gestión de activos dependen de que esta tarea esté resuelta. Continuarla en paralelo al desarrollo de componentes genera inconsistencias y retrabajo.
* **Foco en el Core Funcional:** Las tareas **T15** (Build interactive heatmap component) y **T16** (Implement real-time status update via polling) son el núcleo funcional. El resto de funcionalidades dependen del mapa de calor como superficie de interacción base. Postergar estas tareas compromete la viabilidad de la demo del Sprint Review.
* **Contrato de Interfaz para Migración:** Para que el paso de JSON Server al backend real no implique cambios en los **componentes de Vue**, los endpoints deben respetar los mismos paths y estructuras de respuesta documentados. Con ese contrato preservado, la transición se reduce a actualizar la URL base en las variables de entorno (`.env`) sin tocar la lógica de los servicios o componentes.

### Sprint 3

* **Proceso de QA Formal:** Dado que la ausencia de un proceso de QA formal fue la causa raíz de que solo el 60% de las correcciones del Sprint 1 se completara en el Sprint 2, se recomienda establecer deadlines claros por tarea, rastrear el progreso por capítulo/Bounded Context y ejecutar releases oportunos en lugar de acumular correcciones al final del sprint.
* **Estimación por Bounded Context Individual:** Al planificar sprints de backend, se recomienda estimar la complejidad de cada Bounded Context de forma independiente en vez de asignar una velocidad global al sprint. Esto habría anticipado que Analytics e IoT/Telemetría requerían más tiempo del disponible, evitando que quedaran incompletos al cierre del Sprint 3.
* **Responsable de Integración API:** Se recomienda designar un responsable que valide el contrato de API entre frontend y backend antes de cerrar cada tarea, y definir criterios de aceptación explícitos por endpoint antes de iniciar su implementación. Esto reduce el riesgo de romper la integración lograda entre el frontend Vue del Sprint 2 y el backend real del Sprint 3.

### Sprint 4

* **Descubrimiento Temprano de Precondiciones Estructurales:** Se recomienda que, al planificar sprints de cierre, el equipo identifique explícitamente qué funcionalidades actúan como precondición estructural de otras (como ocurrió con Membership & Billing respecto al onboarding de gimnasios) antes de fijar la estimación de Story Points, ya que estas dependencias ocultas fueron la causa principal de que el alcance real triplicara la estimación inicial.
* **Cobertura de Pruebas Automatizadas:** Se recomienda priorizar la implementación de pruebas unitarias y de integración para los Bounded Contexts incorporados en el Sprint 4 (Membership, Monitoring, Alerts, Maintenance Technicians), dado que el equipo cerró el proyecto sin esta cobertura y la reconoció como un riesgo para la continuidad del producto.
* **Pipeline de CI/CD para el Backend:** Se recomienda implementar un pipeline de CI/CD para `bytesquad-platform`, replicando la automatización de despliegue continuo que ya funcionó exitosamente para la Landing Page desde el Sprint 1, de modo que los 403 commits del Sprint 4 no dependan de verificaciones y despliegues manuales.
* **Onboarding Documentado para Nuevos Integrantes:** Dado que la incorporación de nuevos miembros a mitad de proyecto no afectó el ritmo de entrega gracias a la arquitectura por Bounded Contexts, se recomienda documentar este proceso de onboarding (asignación de BC delimitado, ownership claro) como práctica reutilizable ante futuras rotaciones de equipo.


# Video About-the-Team.

[https://upcedupe-my.sharepoint.com/:v:/g/personal/u202410344_upc_edu_pe/IQBQYfOHmJ33T7P3jOmYqfebAVQqfJcPijESa7oUeaNyzvw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=FYl2st](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202410344_upc_edu_pe/IQBQYfOHmJ33T7P3jOmYqfebAVQqfJcPijESa7oUeaNyzvw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=FYl2st) 

# Bibliografía

<p style="padding-left: 30px; text-indent: -30px;">DINGG Team. (2025, 26 de noviembre). *Your 5-step operational plan to handle equipment failures*. DINGG. https://dingg.app/blogs/your-5-step-operational-plan-to-handle-equipment-failures</p>

<p style="padding-left: 30px; text-indent: -30px;">Maintainnow. (2025, 19 de octubre). *MRO: Maintenance, repair, & operations - A practical guide*. https://www.maintainnow.app/learn/guides/mro-maintenance-repair-operations-a-practical-guide</p>

<p style="padding-left: 30px; text-indent: -30px;">Energym. (2023). *Why do gym members cancel their memberships?* https://energym.io/blogs/braingains/why-do-gym-members-cancel-their-memberships</p>

<p style="padding-left: 30px; text-indent: -30px;">Oxmaint. (2023). *Corrective vs. preventive work orders*. https://www.oxmaint.com/blog/post/corrective-vs-preventive-work-orders</p>

<p style="padding-left: 30px; text-indent: -30px;">Fitness Store. (2024). *Commercial & professional treadmills*. https://www.topfitness.com/collections/commercial-treadmills</p>

## Anexos

### Anexo A : Videos de Exposiciones

| Entrega | Título de la Exposición | Hipervínculo al Video (Microsoft Stream) |
| :--- | :--- | :--- |
| **AV1** | Sprint Review - Semana 4 | [Enlace al video AV1 - SpotTrack](URL_AQUI) |
| **TB1** | Stage Review - Semana 7 | (Pendiente) |
| **AV2** | Sprint Review - Semana 12 | (Pendiente) |
| **TB2** | Release Review - Semana 15 | (Pendiente) |

### Anexo B : Video unificado entrevistas
[Enlace al video unificado de entrevistas - SpotTrack](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202413214_upc_edu_pe/IQDpYTdDwbM1QZOtdJPZIbsQASLFAmK8moRkLLD7ZudoVtM?e=unt1Xd&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)


[Enlace al video unificado de entrevistas de validación - SpotTrack](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202410344_upc_edu_pe/IQDljgiFpIHsRKhGcbeP97MvAf14UGxDGjnNrYevmJVzk6M?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=2kPltB)



### Anexos importantes

* Landing Page: [https://upc-pre-202610-1asi0730-12144-bytesquad.github.io/bytesquad-website/](https://upc-pre-202610-1asi0730-12144-bytesquad.github.io/bytesquad-website/)
* WebApp: [https://green-pebble-07422c50f.7.azurestaticapps.net/](https://green-pebble-07422c50f.7.azurestaticapps.net/)
* Platform: [https://spottrack-platform-aw.azurewebsites.net/](https://spottrack-platform-aw.azurewebsites.net/)
* Organizacion:[https://github.com/upc-pre-202610-1asi0730-12144-bytesquad](https://github.com/upc-pre-202610-1asi0730-12144-bytesquad)
* Repositorio del Report:[https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-report](https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-report)
* Repositorio del Landing page:[https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-website](https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-website)
* Repositorio del WebApp: [https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-webapp](https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-webapp)
* Repositorio del Platform:[https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-platform](https://github.com/upc-pre-202610-1asi0730-12144-bytesquad/bytesquad-platform)

