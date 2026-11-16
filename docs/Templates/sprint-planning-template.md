# Acta de Planificación del Sprint

> **Plantilla.** Copia este archivo a `Records/sprints/sprint-0N/ACT-sprint-0N-planning.md`, reemplaza los textos entre corchetes y borra esta nota.

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SP-00N |
| Nombre del proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Número del Sprint | Sprint N |
| Fecha de planificación | Por definir (YYYY-MM-DD) |
| Hora de inicio | Por definir (HH:MM) |
| Hora de finalización | Por definir (HH:MM) |
| Duración del Sprint | Por definir (sugerido: 2 semanas, YYYY-MM-DD al YYYY-MM-DD) |
| Scrum Master | Por definir |
| Product Owner | Por definir |
| Repositorio del equipo (fork activo) | `https://github.com/PatinoMiguel-22/9Eleven` |
| Repositorio original (upstream / PO) | `https://github.com/FelOnCrackZ/9Eleven` |
| GitHub Project (tablero del equipo) | `https://github.com/users/PatinoMiguel-22/projects/1` |

## 2. Objetivo de la reunión

Definir el objetivo del Sprint, seleccionar los elementos del Product Backlog que serán abordados durante el periodo de trabajo y establecer el plan necesario para alcanzar los resultados esperados.

## 3. Participantes

| Nombre completo | Rol | Asistencia |
|---|---|---|
| [Nombre completo] | Product Owner | Por confirmar (Presente / Ausente) |
| [Nombre completo] | Scrum Master | Por confirmar (Presente / Ausente) |
| [Nombre completo] | Developer | Por confirmar (Presente / Ausente) |
| [Nombre completo] | Developer | Por confirmar (Presente / Ausente) |
| [Nombre completo] | Developer | Por confirmar (Presente / Ausente) |

## 4. Objetivo del Sprint (Sprint Goal)

**Objetivo:**

[Describe en una o dos frases el valor que entregará el Sprint. Debe ser claro y verificable en la Sprint Review.]

## 5. Elementos seleccionados del Product Backlog

Registrar las historias de usuario o elementos del Product Backlog seleccionados para el Sprint. La descripción detallada de cada uno está en `Management/product-backlog.md` y en su issue de GitHub.

| ID | Historia de usuario / Requerimiento | Prioridad | Story Points | Issue |
|---|---|---|---|---|
| US-N01 | Como [rol], quiero [funcionalidad], para [beneficio]. (Referencia a requisito o issue) | Alta / Media / Baja | X | Por crear |
| US-N02 | Como [rol], quiero [funcionalidad], para [beneficio]. | Alta / Media / Baja | X | Por crear |

**Total de Story Points seleccionados:** X

## 6. Descomposición de actividades

Describir las actividades técnicas necesarias. La asignación de responsables la define el equipo junto con el Scrum Master durante el Sprint.

| ID | Actividad | Responsable | Issue relacionado | Estimación |
|---|---|---|---|---|
| TASK-N01 | [Actividad técnica concreta y verificable] (US-N01) | Por asignar (Developer) | Por crear | X h |
| TASK-N02 | [Actividad técnica concreta y verificable] (US-N02) | Por asignar (Developer) | Por crear | X h |

**Total de horas estimadas:** X h

## 7. Criterios de aceptación

Condiciones que deben cumplirse para considerar terminada cada historia. Cómo redactarlos: `Management/acceptance-criteria-and-dod.md`.

**US-N01**

- [ ] [Condición observable que debe cumplirse: caso exitoso.]
- [ ] [Condición observable: caso de error o de permisos.]

**US-N02**

- [ ] [Condición observable que debe cumplirse.]

**Criterio general del Sprint**

- [ ] [Recorrido o demostración que el equipo hará en la Sprint Review.]

## 8. Definición de terminado (Definition of Done)

Aplica la definición completa de `Management/acceptance-criteria-and-dod.md`. Resumen:

- [ ] La funcionalidad cumple los criterios de aceptación.
- [ ] Los archivos modificados pasan `php -l` sin errores.
- [ ] Se probó manualmente en XAMPP con datos de ejemplo: un caso exitoso y uno de error.
- [ ] Se respetan las reglas de seguridad: `requerirLogin()`, consultas preparadas y salida con `h()`.
- [ ] No se versionan contraseñas ni credenciales reales.
- [ ] La documentación se actualizó cuando corresponde.
- [ ] El Pull Request fue revisado y aprobado por otro integrante.
- [ ] Los cambios se integraron a `main` y el issue pasó a *Done*.

## 9. Plan de trabajo

Las fechas reales se registran al confirmar el calendario del Sprint (día 1 = primer día del Sprint).

| Actividad | Inicio | Fin estimado | Responsable |
|---|---|---|---|
| US-N01: [nombre] | Día X | Día Y | Equipo de desarrollo |
| US-N02: [nombre] | Día X | Día Y | Equipo de desarrollo |
| Revisión de avance con el Product Owner | Día X | Día X | Scrum Master y Product Owner |
| Sprint Review y Retrospectiva | Día X | Día X | Todo el equipo Scrum |

## 10. Riesgos, dependencias e impedimentos

| ID | Descripción | Impacto | Acción preventiva o correctiva | Responsable |
|---|---|---|---|---|
| RISK-N01 | [Situación que podría afectar al Sprint.] | Alto / Medio / Bajo | [Acción preventiva o correctiva.] | [Responsable] |

## 11. Acuerdos y compromisos

| ID | Acuerdo o compromiso | Responsable | Fecha límite |
|---|---|---|---|
| AC-001 | [Acuerdo o compromiso.] | [Responsable] | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Product Backlog: `Management/product-backlog.md` y el tablero del equipo
- Issues seleccionados: pendientes de crear
- Documentación relacionada: `Requirements/`, `Resources/`, `Management/`, `README.md`
- Grabación de la reunión (si aplica): Por definir

## 13. Observaciones

- [Observaciones, supuestos o estado del proyecto al iniciar el Sprint.]
- Los campos «Por definir» o «Por confirmar» se completan con la información real de la reunión antes de la aprobación del acta.

## 14. Aprobación y validación

Los participantes dejan constancia de que revisaron el objetivo del Sprint, los elementos seleccionados y el plan de trabajo.

| Participante | Rol | Usuario de GitHub | Fecha |
|---|---|---|---|
| [Nombre completo] | Product Owner | [@usuario] | YYYY-MM-DD |
| [Nombre completo] | Scrum Master | [@usuario] | YYYY-MM-DD |
| [Nombre completo] | Developer | [@usuario] | YYYY-MM-DD |
| [Nombre completo] | Developer | [@usuario] | YYYY-MM-DD |
| [Nombre completo] | Developer | [@usuario] | YYYY-MM-DD |

### Estado de la planificación

- [ ] Objetivo del Sprint definido.
- [ ] Elementos del Product Backlog seleccionados y estimados.
- [ ] Criterios de aceptación revisados.
- [ ] Plan de trabajo establecido.
- [ ] Compromisos registrados.
- [ ] Acta revisada por los participantes.

**Evidencia de aprobación:** [URL del Pull Request o discusión correspondiente]

---

**Fin del documento**

*Este documento constituye el registro formal de la planificación del Sprint. Cualquier modificación significativa del alcance, los acuerdos o los elementos seleccionados deberá quedar documentada y contar con la correspondiente trazabilidad.*
