# Records — Registros del proyecto

Aquí se guarda la evidencia de cómo se trabajó: cada reunión y cada Sprint dejan un acta.

```
Records/
├── meetings/                      Actas de reuniones
│   └── ACT-MIN-001-meeting-kickoff.md
├── sprints/                       Un folder por Sprint (4 en total)
│   ├── sprint-01/  ACT-sprint-01-planning.md · ACT-SR-01-review.md · ACT-RET-01-retrospective.md
│   ├── sprint-02/  …
│   ├── sprint-03/  …
│   └── sprint-04/  …
└── project-acceptance.md          Acta de aceptación y cierre del proyecto (ACT-PA-001)
```

## Convención de nombres

| Documento | Código | Archivo | Plantilla |
|---|---|---|---|
| Acta de reunión | `ACT-MIN-00N` | `meetings/ACT-MIN-00N-meeting-tema.md` | `Templates/meeting-minutes-template.md` |
| Planificación del Sprint | `ACT-SP-00N` | `sprints/sprint-0N/ACT-sprint-0N-planning.md` | `Templates/sprint-planning-template.md` |
| Revisión del Sprint | `ACT-SR-00N` | `sprints/sprint-0N/ACT-SR-0N-review.md` | `Templates/sprint-review-template.md` |
| Retrospectiva del Sprint | `ACT-RET-00N` | `sprints/sprint-0N/ACT-RET-0N-retrospective.md` | `Templates/sprint-retrospective-template.md` |
| Aceptación del proyecto | `ACT-PA-001` | `project-acceptance.md` | — (ya viene preparada) |

## Estado de los documentos

Los archivos de `sprints/` y `project-acceptance.md` vienen **preparados al inicio**: la planificación trae una propuesta de alcance basada en [`../Management/product-backlog.md`](../Management/product-backlog.md), y la revisión y la retrospectiva traen los datos de la planificación con los resultados en «Pendiente» o «Por registrar».

El equipo los completa **durante** cada evento. Mientras un campo diga `Por definir`, `Por registrar` o `Por confirmar`, ese dato todavía no es real.

## Reglas

- Una acta no se borra ni se reescribe después de aprobada; si hay un cambio, se agrega una nota con fecha.
- Las actas se aprueban por Pull Request hacia `main` en el repositorio de desarrollo activo (`https://github.com/PatinoMiguel-22/9Eleven`, ver [`../Management/github-workflow.md`](../Management/github-workflow.md)).
- Este repositorio es público: no se escriben documentos de identidad, contraseñas ni datos privados en las actas.
