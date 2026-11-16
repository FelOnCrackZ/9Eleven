# Acta de Planificación del Sprint 4

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SP-004 |
| Nombre del proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Número del Sprint | Sprint 4 |
| Fecha de planificación | Por definir (YYYY-MM-DD) |
| Hora de inicio | Por definir (HH:MM) |
| Hora de finalización | Por definir (HH:MM) |
| Duración del Sprint | Por definir (sugerido: 2 semanas, YYYY-MM-DD al YYYY-MM-DD) |
| Scrum Master | Miguel Ángel Patiño Caicedo |
| Product Owner | Felipe Nuñez Navarro |
| Repositorio del equipo (fork activo) | `https://github.com/PatinoMiguel-22/9Eleven` |
| Repositorio original (upstream / PO) | `https://github.com/FelOnCrackZ/9Eleven` |
| GitHub Project (tablero del equipo) | `https://github.com/users/PatinoMiguel-22/projects/1` |

## 2. Objetivo de la reunión

Definir el objetivo del Sprint, seleccionar los elementos del Product Backlog que serán abordados durante el periodo de trabajo y establecer el plan necesario para alcanzar los resultados esperados.

## 3. Participantes

| Nombre completo | Rol | Asistencia |
|---|---|---|
| Felipe Nuñez Navarro | Product Owner | Por confirmar (Presente / Ausente) |
| Miguel Ángel Patiño Caicedo | Scrum Master | Por confirmar (Presente / Ausente) |
| Miguel Angel Herrera Lujan | Developer | Por confirmar (Presente / Ausente) |
| Ralay Montaño Hurtado | Developer | Por confirmar (Presente / Ausente) |
| Brahian Alonso Alzate Toro | Developer | Por confirmar (Presente / Ausente) |

## 4. Objetivo del Sprint (Sprint Goal)

**Objetivo:**

Cerrar el proyecto: completar los reportes, endurecer la seguridad, ofrecer recuperación de contraseña y entregar la versión v1.0.0 lista para la aceptación.

## 5. Elementos seleccionados del Product Backlog

Propuesta inicial construida a partir de `Management/product-backlog.md`. El equipo la valida, estima y ajusta durante la Sprint Planning. Las referencias «Backlog #N» corresponden a los issues descritos en ese documento.

| ID | Historia de usuario / Requerimiento | Prioridad | Story Points | Issue |
|---|---|---|---|---|
| US-401 | Como administrador, quiero los cuatro reportes del documento funcional para tomar decisiones sobre el inventario. | Alta | 3 | Por crear (Backlog #8) |
| US-402 | Como administrador, quiero una página de alertas con categoría, faltante y proveedores sugeridos para reponer a tiempo. | Media | 1 | Por crear (Backlog #7) |
| US-403 | Como equipo, queremos cerrar las brechas de seguridad de sesión, formularios y errores para poder desplegar el sistema. | Alta | 3 | Por crear (Backlog #9) |
| US-404 | Como administrador, quiero restablecer mi contraseña olvidada mediante un enlace, para recuperar el acceso. (Deseable: es la primera historia en moverse si falta capacidad) | Media | 2 | Por crear (Backlog #10) |
| US-405 | Como equipo, queremos ejecutar el escenario manual, corregir errores y publicar la versión v1.0.0. | Alta | 1 | Por crear |

**Total de Story Points seleccionados:** 10

## 6. Descomposición de actividades

Describir las actividades técnicas necesarias. La asignación de responsables la define el equipo junto con el Scrum Master durante el Sprint.

| ID | Actividad | Responsable | Issue relacionado | Estimación |
|---|---|---|---|---|
| TASK-401 | Reporte de movimientos de inventario con rango de fechas (US-401) | Por asignar (Developer) | Por crear | 4 h |
| TASK-402 | Reportes de stock bajo y de valor total del inventario (US-401) | Por asignar (Developer) | Por crear | 3 h |
| TASK-403 | Reemplazar la tarjeta duplicada «VENTA MES» y mostrar importes con `formatoPesos()` (US-401) | Por asignar (Developer) | Por crear | 1 h |
| TASK-404 | Alertas: categoría, faltante y proveedores sugeridos; enlace «Ver todas» desde el dashboard (US-402) | Por asignar (Developer) | Por crear | 3 h |
| TASK-405 | Token CSRF en todos los formularios POST (US-403) | Por asignar (Developer) | Por crear | 4 h |
| TASK-406 | Cookies de sesión `HttpOnly` y `SameSite`; `cerrarSesion.php` borra la cookie y funciona por POST (US-403) | Por asignar (Developer) | Por crear | 2 h |
| TASK-407 | Límite de intentos de login; mensajes de error genéricos y registro en un log (US-403) | Por asignar (Developer) | Por crear | 3 h |
| TASK-408 | Post/Redirect/Get en las acciones POST que modifican datos (US-403) | Por asignar (Developer) | Por crear | 2 h |
| TASK-409 | Flujo «Olvidé mi contraseña» con token, expiración y un solo uso (US-404) | Por asignar (Developer) | Por crear | 5 h |
| TASK-410 | Ensayo del escenario manual completo de 9 pasos (US-405) | Por asignar (Developer) | Por crear | 2 h |
| TASK-411 | Actualizar README y registrar los pendientes como issues (US-405) | Por asignar (Developer) | Por crear | 2 h |
| TASK-412 | Congelamiento de código, correcciones menores y publicación del release v1.0.0 (US-405) | Por asignar (Developer) | Por crear | 2 h |

**Total de horas estimadas:** 33 h

## 7. Criterios de aceptación

Condiciones que deben cumplirse para considerar terminada cada historia. Cómo redactarlos: `Management/acceptance-criteria-and-dod.md`.

**US-401**

- [ ] `reportes.php` incluye los cuatro reportes de RF-14: movimientos de inventario, productos más vendidos, stock bajo y valor total del inventario.
- [ ] Los reportes con fechas aceptan un rango desde/hasta.
- [ ] La tarjeta duplicada «VENTA MES» fue reemplazada y los importes usan `formatoPesos()`.

**US-402**

- [ ] `alertaStock.php` muestra categoría y unidades faltantes, y sugiere proveedores de la misma categoría.
- [ ] El dashboard enlaza a la página completa y ordena igual que ella.

**US-403**

- [ ] Todos los formularios POST incluyen y validan un token CSRF.
- [ ] Las cookies de sesión usan `HttpOnly` y `SameSite`; `cerrarSesion.php` borra la cookie y funciona por POST.
- [ ] El login limita los intentos fallidos.
- [ ] Los errores inesperados muestran un mensaje genérico y se registran en un log.
- [ ] Tras un POST exitoso se redirige (Post/Redirect/Get).

**US-404**

- [ ] Existe «Olvidé mi contraseña»: pide el correo y genera un token con expiración y un solo uso.
- [ ] La respuesta es la misma exista o no el correo.
- [ ] Sin servidor de correo, en desarrollo el enlace se escribe en un log.

**US-405**

- [ ] El escenario manual de 9 pasos (ver `Records/project-acceptance.md`) se ejecuta sin fallos sobre una instalación limpia.
- [ ] Todos los pendientes quedan registrados como issues.
- [ ] El release v1.0.0 queda publicado en GitHub.

**Criterio general del Sprint**

- [ ] El equipo ejecuta ante el Product Owner el escenario manual de 9 pasos sobre una instalación limpia.

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
| Cierre de pendientes del Sprint 3 (si los hay) | Día 1 | Día 2 | Equipo de desarrollo |
| US-401: Reportes | Día 1 | Día 4 | Equipo de desarrollo |
| US-402: Alertas de stock | Día 3 | Día 4 | Equipo de desarrollo |
| US-403: Seguridad | Día 2 | Día 7 | Equipo de desarrollo |
| Revisión de avance con el Product Owner | Día 4 | Día 4 | Scrum Master y Product Owner |
| US-404: Recuperar contraseña (deseable) | Día 5 | Día 8 | Equipo de desarrollo |
| Congelamiento de código | Día 9 | Día 9 | Equipo de desarrollo |
| US-405: Escenario manual, correcciones y release | Día 9 | Día 10 | Equipo de desarrollo |
| Sprint Review final y aceptación del proyecto | Día 10 | Día 10 | Todo el equipo Scrum |

## 10. Riesgos, dependencias e impedimentos

| ID | Descripción | Impacto | Acción preventiva o correctiva | Responsable |
|---|---|---|---|---|
| RISK-401 | El token CSRF toca todos los formularios y puede generar conflictos entre ramas. | Alto | Implementar primero una función común y aplicarla en Pull Requests separados por módulo. | Equipo de desarrollo |
| RISK-402 | XAMPP no trae servidor de correo, lo que dificulta probar la recuperación de contraseña. | Medio | Escribir el enlace en un log en desarrollo; PHPMailer + SMTP solo en despliegue. | Equipo de desarrollo |
| RISK-403 | Falta de tiempo por el cierre del semestre. | Medio | Congelar el código antes de la Review y priorizar correcciones; US-404 es la primera en moverse. | Scrum Master |
| RISK-404 | Documentación desactualizada al entregar. | Medio | Actualizar el README y los diagramas antes del congelamiento. | Equipo de desarrollo |
| DEP-401 | US-401 (movimientos de inventario) depende de las entradas del Sprint 3 (US-302). | Alto | Confirmar su estado en la Sprint Review del Sprint 3. | Scrum Master |

## 11. Acuerdos y compromisos

| ID | Acuerdo o compromiso | Responsable | Fecha límite |
|---|---|---|---|
| AC-001 | Congelar el código el penúltimo día del Sprint: después solo se corrigen errores y se prepara la demostración. | Scrum Master | Por definir |
| AC-002 | Realizar la demostración del escenario manual ante el Product Owner y registrar la decisión de aceptación (ACT-PA-001). | Product Owner | Por definir |
| AC-003 | Publicar el release v1.0.0 en GitHub con los entregables finales. | Scrum Master | Por definir |
| AC-004 | Registrar como issues los pendientes (paginación, Docker, pruebas automáticas), para que no se entiendan como funcionalidades entregadas. | Scrum Master | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Product Backlog: `Management/product-backlog.md` y el tablero del equipo
- Issues seleccionados: pendientes de crear
- Documentación relacionada: `Requirements/`, `Resources/`, `Management/`, `README.md`
- Grabación de la reunión (si aplica): Por definir

## 13. Observaciones

- Metas opcionales fuera del compromiso: paginación y buscador (Backlog #14), Docker (Backlog #15) y pruebas/CI (Backlog #16). Se desarrollan solo si el equipo termina antes.
- Los campos «Por definir» se completan con la información real de la reunión antes de la aprobación del acta.
- Los campos «Por definir» o «Por confirmar» se completan con la información real de la reunión antes de la aprobación del acta.

## 14. Aprobación y validación

Los participantes dejan constancia de que revisaron el objetivo del Sprint, los elementos seleccionados y el plan de trabajo.

| Participante | Rol | Usuario de GitHub | Fecha |
|---|---|---|---|
| Felipe Nuñez Navarro | Product Owner | @FelOnCrackZ | YYYY-MM-DD |
| Miguel Ángel Patiño Caicedo | Scrum Master | @PatinoMiguel-22 | YYYY-MM-DD |
| Miguel Angel Herrera Lujan | Developer | @Miguel-lujan2032 | YYYY-MM-DD |
| Ralay Montaño Hurtado | Developer | @raly-cpu | YYYY-MM-DD |
| Brahian Alonso Alzate Toro | Developer | @AlzateBrahian07 | YYYY-MM-DD |

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
