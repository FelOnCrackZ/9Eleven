# Acta de Revisión del Sprint 3

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SR-003 |
| Proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Sprint | Sprint 3 |
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

Esta acta se prepara al inicio del Sprint con los datos de la planificación (ACT-SP-003). Las columnas de estado, resultado y evidencia se completan durante la Sprint Review; hasta entonces permanecen como «Pendiente» o «Por registrar».

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

Registrar ventas y entradas de mercancía actualizando el stock automáticamente, para que el inventario refleje la operación real del minimarket.

**Resultado general:**

[Se completa en la Sprint Review: indicar si se alcanzó el objetivo.]

## 5. Revisión de los elementos del Sprint Backlog

| ID | Elemento seleccionado | Estado | Story Points | Issue |
|---|---|---|---|---|
| US-301 | Nueva venta con descuento de stock | Pendiente | 5 | Por crear |
| US-302 | Entradas de mercancía | Pendiente | 5 | Por crear |

**Total de Story Points planificados:** 10

**Total de Story Points completados:** Por registrar

Nota: según la planificación (ACT-SP-003), si falta capacidad la primera historia en moverse al Product Backlog es US-302.

## 6. Incremento desarrollado

Funcionalidades previstas para el Incremento (versión v0.3.0).

| ID | Funcionalidad | Descripción | Evidencia |
|---|---|---|---|
| INC-001 | Nueva venta con descuento de stock | Entrega de US-301 según sus criterios de aceptación | Por registrar |
| INC-002 | Entradas de mercancía | Entrega de US-302 según sus criterios de aceptación | Por registrar |
| INC-003 | Documentación | README y documentos de `Records/` actualizados | Por registrar |

## 7. Validación de criterios de aceptación

Los criterios completos están en la sección 7 de ACT-SP-003.

| ID | Criterio de aceptación | Resultado | Observaciones |
|---|---|---|---|
| CA-001 | US-301: Existe «Nueva venta»: permite agregar varios productos con cantidades y calcula subtotales y total (con IVA). | Pendiente | Por registrar |
| CA-002 | US-301: Al guardar se crean `ventas` y `detalle_ventas` y se descuenta `stockActual`, todo en una transacción. | Pendiente | Por registrar |
| CA-003 | US-301: No se puede vender más unidades de las que hay en stock. | Pendiente | Por registrar |
| CA-004 | US-301: Si algo falla a mitad del proceso no queda una venta sin detalle ni stock descontado a medias. | Pendiente | Por registrar |
| CA-005 | US-301: La venta queda registrada con el administrador de la sesión y el precio unitario del momento. | Pendiente | Por registrar |
| CA-006 | US-302: Existen las tablas `entradas` y `detalle_entradas`, incluidas en `db_9eleven.sql`. | Pendiente | Por registrar |
| CA-007 | US-302: Una entrada guardada (proveedor, fecha, productos, cantidades y precio unitario) aumenta el stock, en una transacción. | Pendiente | Por registrar |
| CA-008 | US-302: Cada proveedor tiene un historial de sus entradas. | Pendiente | Por registrar |
| CA-009 | US-302: «Movimientos recientes» del dashboard muestra entradas y ventas. | Pendiente | Por registrar |
| CA-010 | General: El equipo demuestra: registrar una entrada y ver subir el stock, registrar una venta y verlo bajar, y ver aparecer la alerta cuando baja del mínimo. | Pendiente | Por registrar |

## 8. Pull Requests y evidencias técnicas

| Pull Request | Descripción | Estado | Revisor |
|---|---|---|---|
| Por registrar | US-301 | Pendiente | Por asignar |
| Por registrar | US-302 | Pendiente | Por asignar |

**Otras evidencias:**

- Revisión de sintaxis: Por registrar (`php -l` sobre los archivos modificados).
- Pruebas manuales en XAMPP: Por registrar (casos exitosos y de error).
- Capturas de pantalla: Por registrar.
- Documentación técnica: README y `Records/` actualizados.
- Versión o demostración: Por registrar (v0.3.0).

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
| AC-003 | Publicar el release v0.3.0 en GitHub | Scrum Master | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Pull Requests: Por registrar
- Incremento presentado: Por registrar (v0.3.0)
- Documentación relacionada: ACT-SP-003 y `Requirements/`

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
