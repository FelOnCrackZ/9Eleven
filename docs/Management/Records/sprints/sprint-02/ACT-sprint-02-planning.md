# Acta de Planificación del Sprint 2

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SP-002 |
| Nombre del proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Número del Sprint | Sprint 2 |
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

Completar el ciclo de gestión (crear, consultar, editar y eliminar) de productos, categorías y proveedores, con validaciones consistentes y mensajes de error claros.

## 5. Elementos seleccionados del Product Backlog

Propuesta inicial construida a partir de `Management/product-backlog.md`. El equipo la valida, estima y ajusta durante la Sprint Planning. Las referencias «Backlog #N» corresponden a los issues descritos en ese documento.

| ID | Historia de usuario / Requerimiento | Prioridad | Story Points | Issue |
|---|---|---|---|---|
| US-201 | Como administrador, quiero editar productos para corregir precios, stock e información. | Alta | 3 | Por crear (Backlog #2) |
| US-202 | Como administrador, quiero editar categorías para corregir sus nombres. | Media | 2 | Por crear (Backlog #3) |
| US-203 | Como administrador, quiero editar proveedores para mantener su contacto al día. | Media | 2 | Por crear (Backlog #4) |
| US-204 | Como administrador, quiero formularios con validaciones y mensajes claros para evitar datos incorrectos. | Alta | 2 | Por crear (Backlog #11) |

**Total de Story Points seleccionados:** 9

## 6. Descomposición de actividades

Describir las actividades técnicas necesarias. La asignación de responsables la define el equipo junto con el Scrum Master durante el Sprint.

| ID | Actividad | Responsable | Issue relacionado | Estimación |
|---|---|---|---|---|
| TASK-201 | Vista `?vista=editar&id=…` en `productos.php` con formulario precargado, incluido `informacionGeneral` (US-201) | Por asignar (Developer) | Por crear | 4 h |
| TASK-202 | `UPDATE` con consulta preparada y control de código único; botón «Editar» en cada fila (US-201) | Por asignar (Developer) | Por crear | 3 h |
| TASK-203 | Pruebas manuales de productos: edición válida, código duplicado y valores negativos (US-201) | Por asignar (Developer) | Por crear | 2 h |
| TASK-204 | Edición de categorías: vista y `UPDATE` (US-202) | Por asignar (Developer) | Por crear | 3 h |
| TASK-205 | `UNIQUE` en `nombreCategoria` (con script de migración) y captura del error (US-202) | Por asignar (Developer) | Por crear | 2 h |
| TASK-206 | Edición de proveedores: vista, `UPDATE` y validación del teléfono (US-203) | Por asignar (Developer) | Por crear | 4 h |
| TASK-207 | Guardar contacto y teléfono vacíos como `NULL` (US-203) | Por asignar (Developer) | Por crear | 1 h |
| TASK-208 | Validaciones comunes: no vacíos ni solo espacios, números no negativos, distinguir error 1062 (duplicado) de 1452 (clave foránea) (US-204) | Por asignar (Developer) | Por crear | 3 h |
| TASK-209 | Avisar cuando `precioVenta` sea menor que `precioCompra` (US-204) | Por asignar (Developer) | Por crear | 1 h |
| TASK-210 | Usar un prefijo distinto para los IDs de proveedores (`PR001`) y de ventas (`V0001`) (US-204) | Por asignar (Developer) | Por crear | 1 h |
| TASK-211 | Pruebas manuales de categorías y proveedores (US-202, US-203) | Por asignar (Developer) | Por crear | 3 h |
| TASK-212 | Actualizar README y preparar la demostración | Por asignar (Developer) | Por crear | 2 h |

**Total de horas estimadas:** 29 h

## 7. Criterios de aceptación

Condiciones que deben cumplirse para considerar terminada cada historia. Cómo redactarlos: `Management/acceptance-criteria-and-dod.md`.

**US-201**

- [ ] Cada fila del listado tiene un botón «Editar» que abre un formulario precargado (incluye `informacionGeneral`).
- [ ] Al guardar, el producto se actualiza con consulta preparada y el cambio se ve en el listado, el dashboard y las alertas.
- [ ] No se permiten precios, IVA o stock negativos ni un código de producto repetido (mensaje claro).

**US-202**

- [ ] Se puede cambiar el nombre de una categoría y sus productos y proveedores conservan la relación.
- [ ] No se aceptan nombres vacíos ni duplicados.

**US-203**

- [ ] El formulario de edición está precargado (empresa, contacto, teléfono y categoría).
- [ ] El teléfono solo acepta dígitos y una longitud razonable.
- [ ] Contacto y teléfono vacíos se guardan como `NULL` y se muestran como «—».

**US-204**

- [ ] Todos los formularios validan en el servidor (no vacíos, números no negativos) aunque el navegador también valide.
- [ ] Los mensajes distinguen entre registro duplicado y clave foránea inválida.
- [ ] Se avisa cuando el precio de venta es menor que el de compra.
- [ ] Los IDs de proveedores usan un prefijo distinto al de ventas.

**Criterio general del Sprint**

- [ ] El equipo demuestra crear, editar y eliminar un producto, una categoría y un proveedor, incluyendo un caso de error en cada módulo.

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
| Cierre de pendientes del Sprint 1 (si los hay) | Día 1 | Día 2 | Equipo de desarrollo |
| US-201: Editar productos | Día 1 | Día 4 | Equipo de desarrollo |
| US-202: Editar categorías | Día 3 | Día 5 | Equipo de desarrollo |
| US-203: Editar proveedores | Día 4 | Día 6 | Equipo de desarrollo |
| Revisión de avance con el Product Owner | Día 4 | Día 4 | Scrum Master y Product Owner |
| US-204: Validaciones comunes | Día 5 | Día 7 | Equipo de desarrollo |
| Documentación y preparación de la demostración | Día 7 | Día 8 | Equipo de desarrollo |
| Sprint Review y Retrospectiva | Día 8 | Día 8 | Todo el equipo Scrum |

## 10. Riesgos, dependencias e impedimentos

| ID | Descripción | Impacto | Acción preventiva o correctiva | Responsable |
|---|---|---|---|---|
| RISK-201 | Pendientes del Sprint 1 sin cerrar reducen la capacidad de este Sprint. | Alto | Revisarlos al iniciar y cerrarlos primero; si ocupan más de un día de trabajo del equipo, el Product Owner decide qué historia se mueve. | Scrum Master |
| RISK-202 | Editar `stockActual` a mano puede dejar el inventario inconsistente con ventas y entradas. | Medio | El Product Owner define si el stock se puede editar o solo cambia con ventas y entradas (Sprint 3). | Product Owner |
| RISK-203 | Agregar `UNIQUE` a `nombreCategoria` falla si ya hay duplicados en la base. | Medio | Revisar los datos antes y entregar un script de migración. | Equipo de desarrollo |
| RISK-204 | Las validaciones quedan distintas en cada módulo. | Medio | Crear funciones comunes en `config.php` o en un archivo de ayuda y revisarlas en cada PR. | Equipo de desarrollo |
| DEP-201 | US-201 a US-203 reutilizan los botones por fila y el borrado por ID del Sprint 1 (US-104). | Medio | Confirmar su estado en la Sprint Review del Sprint 1. | Scrum Master |

## 11. Acuerdos y compromisos

| ID | Acuerdo o compromiso | Responsable | Fecha límite |
|---|---|---|---|
| AC-001 | Revisar el resultado del Sprint 1 al inicio de este Sprint y priorizar el cierre de sus pendientes. | Scrum Master | Por definir |
| AC-002 | Crear en el GitHub Project los issues de las historias y tareas del Sprint 2. | Scrum Master | Por definir |
| AC-003 | Reutilizar las funciones de validación comunes en todos los módulos. | Equipo de desarrollo | Por definir |
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

- El stock todavía no cambia automáticamente: las ventas y las entradas se implementan en el Sprint 3.
- La búsqueda y la paginación (Backlog #14) no forman parte de este Sprint.
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
