# Acta de Revisión del Sprint 2

## 1. Información general

| Campo | Información |
|---|---|
| Código del documento | ACT-SR-002 |
| Proyecto | 9Eleven — Sistema de Gestión de Inventario para Minimarket |
| Sprint | Sprint 2 |
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

Esta acta se prepara al inicio del Sprint con los datos de la planificación (ACT-SP-002). Las columnas de estado, resultado y evidencia se completan durante la Sprint Review; hasta entonces permanecen como «Pendiente» o «Por registrar».

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

Completar el ciclo de gestión (crear, consultar, editar y eliminar) de productos, categorías y proveedores, con validaciones consistentes y mensajes de error claros.

**Resultado general:**

[Se completa en la Sprint Review: indicar si se alcanzó el objetivo.]

## 5. Revisión de los elementos del Sprint Backlog

| ID | Elemento seleccionado | Estado | Story Points | Issue |
|---|---|---|---|---|
| US-201 | Editar productos | Pendiente | 3 | Por crear |
| US-202 | Editar categorías | Pendiente | 2 | Por crear |
| US-203 | Editar proveedores | Pendiente | 2 | Por crear |
| US-204 | Validaciones de formularios | Pendiente | 2 | Por crear |

**Total de Story Points planificados:** 9

**Total de Story Points completados:** Por registrar

Nota: según la planificación (ACT-SP-002), si falta capacidad la primera historia en moverse al Product Backlog es US-204.

## 6. Incremento desarrollado

Funcionalidades previstas para el Incremento (versión v0.2.0).

| ID | Funcionalidad | Descripción | Evidencia |
|---|---|---|---|
| INC-001 | Editar productos | Entrega de US-201 según sus criterios de aceptación | Por registrar |
| INC-002 | Editar categorías | Entrega de US-202 según sus criterios de aceptación | Por registrar |
| INC-003 | Editar proveedores | Entrega de US-203 según sus criterios de aceptación | Por registrar |
| INC-004 | Validaciones de formularios | Entrega de US-204 según sus criterios de aceptación | Por registrar |
| INC-005 | Documentación | README y documentos de `Records/` actualizados | Por registrar |

## 7. Validación de criterios de aceptación

Los criterios completos están en la sección 7 de ACT-SP-002.

| ID | Criterio de aceptación | Resultado | Observaciones |
|---|---|---|---|
| CA-001 | US-201: Cada fila del listado tiene un botón «Editar» que abre un formulario precargado (incluye `informacionGeneral`). | Pendiente | Por registrar |
| CA-002 | US-201: Al guardar, el producto se actualiza con consulta preparada y el cambio se ve en el listado, el dashboard y las alertas. | Pendiente | Por registrar |
| CA-003 | US-201: No se permiten precios, IVA o stock negativos ni un código de producto repetido (mensaje claro). | Pendiente | Por registrar |
| CA-004 | US-202: Se puede cambiar el nombre de una categoría y sus productos y proveedores conservan la relación. | Pendiente | Por registrar |
| CA-005 | US-202: No se aceptan nombres vacíos ni duplicados. | Pendiente | Por registrar |
| CA-006 | US-203: El formulario de edición está precargado (empresa, contacto, teléfono y categoría). | Pendiente | Por registrar |
| CA-007 | US-203: El teléfono solo acepta dígitos y una longitud razonable. | Pendiente | Por registrar |
| CA-008 | US-203: Contacto y teléfono vacíos se guardan como `NULL` y se muestran como «—». | Pendiente | Por registrar |
| CA-009 | US-204: Todos los formularios validan en el servidor (no vacíos, números no negativos) aunque el navegador también valide. | Pendiente | Por registrar |
| CA-010 | US-204: Los mensajes distinguen entre registro duplicado y clave foránea inválida. | Pendiente | Por registrar |
| CA-011 | US-204: Se avisa cuando el precio de venta es menor que el de compra. | Pendiente | Por registrar |
| CA-012 | US-204: Los IDs de proveedores usan un prefijo distinto al de ventas. | Pendiente | Por registrar |
| CA-013 | General: El equipo demuestra crear, editar y eliminar un producto, una categoría y un proveedor, incluyendo un caso de error en cada módulo. | Pendiente | Por registrar |

## 8. Pull Requests y evidencias técnicas

| Pull Request | Descripción | Estado | Revisor |
|---|---|---|---|
| Por registrar | US-201 | Pendiente | Por asignar |
| Por registrar | US-202 | Pendiente | Por asignar |
| Por registrar | US-203 | Pendiente | Por asignar |
| Por registrar | US-204 | Pendiente | Por asignar |

**Otras evidencias:**

- Revisión de sintaxis: Por registrar (`php -l` sobre los archivos modificados).
- Pruebas manuales en XAMPP: Por registrar (casos exitosos y de error).
- Capturas de pantalla: Por registrar.
- Documentación técnica: README y `Records/` actualizados.
- Versión o demostración: Por registrar (v0.2.0).

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
| AC-003 | Publicar el release v0.2.0 en GitHub | Scrum Master | Por definir |

## 12. Evidencias y referencias

- Repositorio del equipo (fork activo): `https://github.com/PatinoMiguel-22/9Eleven`
- Repositorio original (upstream / PO): `https://github.com/FelOnCrackZ/9Eleven`
- GitHub Project (tablero del equipo): `https://github.com/users/PatinoMiguel-22/projects/1`
- Pull Requests: Por registrar
- Incremento presentado: Por registrar (v0.2.0)
- Documentación relacionada: ACT-SP-002 y `Requirements/`

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
