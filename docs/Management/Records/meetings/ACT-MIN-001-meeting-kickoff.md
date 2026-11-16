# ACT-MIN-001 — Acta de reunión de inicio y entrega del contexto del proyecto

> Acta preparada con la información del proyecto. Los campos `Por definir`, `Por confirmar` y `[ ]` se completan con la información real de la reunión.

## 1. Información general

| Campo | Descripción |
|---|---|
| Código del documento | ACT-MIN-001 |
| Nombre de la reunión | Reunión inicial — Entrega del contexto de 9Eleven |
| Proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Fecha de la reunión | Por definir (YYYY-MM-DD) |
| Hora de inicio | Por definir (HH:MM) |
| Hora de finalización | Por definir (HH:MM) |
| Modalidad | Por definir (Presencial / Virtual) |
| Responsables de la entrega | Equipo original de 9Eleven: Felipe Nuñez Navarro, Jorge Humberto Leyes Rojas y Manuel Alejandro Mera Ruiz |
| Tipo de reunión | Inicio del proyecto y transferencia de contexto |
| Repositorio del equipo (fork activo) | `https://github.com/PatinoMiguel-22/9Eleven` |
| Repositorio original (upstream / equipo fundador) | `https://github.com/FelOnCrackZ/9Eleven` |
| GitHub Project (tablero del equipo) | `https://github.com/users/PatinoMiguel-22/projects/1` |

## 2. Participantes

| Nombre completo | Rol | Usuario de GitHub | Asistencia |
|---|---|---|---|
| Felipe Nuñez Navarro | Product Owner y equipo original (entrega de contexto) | @FelOnCrackZ | Por confirmar |
| Jorge Humberto Leyes Rojas | Equipo original (entrega de contexto) | @DEAR3SMILE | Por confirmar |
| Manuel Alejandro Mera Ruiz | Equipo original (entrega de contexto) | @Aleec-18 | Por confirmar |
| Miguel Ángel Patiño Caicedo | Scrum Master | @PatinoMiguel-22 | Por confirmar |
| Miguel Angel Herrera Lujan | Developer | @Miguel-lujan2032 | Por confirmar |
| Ralay Montaño Hurtado | Developer | @raly-cpu | Por confirmar |
| Brahian Alonso Alzate Toro | Developer | @AlzateBrahian07 | Por confirmar |

## 3. Objetivo de la reunión

Presentar al equipo que continuará el proyecto el contexto general, el estado actual, la arquitectura, las funcionalidades existentes y los requerimientos pendientes de 9Eleven, para que pueda analizar la situación del proyecto, identificar el trabajo necesario y organizar su primer Sprint.

## 4. Agenda

1. Presentación del proyecto 9Eleven: problema, propósito y alcance.
2. Estado actual del repositorio, la arquitectura y las tecnologías.
3. Funcionalidades existentes y pendientes.
4. Documentación disponible (`Requirements/`, `Resources/`, `Management/`).
5. Forma de trabajo con Scrum y GitHub (fork activo y tablero de seguimiento).
6. Calendario de Sprints y siguiente reunión.
7. Dudas, acuerdos y compromisos.

## 5. Desarrollo de la reunión

### 5.1. Presentación y contexto del proyecto

9Eleven es una aplicación web de **gestión de inventario para un minimarket**. Nació de un levantamiento de información (observación, entrevistas y encuestas) que encontró tres problemas:

| # | Hallazgo |
|---|---|
| 1 (crítico) | No hay aviso de escasez: los productos se agotan antes de pedirlos al proveedor. |
| 2 | Los datos de proveedores (contactos y precios) están dispersos en facturas de papel. |
| 3 | No existen reportes consolidados con el valor del inventario. |

El sistema tiene **un único rol: Administrador**. Sus módulos son: inicio de sesión, dashboard, productos, categorías, proveedores, ventas, alertas de stock y reportes.

**Fuera de alcance:** múltiples roles, app móvil nativa, versión de escritorio, integración con puntos de venta externos y facturación electrónica.

**Preguntas y observaciones del equipo:** [Registrar durante la reunión]

### 5.2. Estado inicial del repositorio

Aplicación en **PHP nativo (sin framework)** que corre en **Apache + MariaDB (XAMPP)**, con acceso a datos mediante PDO y sesiones nativas de PHP. Cada módulo vive en un solo archivo `.php`; `config.php` se incluye en todas las páginas y ofrece la conexión y las funciones `requerirLogin()`, `h()` y `formatoPesos()`.

| Funciona hoy | Pendiente o incompleto |
|---|---|
| Inicio de sesión y cierre de sesión | Contraseñas en texto plano en la base de ejemplo |
| Cambio de contraseña (con hash) | Recuperación de contraseña por correo |
| Productos, categorías y proveedores: crear, consultar y eliminar | **Editar** productos, categorías y proveedores |
| Listado de ventas por fecha | **Registrar ventas** (y descontar stock) |
| Alertas de stock (dashboard y `alertaStock.php`) | Entradas de mercancía (no existe la tabla) |
| Reporte de productos más vendidos | Reportes de movimientos, stock bajo y valor del inventario |
| — | Eliminar un producto con ventas muestra un error técnico; protección CSRF; zona horaria |

El detalle de cada pendiente, con tareas y criterios, está en [`Management/product-backlog.md`](../../Management/product-backlog.md).

**Preguntas y observaciones del equipo:** [Registrar durante la reunión]

### 5.3. Documentación entregada

| Carpeta | Contenido |
|---|---|
| `Requirements/` | Documento funcional original: introducción, requerimientos, casos de uso e historias |
| `Resources/` | Diagramas y material técnico del semestre anterior |
| `Management/` | Lineamientos de Scrum, criterios de aceptación y flujo de GitHub |
| `Templates/` | Plantillas de actas |
| `Records/` | Actas de reuniones y de los 4 Sprints |

El diagrama ER del documento original está desactualizado frente al script SQL (ver `Resources/README.md`).

### 5.4. Forma de trabajo

El equipo se organiza con su Scrum Master; el Product Owner prioriza el backlog y valida los criterios de aceptación. Se trabaja sobre el fork del equipo (`PatinoMiguel-22/9Eleven`) con una rama por historia, Pull Request y revisión de otro integrante, y cada evento de Scrum deja un acta en `Records/`. Detalles en [`Management/scrum-guidelines.md`](../../Management/scrum-guidelines.md).

### 5.5. Hoja de ruta propuesta (referencial)

| Sprint | Fechas | Enfoque |
|---|---|---|
| Sprint 1 | Por definir | Base segura y reproducible (contraseñas con hash, configuración, eliminación segura) |
| Sprint 2 | Por definir | CRUD completo (editar) y validaciones |
| Sprint 3 | Por definir | Ventas y entradas con control de stock |
| Sprint 4 | Por definir | Reportes, seguridad y cierre (v1.0.0) |

## 6. Identificación inicial de áreas de trabajo

| Área | Necesidad identificada |
|---|---|
| Seguridad | Contraseñas con hash, CSRF, sesión y configuración por entorno |
| Productos, categorías y proveedores | Edición, validaciones y eliminación segura |
| Ventas | Registro con descuento de stock en una transacción |
| Entradas de mercancía | Nueva tabla y flujo que aumente el stock |
| Reportes y alertas | Completar los cuatro reportes y mejorar la página de alertas |

Esta identificación no representa una asignación definitiva de tareas ni una aprobación del alcance de ningún Sprint.

## 7. Acuerdos y decisiones

| ID | Acuerdo o decisión | Responsable | Fecha de cumplimiento |
|---|---|---|---|
| AC-001 | El fork del equipo (`PatinoMiguel-22/9Eleven`) será la fuente activa del desarrollo, issues y PRs; el repositorio original (`FelOnCrackZ/9Eleven`) queda como referencia upstream. | Todo el equipo | Por definir |
| AC-002 | El equipo analizará la base existente antes de implementar nuevas funcionalidades. | Equipo de desarrollo | Por definir |
| AC-003 | Se conserva el alcance actual (un único rol, inventario de minimarket); no se agregan funcionalidades fuera de alcance sin aprobación del Product Owner. | Product Owner | Por definir |
| AC-004 | Las tareas se registran como GitHub Issues en el fork y se organizan en el GitHub Project del equipo. | Scrum Master | Por definir |
| AC-005 | Los cambios de código se entregan mediante Pull Request revisado por otro integrante. | Equipo de desarrollo | Por definir |
| AC-006 | Los resultados de cada evento se documentan en `Records/`. | Scrum Master | Por definir |

## 8. Compromisos y tareas pendientes

| ID | Actividad | Responsable | Fecha límite | Estado |
|---|---|---|---|---|
| TASK-001 | Hacer fork / sincronizar el proyecto desde el repositorio original al repositorio del equipo y confirmar los usuarios de GitHub de todos los integrantes. | Equipo original y Scrum Master | Por definir | Completado |
| TASK-002 | Clonar el repositorio, instalar XAMPP, importar `db_9eleven.sql` y reportar bloqueos. | Developers | Por definir | Pendiente |
| TASK-003 | Leer `README.md`, `Requirements/`, `Resources/` y `Management/`. | Equipo de desarrollo | Por definir | Pendiente |
| TASK-004 | Crear el tablero y los issues del Sprint 1. | Scrum Master | Por definir | Pendiente |
| TASK-005 | Estimar el Sprint 1 y firmar el acta ACT-SP-001. | Equipo de desarrollo y Scrum Master | Por definir | Pendiente |

## 9. Riesgos, problemas e impedimentos

| ID | Descripción | Impacto | Acción propuesta | Responsable |
|---|---|---|---|---|
| RISK-001 | La base de ejemplo y el README original traen una contraseña de prueba en texto plano. | Alto | Resolverlo al inicio del Sprint 1 (US-102) y no reutilizar esa clave. | Equipo de desarrollo |
| RISK-002 | No existen pruebas automáticas; la verificación es manual. | Medio | Documentar la evidencia manual en cada PR; evaluar CI en el Sprint 4. | Scrum Master |
| RISK-003 | Equipo con poca experiencia en PHP puro, XAMPP y MariaDB. | Medio | Trabajo en parejas y README claro. | Scrum Master |
| RISK-004 | Los cambios de esquema (entradas de mercancía) pueden romper instalaciones existentes. | Medio | Entregar scripts de migración. | Equipo de desarrollo |

## 10. Resultado de la reunión

El equipo recibe el contexto funcional y técnico de 9Eleven y el repositorio que servirá de punto de partida. A partir de esta entrega, el equipo analiza el proyecto y organiza su trabajo; la selección definitiva del Sprint 1 se documenta en `ACT-SP-001`.

## 11. Evidencias y recursos

| Recurso | Ubicación |
|---|---|
| Repositorio del equipo (fork activo de desarrollo) | `https://github.com/PatinoMiguel-22/9Eleven` |
| Repositorio original (upstream / equipo fundador) | `https://github.com/FelOnCrackZ/9Eleven` |
| Tablero de seguimiento (GitHub Project) | `https://github.com/users/PatinoMiguel-22/projects/1` |
| Backlog del proyecto | `Management/product-backlog.md` |
| Documento funcional | `Requirements/` |
| Diagramas | `Resources/` |

## 12. Observaciones

Esta acta no corresponde a la planificación del Sprint 1 ni aprueba por sí misma las actividades que el equipo registre después en el tablero.

## 13. Aprobación y constancia

| Participante | Rol | Usuario de GitHub | Fecha de revisión |
|---|---|---|---|
| Felipe Nuñez Navarro | Product Owner y equipo original | @FelOnCrackZ | YYYY-MM-DD |
| Jorge Humberto Leyes Rojas | Equipo original | @DEAR3SMILE | YYYY-MM-DD |
| Manuel Alejandro Mera Ruiz | Equipo original | @Aleec-18 | YYYY-MM-DD |
| Miguel Ángel Patiño Caicedo | Scrum Master | @PatinoMiguel-22 | YYYY-MM-DD |

### Estado del acta

- [ ] Acta elaborada.
- [ ] Información y participantes verificados.
- [ ] Acuerdos y compromisos documentados.
- [ ] Acta revisada por los participantes.
- [ ] Acta aprobada.

**Evidencia de aprobación:** [URL del Pull Request o discusión correspondiente]

---

**Código del documento:** ACT-MIN-001 · **Proyecto:** 9Eleven · **Estado:** Preparada, pendiente de completar con los datos reales de la reunión.
