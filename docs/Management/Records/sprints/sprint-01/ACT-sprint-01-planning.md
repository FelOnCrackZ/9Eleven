# Acta de Planificación del Sprint 1

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SP-001 |
| Nombre del proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Número del Sprint | Sprint 1 |
| Fecha de planificación | 2026-11-03 |
| Hora de inicio | Por definir (HH:MM) |
| Hora de finalización | Por definir (HH:MM) |
| Duración del Sprint | 2 semanas (2026-11-03 al 2026-11-16) |
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

Dejar una base de trabajo segura y reproducible: que cualquier integrante pueda instalar 9Eleven desde cero, que las contraseñas se guarden con hash, que la configuración y la zona horaria sean correctas y que eliminar registros no rompa la aplicación.

## 5. Elementos seleccionados del Product Backlog

Propuesta inicial construida a partir de `Management/product-backlog.md`. El equipo la valida, estima y ajusta durante la Sprint Planning. Las referencias «Backlog #N» corresponden a los issues descritos en ese documento.

| ID | Historia de usuario / Requerimiento | Prioridad | Story Points | Issue |
|---|---|---|---|---|
| US-101 | Como equipo, queremos instalar y entender el proyecto (XAMPP, base de datos, estructura del código) para trabajar sin bloqueos. | Alta | 2 | Por crear |
| US-102 | Como administrador, quiero que mi contraseña se guarde con hash y que el SQL no traiga claves en texto plano, para proteger el acceso al sistema. | Alta | 2 | Por crear (Backlog #1) |
| US-103 | Como equipo, queremos configuración por entorno y zona horaria de Colombia, para no editar `config.php` en cada equipo y no tener fechas incorrectas. | Alta | 2 | Por crear (Backlog #17 y #18) |
| US-104 | Como administrador, quiero eliminar productos, categorías y proveedores sin errores técnicos ni borrados accidentales. | Alta | 3 | Por crear (Backlog #12) |
| US-105 | Como equipo, queremos el diagrama ER actualizado a las 6 tablas reales, para que la documentación coincida con el código. | Media | 1 | Por crear (Backlog #13) |

**Total de Story Points seleccionados:** 10

## 6. Descomposición de actividades

Describir las actividades técnicas necesarias. La asignación de responsables la define el equipo junto con el Scrum Master durante el Sprint.

| ID | Actividad | Responsable | Issue relacionado | Estimación |
|---|---|---|---|---|
| TASK-101 | Instalar XAMPP, clonar el repositorio, importar `db_9eleven.sql` e iniciar sesión (US-101) | Por asignar (Developer) | Por crear | 2 h |
| TASK-102 | Leer `README.md`, `Management/` y `Requirements/`; anotar dudas (US-101) | Por asignar (Developer) | Por crear | 2 h |
| TASK-103 | Recorrido guiado por `config.php`, `index.php`, `productos.php` e `includes/` (US-101) | Por asignar (Developer) | Por crear | 2 h |
| TASK-104 | Documentar en el README los bloqueos encontrados y su solución (US-101) | Por asignar (Developer) | Por crear | 1 h |
| TASK-105 | Convertir la contraseña del administrador a hash y reemplazar la clave del SQL por un hash o por un script `crear_admin.php` (US-102) | Por asignar (Developer) | Por crear | 3 h |
| TASK-106 | Quitar la rama de texto plano de `index.php` y `cambiarContrasena.php`; llamar `session_regenerate_id(true)` tras el login (US-102) | Por asignar (Developer) | Por crear | 2 h |
| TASK-107 | Probar el login: correcto, incorrecto y cambio de contraseña con hash (US-102) | Por asignar (Developer) | Por crear | 2 h |
| TASK-108 | Leer `DB_*` desde variables de entorno o `.env` con respaldo de XAMPP; crear `.env.example` y `.gitignore` (US-103) | Por asignar (Developer) | Por crear | 3 h |
| TASK-109 | Fijar `America/Bogota` en PHP y en la conexión PDO; usar una sola fuente para «hoy» (US-103) | Por asignar (Developer) | Por crear | 2 h |
| TASK-110 | Probar Dashboard, Ventas y Reportes pasadas las 7 p. m. (US-103) | Por asignar (Developer) | Por crear | 1 h |
| TASK-111 | Eliminar productos por ID con botón por fila y confirmación (US-104) | Por asignar (Developer) | Por crear | 3 h |
| TASK-112 | Capturar la excepción al borrar un producto con ventas y mostrar un mensaje claro (US-104) | Por asignar (Developer) | Por crear | 2 h |
| TASK-113 | Aplicar el borrado por ID a categorías y proveedores; avisar cuántos productos quedan sin categoría (US-104) | Por asignar (Developer) | Por crear | 4 h |
| TASK-114 | Pruebas manuales de eliminación en los tres módulos (US-104) | Por asignar (Developer) | Por crear | 2 h |
| TASK-115 | Redibujar el ER con las 6 tablas y guardarlo en `Resources/` (US-105) | Por asignar (Developer) | Por crear | 2 h |
| TASK-116 | Actualizar el README y preparar la demostración | Por asignar (Developer) | Por crear | 2 h |

**Total de horas estimadas:** 35 h

## 7. Criterios de aceptación

Condiciones que deben cumplirse para considerar terminada cada historia. Cómo redactarlos: `Management/acceptance-criteria-and-dod.md`.

**US-101**

- [ ] El proyecto se instala y se ejecuta desde cero siguiendo únicamente el README.
- [ ] Cada integrante logra iniciar sesión en su propio equipo.
- [ ] Los bloqueos encontrados y su solución quedan documentados.

**US-102**

- [ ] La contraseña del administrador se guarda como hash (`$2y$…`) y el inicio de sesión sigue funcionando.
- [ ] `db_9eleven.sql` ya no contiene ninguna contraseña en texto plano.
- [ ] `index.php` y `cambiarContrasena.php` solo aceptan contraseñas con hash.
- [ ] Tras un inicio de sesión correcto se regenera el identificador de sesión.

**US-103**

- [ ] Los datos de conexión se leen de variables de entorno o `.env`, con los valores de XAMPP como respaldo; `.env` está en `.gitignore` y existe `.env.example`.
- [ ] Dashboard, Ventas y Reportes calculan «hoy» con la zona horaria `America/Bogota` y muestran el mismo día.

**US-104**

- [ ] Eliminar productos, categorías y proveedores se hace por ID desde un botón en cada fila, con confirmación.
- [ ] Intentar eliminar un producto con ventas muestra un mensaje claro y no un error técnico.
- [ ] Nunca se elimina más de un registro por acción.
- [ ] Al eliminar una categoría se avisa cuántos productos quedarán sin categoría.

**US-105**

- [ ] El diagrama ER refleja las 6 tablas actuales y está en `Resources/`.
- [ ] El README enlaza al diagrama actualizado.

**Criterio general del Sprint**

- [ ] El equipo demuestra: instalar desde cero, iniciar sesión con la contraseña con hash, y eliminar una categoría y un producto con ventas viendo mensajes claros.

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
| US-101: Instalación y onboarding | Día 1 | Día 2 | Equipo de desarrollo |
| US-102: Contraseñas con hash | Día 2 | Día 5 | Equipo de desarrollo |
| US-103: Configuración por entorno y zona horaria | Día 3 | Día 6 | Equipo de desarrollo |
| Revisión de avance con el Product Owner | Día 7 | Día 7 | Scrum Master y Product Owner |
| US-104: Eliminación segura | Día 5 | Día 10 | Equipo de desarrollo |
| US-105: Diagrama ER actualizado | Día 8 | Día 9 | Equipo de desarrollo |
| Documentación y preparación de la demostración | Día 11 | Día 13 | Equipo de desarrollo |
| Sprint Review y Retrospectiva | Día 14 | Día 14 | Todo el equipo Scrum |

## 10. Riesgos, dependencias e impedimentos

| ID | Descripción | Impacto | Acción preventiva o correctiva | Responsable |
|---|---|---|---|---|
| RISK-101 | El equipo es nuevo en PHP, XAMPP y MariaDB. | Medio | Trabajo en parejas en US-101 y README claro. | Scrum Master |
| RISK-102 | Pasar a contraseñas con hash puede dejar al administrador sin acceso. | Alto | Respaldar la base antes, probar el login con hash y solo entonces quitar la rama de texto plano. | Equipo de desarrollo |
| RISK-103 | El borrado por ID cambia los formularios de tres módulos y puede generar conflictos entre ramas. | Medio | Una rama por historia y Pull Requests pequeños. | Equipo de desarrollo |
| DEP-101 | US-103 (zona horaria) debe quedar antes del Sprint 3, donde se registran ventas con fecha. | Medio | Priorizarla en la primera semana. | Scrum Master |

## 11. Acuerdos y compromisos

| ID | Acuerdo o compromiso | Responsable | Fecha límite |
|---|---|---|---|
| AC-001 | Trabajar con una rama por historia (`feature/US-10X-nombre`) creada desde `main`, con Pull Request revisado por otro integrante. | Scrum Master | Por definir |
| AC-002 | Crear en el GitHub Project los issues de las historias y tareas, con su ID y sus Story Points. | Scrum Master | Por definir |
| AC-003 | No reutilizar en ningún otro servicio la contraseña de prueba del SQL. | Todo el equipo | Por definir |
| AC-004 | Realizar una revisión de avance con el Product Owner a mitad del Sprint. | Scrum Master | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Product Backlog: `Management/product-backlog.md` y el tablero del equipo
- Issues seleccionados: pendientes de crear
- Documentación relacionada: `Requirements/`, `Resources/`, `Management/`, `README.md`
- Grabación de la reunión (si aplica): Por definir

## 13. Observaciones

- Esta planificación es una propuesta inicial construida a partir de `Management/product-backlog.md`; el equipo la valida, estima y ajusta en la reunión de Sprint Planning.
- Punto de partida del código (verificado): inicio de sesión, cambio de contraseña, crear/consultar/eliminar en productos, categorías y proveedores, listado de ventas, alertas de stock y un reporte. Faltan: editar registros, registrar ventas, entradas de mercancía y los otros tres reportes.
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
