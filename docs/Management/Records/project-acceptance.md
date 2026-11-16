# Acta de Aceptación y Cierre del Proyecto

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-PA-001 |
| Nombre del proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Fecha de evaluación | Por definir (YYYY-MM-DD) |
| Fecha de cierre | Por definir (YYYY-MM-DD) |
| Product Owner | Felipe Nuñez Navarro |
| Scrum Master | Miguel Ángel Patiño Caicedo |
| Equipo de desarrollo | Miguel Angel Herrera Lujan, Ralay Montaño Hurtado y Brahian Alonso Alzate Toro |
| Repositorio del equipo (fork activo) | `https://github.com/PatinoMiguel-22/9Eleven` |
| Repositorio original (upstream / equipo fundador) | `https://github.com/FelOnCrackZ/9Eleven` |
| GitHub Project (tablero del equipo) | `https://github.com/users/PatinoMiguel-22/projects/1` |
| Versión entregada | v1.0.0 (prevista) |

## 2. Objetivo del documento

Registrar la evaluación final de los entregables, verificar el cumplimiento de los requerimientos y documentar la aceptación formal de la solución por parte del Product Owner.

Esta acta se prepara al inicio del proyecto con los criterios de aceptación acordados. Las columnas de estado, resultado y evidencia se completan en la evaluación final; hasta entonces permanecen como «Pendiente» o «Por registrar».

## 3. Descripción general del proyecto

**Descripción:** 9Eleven es una aplicación web para gestionar el inventario de un minimarket: productos, categorías, proveedores, ventas, alertas de stock y reportes. Está desarrollada en PHP nativo con MariaDB/MySQL, sobre Apache (XAMPP), con acceso a datos por PDO y un único rol de Administrador.

**Objetivo general:** automatizar el control de inventario del minimarket, ordenar la relación con proveedores y entregar reportes útiles para decisiones de gerencia.

## 4. Alcance del proyecto

- Inicio de sesión, cierre de sesión y cambio y recuperación de contraseña.
- Gestión completa (crear, consultar, editar, eliminar) de productos, categorías y proveedores.
- Registro de ventas con descuento automático de stock.
- Registro de entradas de mercancía con aumento automático de stock.
- Alertas de stock bajo y cuatro reportes (movimientos, más vendidos, stock bajo y valor del inventario).
- Seguridad básica: contraseñas con hash, consultas preparadas, protección CSRF y sesión segura.

**Limitaciones conocidas (fuera del alcance acordado, salvo aprobación expresa del Product Owner):** múltiples roles, app móvil nativa, versión de escritorio, integración con puntos de venta externos, facturación electrónica, paginación y buscador, Docker y pruebas automáticas (metas opcionales). Esta sección se actualiza en la evaluación final con las limitaciones reales.

## 5. Evaluación de requerimientos

**Criterio mínimo de aceptación:** el proyecto puede aceptarse cuando todos los requerimientos **Obligatorios** están cumplidos y el equipo ejecuta sin fallos, ante el Product Owner y sobre una instalación limpia, el **escenario manual de nueve pasos**:

1. Iniciar sesión como administrador.
2. Crear una categoría, un proveedor y un producto.
3. Editar el producto (precio y stock mínimo).
4. Registrar una entrada de mercancía y comprobar que el stock aumenta.
5. Registrar una venta con dos productos y comprobar que el stock baja y que el total es correcto.
6. Llevar un producto por debajo de su stock mínimo y verlo en el dashboard y en la página de alertas.
7. Consultar los cuatro reportes.
8. Intentar eliminar un producto con ventas y ver un mensaje claro, sin errores técnicos.
9. Cambiar la contraseña y cerrar sesión, comprobando que las páginas protegidas exigen iniciar sesión.

**Criterio de carga:** el alcance obligatorio se dimensionó para unos 10 Story Points por Sprint de 2 semanas. Los requerimientos Deseables no condicionan la aceptación.

| ID | Requerimiento | Estado | Evidencia |
|---|---|---|---|
| REQ-F-001 | Inicio y cierre de sesión y cambio de contraseña, con contraseñas guardadas con hash. Obligatorio. Sprint 1. | Pendiente | Por registrar |
| REQ-F-002 | Gestión completa de productos (crear, consultar, editar, eliminar sin errores técnicos). Obligatorio. Sprints 1 y 2. | Pendiente | Por registrar |
| REQ-F-003 | Gestión completa de categorías. Obligatorio. Sprints 1 y 2. | Pendiente | Por registrar |
| REQ-F-004 | Gestión completa de proveedores. Obligatorio. Sprints 1 y 2. | Pendiente | Por registrar |
| REQ-F-005 | Registro de ventas con varios productos y descuento de stock en una transacción. Obligatorio. Sprint 3. | Pendiente | Por registrar |
| REQ-F-006 | Entradas de mercancía con aumento de stock (RF-12). Obligatorio. Sprint 3. | Pendiente | Por registrar |
| REQ-F-007 | Alertas de stock bajo con página completa (RF-15). Obligatorio. Sprint 4. | Pendiente | Por registrar |
| REQ-F-008 | Los cuatro reportes del documento funcional (RF-14). Obligatorio. Sprint 4. | Pendiente | Por registrar |
| REQ-F-009 | Recuperación de contraseña olvidada mediante enlace (RF-03). Deseable. Sprint 4. | Pendiente | Por registrar |
| REQ-F-010 | Paginación y buscador en los listados. Deseable (meta opcional). | Pendiente | Por registrar |
| REQ-NF-001 | Seguridad: consultas preparadas, salida escapada, protección CSRF, sesión segura y errores genéricos. Obligatorio. Sprints 1 y 4. | Pendiente | Por registrar |
| REQ-NF-002 | Configuración por entorno y zona horaria de Colombia. Obligatorio. Sprint 1. | Pendiente | Por registrar |
| REQ-NF-003 | Verificación: `php -l` sin errores y pruebas manuales documentadas (caso exitoso y de error) en cada PR. Obligatorio. Sprints 1 a 4. | Pendiente | Por registrar |
| REQ-NF-004 | Entorno reproducible y documentación actualizada (README, diagramas, actas). Obligatorio. Sprints 1 y 4. | Pendiente | Por registrar |

## 6. Entregables finales

| ID | Entregable | Descripción | Evidencia |
|---|---|---|---|
| DEL-001 | Código fuente | Código en la rama `main`, con la etiqueta v1.0.0 | `https://github.com/PatinoMiguel-22/9Eleven` |
| DEL-002 | Base de datos | `db_9eleven.sql` actualizado, con scripts de migración | Por registrar |
| DEL-003 | Documentación técnica | README, diagramas de `Resources/` y `Requirements/` actualizados al estado real | Por registrar |
| DEL-004 | Aplicación funcional | Versión v1.0.0, demostrada con el escenario manual de 9 pasos en la Sprint Review del Sprint 4 | Por registrar |
| DEL-005 | Actas del proyecto | Actas de reunión, de cada Sprint y de aceptación y cierre | `Records/` |

## 7. Evaluación de calidad y validación

| Aspecto evaluado | Resultado | Observaciones |
|---|---|---|
| Cumplimiento de requerimientos | Pendiente | Criterio de aprobación: todos los obligatorios en estado Cumplido. Los deseables pueden quedar Parcial o No cumplido. |
| Funcionamiento de las funcionalidades principales | Pendiente | Criterio de aprobación: el escenario manual de 9 pasos se ejecuta sin fallos, ante el Product Owner, sobre una instalación limpia. |
| Pruebas | Pendiente | Criterio de aprobación: cada historia tiene evidencia de un caso exitoso y uno de error en su Pull Request; `php -l` sin errores. |
| Calidad del código | Pendiente | Criterio de aprobación: sin credenciales versionadas; una rama por historia con PR revisado por otro integrante; `requerirLogin()`, consultas preparadas y `h()` en todas las páginas. |
| Documentación técnica | Pendiente | Criterio de aprobación: el README refleja el estado real y otra persona logra instalar el proyecto desde cero siguiéndolo. |
| Integración de los componentes | Pendiente | Criterio de aprobación: la aplicación arranca con la base de ejemplo importada y los flujos funcionan de punta a punta sobre `main` sin conflictos pendientes. |

## 8. Historial de entregas

| Versión | Descripción | Fecha | Referencia |
|---|---|---|---|
| v0.1.0 | Base segura y reproducible: contraseñas con hash, configuración por entorno, eliminación segura (Sprint 1) | Por definir | Por registrar |
| v0.2.0 | CRUD completo y validaciones (Sprint 2) | Por definir | Por registrar |
| v0.3.0 | Ventas y entradas con control de stock (Sprint 3) | Por definir | Por registrar |
| v1.0.0 | Reportes, seguridad y cierre (Sprint 4) | Por definir | Por registrar |

## 9. Requerimientos pendientes y limitaciones

| ID | Descripción | Justificación | Estado |
|---|---|---|---|
| PEND-001 | Paginación y buscador en los listados. | Meta opcional: solo si el equipo termina antes el compromiso del Sprint 4. | Opcional |
| PEND-002 | Docker y pruebas automáticas / integración continua. | Meta opcional de mejora operativa. | Opcional |
| PEND-003 | Múltiples roles, app móvil, versión de escritorio, integración con POS y facturación electrónica. | Fuera del alcance acordado. | Pendiente |

Se actualiza en la evaluación final con los pendientes reales. Estos elementos deben quedar documentados para evitar que se interpreten como funcionalidades entregadas.

## 10. Observaciones del Product Owner

**Aspectos satisfactorios:**

[Se completa en la evaluación final.]

**Observaciones generales:**

[Se completa en la evaluación final.]

**Recomendaciones futuras:**

[Se completa en la evaluación final.]

## 11. Declaración de aceptación

Mediante esta acta se deja constancia de que el Product Owner revisó los entregables, evaluó el cumplimiento de los requerimientos y registró sus observaciones.

**Estado de aceptación:**

- [ ] Proyecto aceptado.
- [ ] Proyecto aceptado con observaciones menores.
- [ ] Proyecto no aceptado; requiere correcciones.

**Criterio de decisión acordado:**

- **Aceptado:** todos los requerimientos obligatorios están cumplidos y todos los aspectos de la sección 7 están aprobados.
- **Aceptado con observaciones menores:** el escenario manual se ejecuta sin fallos y los obligatorios están cumplidos, pero quedan observaciones que no lo impiden (por ejemplo, documentación parcial).
- **No aceptado:** el escenario manual falla o no se cumple alguno de los requerimientos obligatorios principales (REQ-F-001 a REQ-F-006).

**Justificación de la decisión:**

[Se completa en la evaluación final.]

## 12. Acuerdos de cierre

| ID | Acuerdo | Responsable | Fecha límite |
|---|---|---|---|
| AC-001 | Congelar el código antes de la Review final: después solo se corrigen errores y se prepara la demostración. | Scrum Master | Por definir |
| AC-002 | Realizar la demostración del escenario manual ante el Product Owner y registrar la decisión de aceptación. | Product Owner | Por definir |
| AC-003 | Publicar el release v1.0.0 en GitHub con los entregables finales. | Scrum Master | Por definir |
| AC-004 | Registrar como issues los pendientes y las mejoras futuras para que no se interpreten como funcionalidades entregadas. | Scrum Master | Por definir |

## 13. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / equipo fundador): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Documentación final: `README.md`, `Requirements/` y `Resources/`
- Release final: Por registrar (v1.0.0)
- Pull Requests principales: Por registrar
- Actas anteriores: ACT-MIN-001 y las actas de planificación, revisión y retrospectiva de los Sprints 1 a 4

## 14. Aprobación y cierre

| Participante | Rol | Usuario de GitHub | Fecha |
|---|---|---|---|
| Felipe Nuñez Navarro | Product Owner | @FelOnCrackZ | YYYY-MM-DD |
| Miguel Ángel Patiño Caicedo | Scrum Master | @PatinoMiguel-22 | YYYY-MM-DD |
| Miguel Angel Herrera Lujan | Developer | @Miguel-lujan2032 | YYYY-MM-DD |
| Ralay Montaño Hurtado | Developer | @raly-cpu | YYYY-MM-DD |
| Brahian Alonso Alzate Toro | Developer | @AlzateBrahian07 | YYYY-MM-DD |

### Estado final del proyecto

- [ ] Requerimientos evaluados.
- [ ] Entregables revisados.
- [ ] Verificación completada.
- [ ] Documentación final entregada.
- [ ] Pendientes identificados.
- [ ] Decisión de aceptación registrada.
- [ ] Acta de cierre aprobada.

**Evidencia de aprobación:** [URL del Pull Request o discusión correspondiente]

---

**Fin del documento**

*Esta acta constituye el registro documental de la evaluación final y aceptación del proyecto. La aceptación debe corresponder a los entregables realmente verificados y no implica que las funcionalidades pendientes se consideren completadas.*
