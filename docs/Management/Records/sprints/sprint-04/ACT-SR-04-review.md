# Acta de Revisión del Sprint 4

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SR-004 |
| Proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Sprint | Sprint 4 |
| Fecha de revisión | Por definir (YYYY-MM-DD) |
| Hora de inicio | Por definir (HH:MM) |
| Hora de finalización | Por definir (HH:MM) |
| Scrum Master | Miguel Ángel Patiño Caicedo |
| Product Owner | Felipe Nuñez Navarro |
| Repositorio del equipo (fork activo) | `https://github.com/PatinoMiguel-22/9Eleven` |
| Repositorio original (upstream / PO) | `https://github.com/FelOnCrackZ/9Eleven` |
| GitHub Project (tablero del equipo) | `https://github.com/users/PatinoMiguel-22/projects/1` |

## 2. Objetivo de la reunión

Inspeccionar los resultados obtenidos durante el Sprint, revisar el Incremento desarrollado, verificar el cumplimiento de los criterios de aceptación y recopilar retroalimentación para orientar las siguientes etapas del proyecto.

Esta acta se prepara al inicio del Sprint con los datos de la planificación (ACT-SP-004). Las columnas de estado, resultado y evidencia se completan durante la Sprint Review; hasta entonces permanecen como «Pendiente» o «Por registrar».

## 3. Participantes

| Nombre completo | Rol | Asistencia |
|---|---|---|
| Felipe Nuñez Navarro | Product Owner | Por confirmar |
| Miguel Ángel Patiño Caicedo | Scrum Master | Por confirmar |
| Miguel Angel Herrera Lujan | Developer | Por confirmar |
| Ralay Montaño Hurtado | Developer | Por confirmar |
| Brahian Alonso Alzate Toro | Developer | Por confirmar |
| [Nombre o cargo] | Interesado / Invitado (opcional) | Por confirmar |

## 4. Objetivo del Sprint

**Sprint Goal establecido:**

Cerrar el proyecto: completar los reportes, endurecer la seguridad, ofrecer recuperación de contraseña y entregar la versión v1.0.0 lista para la aceptación.

**Resultado general:**

[Se completa en la Sprint Review: indicar si se alcanzó el objetivo.]

## 5. Revisión de los elementos del Sprint Backlog

| ID | Elemento seleccionado | Estado | Story Points | Issue |
|---|---|---|---|---|
| US-401 | Reportes completos | Pendiente | 3 | Por crear |
| US-402 | Página de alertas de stock | Pendiente | 1 | Por crear |
| US-403 | Seguridad de sesión y formularios | Pendiente | 3 | Por crear |
| US-404 | Recuperar contraseña (deseable) | Pendiente | 2 | Por crear |
| US-405 | Escenario manual y release v1.0.0 | Pendiente | 1 | Por crear |

**Total de Story Points planificados:** 10

**Total de Story Points completados:** Por registrar

Nota: según la planificación (ACT-SP-004), si falta capacidad la primera historia en moverse al Product Backlog es US-404.

## 6. Incremento desarrollado

Funcionalidades previstas para el Incremento (versión v1.0.0).

| ID | Funcionalidad | Descripción | Evidencia |
|---|---|---|---|
| INC-001 | Reportes completos | Entrega de US-401 según sus criterios de aceptación | Por registrar |
| INC-002 | Página de alertas de stock | Entrega de US-402 según sus criterios de aceptación | Por registrar |
| INC-003 | Seguridad de sesión y formularios | Entrega de US-403 según sus criterios de aceptación | Por registrar |
| INC-004 | Recuperar contraseña (deseable) | Entrega de US-404 según sus criterios de aceptación | Por registrar |
| INC-005 | Escenario manual y release v1.0.0 | Entrega de US-405 según sus criterios de aceptación | Por registrar |
| INC-006 | Documentación | README y documentos de `Records/` actualizados | Por registrar |

## 7. Validación de criterios de aceptación

Los criterios completos están en la sección 7 de ACT-SP-004.

| ID | Criterio de aceptación | Resultado | Observaciones |
|---|---|---|---|
| CA-001 | US-401: `reportes.php` incluye los cuatro reportes de RF-14: movimientos de inventario, productos más vendidos, stock bajo y valor total del inventario. | Pendiente | Por registrar |
| CA-002 | US-401: Los reportes con fechas aceptan un rango desde/hasta. | Pendiente | Por registrar |
| CA-003 | US-401: La tarjeta duplicada «VENTA MES» fue reemplazada y los importes usan `formatoPesos()`. | Pendiente | Por registrar |
| CA-004 | US-402: `alertaStock.php` muestra categoría y unidades faltantes, y sugiere proveedores de la misma categoría. | Pendiente | Por registrar |
| CA-005 | US-402: El dashboard enlaza a la página completa y ordena igual que ella. | Pendiente | Por registrar |
| CA-006 | US-403: Todos los formularios POST incluyen y validan un token CSRF. | Pendiente | Por registrar |
| CA-007 | US-403: Las cookies de sesión usan `HttpOnly` y `SameSite`; `cerrarSesion.php` borra la cookie y funciona por POST. | Pendiente | Por registrar |
| CA-008 | US-403: El login limita los intentos fallidos. | Pendiente | Por registrar |
| CA-009 | US-403: Los errores inesperados muestran un mensaje genérico y se registran en un log. | Pendiente | Por registrar |
| CA-010 | US-403: Tras un POST exitoso se redirige (Post/Redirect/Get). | Pendiente | Por registrar |
| CA-011 | US-404: Existe «Olvidé mi contraseña»: pide el correo y genera un token con expiración y un solo uso. | Pendiente | Por registrar |
| CA-012 | US-404: La respuesta es la misma exista o no el correo. | Pendiente | Por registrar |
| CA-013 | US-404: Sin servidor de correo, en desarrollo el enlace se escribe en un log. | Pendiente | Por registrar |
| CA-014 | US-405: El escenario manual de 9 pasos (ver `Records/project-acceptance.md`) se ejecuta sin fallos sobre una instalación limpia. | Pendiente | Por registrar |
| CA-015 | US-405: Todos los pendientes quedan registrados como issues. | Pendiente | Por registrar |
| CA-016 | US-405: El release v1.0.0 queda publicado en GitHub. | Pendiente | Por registrar |
| CA-017 | General: El equipo ejecuta ante el Product Owner el escenario manual de 9 pasos sobre una instalación limpia. | Pendiente | Por registrar |

## 8. Pull Requests y evidencias técnicas

| Pull Request | Descripción | Estado | Revisor |
|---|---|---|---|
| Por registrar | US-401 | Pendiente | Por asignar |
| Por registrar | US-402 | Pendiente | Por asignar |
| Por registrar | US-403 | Pendiente | Por asignar |
| Por registrar | US-404 | Pendiente | Por asignar |
| Por registrar | US-405 | Pendiente | Por asignar |

**Otras evidencias:**

- Revisión de sintaxis: Por registrar (`php -l` sobre los archivos modificados).
- Pruebas manuales en XAMPP: Por registrar (casos exitosos y de error).
- Capturas de pantalla: Por registrar.
- Documentación técnica: README y `Records/` actualizados.
- Versión o demostración: Por registrar (v1.0.0).

## 9. Retroalimentación del Product Owner y los interesados

**Aspectos satisfactorios:**

[Se completa en la Sprint Review.]

**Observaciones y oportunidades de mejora:**

[Se completa en la Sprint Review.]

**Nuevas necesidades identificadas:**

[Se completa en la Sprint Review.]

## 10. Elementos pendientes

| ID | Elemento pendiente | Motivo | Acción propuesta |
|---|---|---|---|
| PEND-001 | Por registrar | Por registrar | Por registrar |

Los elementos no completados regresan al Product Backlog para su evaluación y priorización. No se consideran automáticamente comprometidos para el siguiente Sprint.

## 11. Acuerdos y decisiones

| ID | Acuerdo o decisión | Responsable | Fecha límite |
|---|---|---|---|
| AC-001 | Registrar el resultado de la demostración | Scrum Master | Por definir |
| AC-002 | Devolver los pendientes al Product Backlog | Product Owner | Por definir |
| AC-003 | Publicar el release v1.0.0 en GitHub | Scrum Master | Por definir |
| AC-004 | Registrar la decisión de aceptación en ACT-PA-001 | Product Owner | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Pull Requests: Por registrar
- Incremento presentado: Por registrar (v1.0.0)
- Documentación relacionada: ACT-SP-004 y `Requirements/`

## 13. Observaciones

- La Sprint Review es una sesión de inspección y adaptación del producto, no solo una presentación de resultados.
- Los campos «Por registrar», «Por confirmar» y «Por definir» se completan con la información real de la reunión antes de la aprobación del acta.

## 14. Validación y aprobación

| Participante | Rol | Usuario de GitHub | Fecha |
|---|---|---|---|
| Felipe Nuñez Navarro | Product Owner | @FelOnCrackZ | YYYY-MM-DD |
| Miguel Ángel Patiño Caicedo | Scrum Master | @PatinoMiguel-22 | YYYY-MM-DD |
| Miguel Angel Herrera Lujan | Developer | @Miguel-lujan2032 | YYYY-MM-DD |
| Ralay Montaño Hurtado | Developer | @raly-cpu | YYYY-MM-DD |
| Brahian Alonso Alzate Toro | Developer | @AlzateBrahian07 | YYYY-MM-DD |

### Estado de la revisión

- [ ] Se presentó el Incremento desarrollado.
- [ ] Se revisaron los elementos del Sprint Backlog.
- [ ] Se verificaron los criterios de aceptación.
- [ ] Se registró la retroalimentación.
- [ ] Se identificaron elementos pendientes.
- [ ] Se documentaron los acuerdos y decisiones.

**Evidencia de aprobación:** [URL del Pull Request o discusión correspondiente]

---

**Fin del documento**
