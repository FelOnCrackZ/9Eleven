# Lineamientos de Scrum — 9Eleven

Cómo trabaja el equipo. Es una adaptación de Scrum al contexto del curso: equipos de 3 a 5 personas, reuniones remotas y un semestre dividido en **4 Sprints**.

## 1. Roles

| Rol | Responsabilidades |
|---|---|
| **Product Owner** | Dueño del *qué*. Mantiene y ordena el Product Backlog, define el Sprint Goal junto con el equipo, responde dudas de negocio, **valida** los criterios de aceptación en la Review y aprueba cualquier cambio de alcance. |
| **Scrum Master** | Facilita los eventos, protege el proceso, ayuda a quitar impedimentos y vela porque las actas y el tablero estén al día. No es jefe del equipo ni asigna tareas por su cuenta. |
| **Developers** | Estiman, descomponen, construyen, prueban y revisan Pull Requests. Se autoorganizan para repartir el trabajo. |

Una persona **no aprueba su propio Pull Request**. Los roles pueden rotar entre Sprints si el equipo lo acuerda y lo deja en el acta.

## 2. Artefactos

| Artefacto | Dónde vive |
|---|---|
| **Product Backlog** | [`product-backlog.md`](product-backlog.md) y el tablero de GitHub Project |
| **Sprint Backlog** | Los issues seleccionados en la Sprint Planning (columnas *Ready* → *Done* del tablero) |
| **Incremento** | La versión funcional en la rama `main`, con su etiqueta (`v0.1.0`, `v0.2.0`, `v0.3.0`, `v1.0.0`) |

Los compromisos de cada artefacto son: el Product Backlog → el objetivo del producto; el Sprint Backlog → el **Sprint Goal**; el Incremento → la **Definition of Done** ([ver aquí](acceptance-criteria-and-dod.md)).

## 3. Calendario y duración de los eventos

Cada Sprint dura **1 o 2 semanas** (se recomienda 2). El Sprint Goal no cambia durante el Sprint; si algo se vuelve imposible, el Product Owner y el equipo renegocian el alcance, no el objetivo.

| Evento | Cuándo | Duración máxima (Sprint de 2 semanas) | Acta |
|---|---|---|---|
| Sprint Planning | Primer día del Sprint | 2 horas | `ACT-SP-00N` |
| Daily | Cada día de trabajo (puede ser asíncrono) | 15 minutos | No requiere acta |
| Revisión de avance con el PO | Mitad del Sprint | 30 minutos | Nota en la planificación |
| Sprint Review | Último día | 1 hora | `ACT-SR-00N` |
| Retrospective | Último día, después de la Review | 45 a 60 minutos | `ACT-RET-00N` |

## 4. Cómo hacemos la Sprint Planning

**Objetivo:** definir el Sprint Goal, elegir qué historias entran y dejar un plan realista.

### Antes de la reunión

- [ ] El Product Owner ordena el Product Backlog por prioridad.
- [ ] El Scrum Master copia [`../Templates/sprint-planning-template.md`](../Templates/sprint-planning-template.md) a `Records/sprints/sprint-0N/` y precarga lo que ya se sabe.
- [ ] Todos leen las historias candidatas y los criterios de aceptación propuestos.
- [ ] Se revisan los pendientes del Sprint anterior (volvieron al Backlog en la Review).
- [ ] Cada Developer indica cuántas horas puede dedicar al Sprint (capacidad).

### Durante la reunión (2 horas)

| Minutos | Paso | Resultado |
|---|---|---|
| 10 | Resumen del Sprint anterior y capacidad disponible | Capacidad en horas |
| 10 | El Product Owner propone el **Sprint Goal** | Objetivo acordado |
| 40 | Se eligen historias y se **estiman en Story Points** (Planning Poker) | Sprint Backlog con total de SP |
| 30 | Cada historia se **descompone en tareas** con horas | Tabla de `TASK-xxx` |
| 15 | Se revisan **criterios de aceptación**, riesgos y dependencias | Criterios y riesgos registrados |
| 15 | Acuerdos, fechas y responsables | Plan de trabajo |

### Reglas

- No se compromete más trabajo del que cabe en la capacidad. Las horas estimadas no deben superar la suma de las capacidades individuales.
- Toda historia seleccionada debe cumplir la **Definition of Ready**.
- Si algo no cabe, queda en el Product Backlog; no se «mete a la fuerza».
- Todo cambio de alcance durante el Sprint lo aprueba el Product Owner.

### Después de la reunión

- [ ] El Scrum Master completa el acta `ACT-SP-00N` y abre un Pull Request.
- [ ] Se crean los issues (historias y tareas) con su ID y sus Story Points, y se mueven a *Ready*.
- [ ] Los participantes aprueban el acta comentando o aprobando el PR.

## 5. Cómo hacemos la Sprint Review

**Objetivo:** inspeccionar el Incremento, validar los criterios de aceptación y recibir retroalimentación. **No es solo una presentación**: se revisa y se decide qué sigue.

| Minutos | Paso |
|---|---|
| 5 | El Scrum Master recuerda el Sprint Goal y qué se planeó |
| 30 | Los Developers **demuestran** cada historia sobre `main`, en una instalación limpia o con la base de ejemplo, recorriendo sus criterios de aceptación (caso exitoso y caso de error) |
| 10 | El Product Owner marca cada criterio como **Cumplido**, **Parcial** o **No cumplido** |
| 10 | Retroalimentación del Product Owner e interesados; nuevas necesidades |
| 5 | Pendientes: lo no terminado **vuelve al Product Backlog** (no pasa solo al siguiente Sprint) |

**Reglas**

- Solo se demuestra lo que cumple la Definition of Done. Lo que no la cumple se reporta como pendiente.
- Presentan los Developers, preferiblemente rotando.
- Se publica la versión (`vX.Y.Z`) del Incremento aceptado.
- El Scrum Master completa `ACT-SR-00N` con los resultados y la evidencia (PRs, capturas, versión).

## 6. Cómo hacemos la Retrospective

**Objetivo:** mejorar la forma de trabajar. Se habla del proceso, no de culpables.

| Minutos | Paso |
|---|---|
| 5 | Revisar las acciones de la retrospectiva anterior: ¿se cumplieron? |
| 15 | Cada persona escribe tarjetas en tres columnas: **¿Qué funcionó bien? / ¿Qué dificultades hubo? / ¿Qué podemos mejorar?** (también sirve el formato Start–Stop–Continue) |
| 10 | Se agrupan tarjetas parecidas y se votan las más importantes |
| 15 | Se definen **máximo 3 acciones** concretas, cada una con responsable y fecha |
| 5 | Cierre: cada acción se convierte en un issue |

**Reglas**

- Se evalúan los datos reales: SP planificados frente a completados y horas estimadas frente a reales.
- Una acción de mejora debe ser verificable («revisar los PR en menos de 24 h»), no un deseo («comunicarnos mejor»).
- Las acciones se llevan a la siguiente Sprint Planning y se revisan al inicio de la siguiente retrospectiva.
- El Scrum Master completa `ACT-RET-00N`.

## 7. Daily

Cada persona responde: ¿qué hice desde la última vez?, ¿qué haré hoy? y ¿qué me bloquea? Puede hacerse por el canal del equipo si no hay reunión. Los impedimentos pasan al Scrum Master el mismo día.

## 8. Estimación y capacidad

Se usan **Story Points** con la escala 1, 2, 3, 5 y 8. Se estiman en relación unas con otras, no en horas.

| SP | Referencia en 9Eleven |
|---|---|
| 1 | Cambio pequeño en una página (por ejemplo, un campo o un mensaje) |
| 2 | Funcionalidad sencilla con validaciones (por ejemplo, editar una categoría) |
| 3 | Flujo completo en una página con validaciones y casos de error (editar productos) |
| 5 | Flujo con varias tablas y transacciones (nueva venta con descuento de stock) |
| 8 | Demasiado grande: se **divide** antes de entrar a un Sprint |

Como referencia inicial, un equipo de 3 a 4 personas compromete **unos 10 Story Points por Sprint de 2 semanas**. Tras el Sprint 1 se ajusta con la velocidad real (los SP que sí se completaron).

## 9. Registro de eventos

Cada evento deja un acta en [`../Records/`](../Records/) hecha con la plantilla de [`../Templates/`](../Templates/). Las actas se aprueban por Pull Request. Los números de código coinciden con el número del Sprint (`ACT-SP-001` es la planificación del Sprint 1).

## 10. Acuerdos de trabajo

- Una rama por historia, creada desde `main`. Ver [`github-workflow.md`](github-workflow.md).
- Todo Pull Request lo revisa otra persona del equipo.
- El tablero se actualiza al mover cada issue.
- Se consulta al Product Owner antes de agregar alcance.
- `main` siempre queda funcionando.
- Las decisiones importantes se registran en el acta que corresponda.
