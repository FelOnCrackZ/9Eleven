# Acta de Revisión del Sprint 1

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SR-001 |
| Proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Sprint | Sprint 1 |
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

Esta acta se prepara al inicio del Sprint con los datos de la planificación (ACT-SP-001). Las columnas de estado, resultado y evidencia se completan durante la Sprint Review; hasta entonces permanecen como «Pendiente» o «Por registrar».

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

Dejar una base de trabajo segura y reproducible: que cualquier integrante pueda instalar 9Eleven desde cero, que las contraseñas se guarden con hash, que la configuración y la zona horaria sean correctas y que eliminar registros no rompa la aplicación.

**Resultado general:**

[Se completa en la Sprint Review: indicar si se alcanzó el objetivo.]

## 5. Revisión de los elementos del Sprint Backlog

| ID | Elemento seleccionado | Estado | Story Points | Issue |
|---|---|---|---|---|
| US-101 | Instalación y onboarding | Pendiente | 2 | Por crear |
| US-102 | Contraseñas con hash | Pendiente | 2 | Por crear |
| US-103 | Configuración por entorno y zona horaria | Pendiente | 2 | Por crear |
| US-104 | Eliminación segura de registros | Pendiente | 3 | Por crear |
| US-105 | Diagrama ER actualizado | Pendiente | 1 | Por crear |

**Total de Story Points planificados:** 10

**Total de Story Points completados:** Por registrar

Nota: según la planificación (ACT-SP-001), si falta capacidad la primera historia en moverse al Product Backlog es US-105.

## 6. Incremento desarrollado

Funcionalidades previstas para el Incremento (versión v0.1.0).

| ID | Funcionalidad | Descripción | Evidencia |
|---|---|---|---|
| INC-001 | Instalación y onboarding | Entrega de US-101 según sus criterios de aceptación | Por registrar |
| INC-002 | Contraseñas con hash | Entrega de US-102 según sus criterios de aceptación | Por registrar |
| INC-003 | Configuración por entorno y zona horaria | Entrega de US-103 según sus criterios de aceptación | Por registrar |
| INC-004 | Eliminación segura de registros | Entrega de US-104 según sus criterios de aceptación | Por registrar |
| INC-005 | Diagrama ER actualizado | Entrega de US-105 según sus criterios de aceptación | Por registrar |
| INC-006 | Documentación | README y documentos de `Records/` actualizados | Por registrar |

## 7. Validación de criterios de aceptación

Los criterios completos están en la sección 7 de ACT-SP-001.

| ID | Criterio de aceptación | Resultado | Observaciones |
|---|---|---|---|
| CA-001 | US-101: El proyecto se instala y se ejecuta desde cero siguiendo únicamente el README. | Pendiente | Por registrar |
| CA-002 | US-101: Cada integrante logra iniciar sesión en su propio equipo. | Pendiente | Por registrar |
| CA-003 | US-101: Los bloqueos encontrados y su solución quedan documentados. | Pendiente | Por registrar |
| CA-004 | US-102: La contraseña del administrador se guarda como hash (`$2y$…`) y el inicio de sesión sigue funcionando. | Pendiente | Por registrar |
| CA-005 | US-102: `db_9eleven.sql` ya no contiene ninguna contraseña en texto plano. | Pendiente | Por registrar |
| CA-006 | US-102: `index.php` y `cambiarContrasena.php` solo aceptan contraseñas con hash. | Pendiente | Por registrar |
| CA-007 | US-102: Tras un inicio de sesión correcto se regenera el identificador de sesión. | Pendiente | Por registrar |
| CA-008 | US-103: Los datos de conexión se leen de variables de entorno o `.env`, con los valores de XAMPP como respaldo; `.env` está en `.gitignore` y existe `.env.example`. | Pendiente | Por registrar |
| CA-009 | US-103: Dashboard, Ventas y Reportes calculan «hoy» con la zona horaria `America/Bogota` y muestran el mismo día. | Pendiente | Por registrar |
| CA-010 | US-104: Eliminar productos, categorías y proveedores se hace por ID desde un botón en cada fila, con confirmación. | Pendiente | Por registrar |
| CA-011 | US-104: Intentar eliminar un producto con ventas muestra un mensaje claro y no un error técnico. | Pendiente | Por registrar |
| CA-012 | US-104: Nunca se elimina más de un registro por acción. | Pendiente | Por registrar |
| CA-013 | US-104: Al eliminar una categoría se avisa cuántos productos quedarán sin categoría. | Pendiente | Por registrar |
| CA-014 | US-105: El diagrama ER refleja las 6 tablas actuales y está en `Resources/`. | Pendiente | Por registrar |
| CA-015 | US-105: El README enlaza al diagrama actualizado. | Pendiente | Por registrar |
| CA-016 | General: El equipo demuestra: instalar desde cero, iniciar sesión con la contraseña con hash, y eliminar una categoría y un producto con ventas viendo mensajes claros. | Pendiente | Por registrar |

## 8. Pull Requests y evidencias técnicas

| Pull Request | Descripción | Estado | Revisor |
|---|---|---|---|
| Por registrar | US-101 | Pendiente | Por asignar |
| Por registrar | US-102 | Pendiente | Por asignar |
| Por registrar | US-103 | Pendiente | Por asignar |
| Por registrar | US-104 | Pendiente | Por asignar |
| Por registrar | US-105 | Pendiente | Por asignar |

**Otras evidencias:**

- Revisión de sintaxis: Por registrar (`php -l` sobre los archivos modificados).
- Pruebas manuales en XAMPP: Por registrar (casos exitosos y de error).
- Capturas de pantalla: Por registrar.
- Documentación técnica: README y `Records/` actualizados.
- Versión o demostración: Por registrar (v0.1.0).

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
| AC-003 | Publicar el release v0.1.0 en GitHub | Scrum Master | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Pull Requests: Por registrar
- Incremento presentado: Por registrar (v0.1.0)
- Documentación relacionada: ACT-SP-001 y `Requirements/`

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
