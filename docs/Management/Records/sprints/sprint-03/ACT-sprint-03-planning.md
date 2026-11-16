# Acta de Planificación del Sprint 3

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SP-003 |
| Nombre del proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Número del Sprint | Sprint 3 |
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

Registrar ventas y entradas de mercancía actualizando el stock automáticamente, para que el inventario refleje la operación real del minimarket.

## 5. Elementos seleccionados del Product Backlog

Propuesta inicial construida a partir de `Management/product-backlog.md`. El equipo la valida, estima y ajusta durante la Sprint Planning. Las referencias «Backlog #N» corresponden a los issues descritos en ese documento.

| ID | Historia de usuario / Requerimiento | Prioridad | Story Points | Issue |
|---|---|---|---|---|
| US-301 | Como administrador, quiero registrar una venta con varios productos y que el stock se descuente automáticamente. | Alta | 5 | Por crear (Backlog #6) |
| US-302 | Como administrador, quiero registrar las entradas de mercancía de un proveedor y que el stock aumente automáticamente. | Alta | 5 | Por crear (Backlog #5) |

**Total de Story Points seleccionados:** 10

## 6. Descomposición de actividades

Describir las actividades técnicas necesarias. La asignación de responsables la define el equipo junto con el Scrum Master durante el Sprint.

| ID | Actividad | Responsable | Issue relacionado | Estimación |
|---|---|---|---|---|
| TASK-301 | Diseñar el flujo de «Nueva venta» (boceto) y definir el cálculo del IVA (US-301) | Por asignar (Developer) | Por crear | 2 h |
| TASK-302 | Formulario de nueva venta con varios productos y cantidades (US-301) | Por asignar (Developer) | Por crear | 5 h |
| TASK-303 | Guardar en `ventas` y `detalle_ventas` y restar `stockActual` dentro de una transacción (US-301) | Por asignar (Developer) | Por crear | 5 h |
| TASK-304 | Validar stock suficiente con `SELECT … FOR UPDATE` y guardar el `admin_id` de la sesión y el precio unitario del momento (US-301) | Por asignar (Developer) | Por crear | 3 h |
| TASK-305 | Pruebas manuales de ventas: éxito, stock insuficiente y fallo a mitad del proceso (US-301) | Por asignar (Developer) | Por crear | 3 h |
| TASK-306 | Agregar las tablas `entradas` y `detalle_entradas` a `db_9eleven.sql` y crear el script de migración (US-302) | Por asignar (Developer) | Por crear | 3 h |
| TASK-307 | Pantalla «Nueva entrada» dentro del módulo Proveedores (US-302) | Por asignar (Developer) | Por crear | 5 h |
| TASK-308 | Guardar la entrada y sumar el stock en una transacción (US-302) | Por asignar (Developer) | Por crear | 4 h |
| TASK-309 | Historial de entradas por proveedor (US-302) | Por asignar (Developer) | Por crear | 3 h |
| TASK-310 | Mostrar entradas y ventas en «Movimientos recientes» del dashboard (US-302) | Por asignar (Developer) | Por crear | 2 h |
| TASK-311 | Actualizar el ER, el README y preparar la demostración | Por asignar (Developer) | Por crear | 3 h |

**Total de horas estimadas:** 38 h

## 7. Criterios de aceptación

Condiciones que deben cumplirse para considerar terminada cada historia. Cómo redactarlos: `Management/acceptance-criteria-and-dod.md`.

**US-301**

- [ ] Existe «Nueva venta»: permite agregar varios productos con cantidades y calcula subtotales y total (con IVA).
- [ ] Al guardar se crean `ventas` y `detalle_ventas` y se descuenta `stockActual`, todo en una transacción.
- [ ] No se puede vender más unidades de las que hay en stock.
- [ ] Si algo falla a mitad del proceso no queda una venta sin detalle ni stock descontado a medias.
- [ ] La venta queda registrada con el administrador de la sesión y el precio unitario del momento.

**US-302**

- [ ] Existen las tablas `entradas` y `detalle_entradas`, incluidas en `db_9eleven.sql`.
- [ ] Una entrada guardada (proveedor, fecha, productos, cantidades y precio unitario) aumenta el stock, en una transacción.
- [ ] Cada proveedor tiene un historial de sus entradas.
- [ ] «Movimientos recientes» del dashboard muestra entradas y ventas.

**Criterio general del Sprint**

- [ ] El equipo demuestra: registrar una entrada y ver subir el stock, registrar una venta y verlo bajar, y ver aparecer la alerta cuando baja del mínimo.

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
| Cierre de pendientes del Sprint 2 (si los hay) | Día 1 | Día 2 | Equipo de desarrollo |
| US-301: Nueva venta con descuento de stock | Día 1 | Día 6 | Equipo de desarrollo |
| US-302: Entradas de mercancía | Día 3 | Día 9 | Equipo de desarrollo |
| Revisión de avance con el Product Owner | Día 5 | Día 5 | Scrum Master y Product Owner |
| Pruebas de integración manual y ajustes | Día 9 | Día 11 | Equipo de desarrollo |
| Documentación y preparación de la demostración | Día 11 | Día 13 | Equipo de desarrollo |
| Sprint Review y Retrospectiva | Día 14 | Día 14 | Todo el equipo Scrum |

## 10. Riesgos, dependencias e impedimentos

| ID | Descripción | Impacto | Acción preventiva o correctiva | Responsable |
|---|---|---|---|---|
| RISK-301 | Una transacción mal implementada deja datos inconsistentes (ventas sin detalle, stock incorrecto). | Alto | Usar `beginTransaction`, `commit` y `rollBack`; probar con fallos provocados; revisión cruzada del PR. | Equipo de desarrollo |
| RISK-302 | Dos ventas simultáneas sobre el mismo producto pueden vender más stock del que hay. | Medio | Usar `SELECT … FOR UPDATE` dentro de la transacción y probarlo con dos pestañas. | Equipo de desarrollo |
| RISK-303 | El cambio de esquema (tablas de entradas) rompe instalaciones existentes. | Medio | Entregar un script de migración y actualizar `db_9eleven.sql` y el ER. | Equipo de desarrollo |
| RISK-304 | Las dos historias suman 10 SP y son las de mayor complejidad del proyecto. | Alto | Si falta capacidad, el Product Owner decide mover US-302 al Sprint 4. | Product Owner |
| DEP-301 | US-301 depende de la zona horaria correcta (US-103) y de la eliminación segura (US-104). | Medio | Confirmar su estado en la Sprint Review del Sprint 1. | Scrum Master |

## 11. Acuerdos y compromisos

| ID | Acuerdo o compromiso | Responsable | Fecha límite |
|---|---|---|---|
| AC-001 | Revisar el resultado del Sprint 2 al inicio de este Sprint y priorizar el cierre de sus pendientes. | Scrum Master | Por definir |
| AC-002 | Crear en el GitHub Project los issues de las historias y tareas del Sprint 3. | Scrum Master | Por definir |
| AC-003 | Todo cambio de esquema debe incluir script de migración y actualizar `db_9eleven.sql`. | Equipo de desarrollo | Por definir |
| AC-004 | Probar cada flujo con dos pestañas del navegador para verificar el comportamiento ante ventas simultáneas. | Equipo de desarrollo | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Product Backlog: `Management/product-backlog.md` y el tablero del equipo
- Issues seleccionados: pendientes de crear
- Documentación relacionada: `Requirements/`, `Resources/`, `Management/`, `README.md`
- Grabación de la reunión (si aplica): Por definir

## 13. Observaciones

- La regla de si `stockActual` puede editarse manualmente (RISK-202 del Sprint 2) debe estar decidida antes de iniciar este Sprint.
- Los reportes que dependen de entradas (movimientos de inventario) se completan en el Sprint 4.
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
