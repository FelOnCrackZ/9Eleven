# Templates — Plantillas

Plantillas para los documentos que el equipo genera durante el proyecto. **No se editan para registrar un evento real**: se copian a `Records/`, se renombran y se completan.

| Plantilla | Se usa para | Se copia a | Nombre del archivo |
|---|---|---|---|
| `meeting-minutes-template.md` | Acta de cualquier reunión (requerimientos, seguimiento, entrega de contexto…) | `Records/meetings/` | `ACT-MIN-00N-meeting-tema.md` |
| `sprint-planning-template.md` | Planificación de un Sprint | `Records/sprints/sprint-0N/` | `ACT-sprint-0N-planning.md` |
| `sprint-review-template.md` | Revisión del Sprint (demostración del Incremento) | `Records/sprints/sprint-0N/` | `ACT-SR-0N-review.md` |
| `sprint-retrospective-template.md` | Retrospectiva del Sprint | `Records/sprints/sprint-0N/` | `ACT-RET-0N-retrospective.md` |

## Cómo usarlas

1. Copia la plantilla a su carpeta de destino y renómbrala según la tabla.
2. Reemplaza todo lo que esté entre corchetes `[ ]` y los valores `Por definir`, `Por registrar` y `Por confirmar` con la información real.
3. Borra la nota «Plantilla» del inicio del archivo.
4. Sube el acta en una rama (`docs/ACT-SP-00N`) y abre un Pull Request hacia `main` en el repositorio activo (`https://github.com/PatinoMiguel-22/9Eleven`). La aprobación de los participantes queda como revisión o comentario en ese PR.

## Reglas

- El número del código (`ACT-SP-001`, `ACT-SR-001`…) coincide con el número del Sprint o de la reunión.
- No se incluyen documentos de identidad, contraseñas ni datos personales sensibles en las actas: este repositorio es público.
- Si una sección no aplica, se deja con «No aplica» en lugar de borrarla, para conservar la estructura.
