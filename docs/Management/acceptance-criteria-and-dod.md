# Criterios de aceptación, Definition of Ready y Definition of Done

## 1. Criterios de aceptación

Un **criterio de aceptación** es una condición que se puede comprobar con *sí* o *no* y que debe cumplirse para dar por terminada una historia. Son el contrato entre el equipo y el Product Owner: en la Sprint Review se validan uno por uno.

### Cómo redactarlos

1. **Observables y verificables.** Alguien debe poder probarlos sin interpretar.
2. **Una condición por criterio.** Si lleva una «y» que une dos cosas distintas, se separa.
3. **Cubrir los tres casos:** el caso exitoso, el caso de error y los permisos (¿qué pasa sin sesión?).
4. **Hablar del resultado, no de la implementación.** Se describe lo que el usuario ve o lo que queda en la base de datos, no cómo se programa.
5. **Usar datos concretos** cuando ayuden (valores límite, mensajes esperados).
6. **Evitar palabras vagas:** «rápido», «amigable», «correcto», «adecuado».

### Formato

Lista de verificación en el acta de planificación:

```markdown
**US-301**

- [ ] «Nueva venta» permite agregar varios productos con cantidades y calcula subtotales y total.
- [ ] Al guardar se crean `ventas` y `detalle_ventas` y se descuenta `stockActual`.
- [ ] No se puede vender más unidades de las que hay en stock.
```

Si una historia es compleja, puede usarse el formato **Dado / Cuando / Entonces**:

```text
Dado que el producto «Agua 600ml» tiene 5 unidades en stock
Cuando intento vender 6 unidades
Entonces el sistema rechaza la venta y muestra «Stock insuficiente», sin descontar nada
```

### Ejemplos

| ❌ Mal | ✅ Bien |
|---|---|
| La eliminación funciona correctamente. | Intentar eliminar un producto con ventas muestra un mensaje claro y el producto sigue existiendo. |
| Las ventas descuentan el stock. | Tras guardar una venta de 2 unidades, el `stockActual` del producto baja exactamente en 2. |
| El sistema es seguro. | Todas las páginas protegidas redirigen a `index.php` si no hay sesión activa. |
| Se puede editar el producto. | El formulario de edición abre precargado, rechaza precios negativos y rechaza un código ya usado por otro producto. |

## 2. Definition of Ready (lista para entrar a un Sprint)

Una historia se puede seleccionar en la Sprint Planning si:

- [ ] Está escrita como «Como [rol], quiero [funcionalidad], para [beneficio]».
- [ ] Tiene criterios de aceptación claros y verificables.
- [ ] Está estimada en Story Points y no supera 5 SP (si es mayor, se divide).
- [ ] Sus dependencias están resueltas o planificadas antes.
- [ ] El Product Owner confirmó su prioridad y resolvió las dudas de negocio.

## 3. Definition of Done (terminada)

Una historia solo está **terminada** si cumple todo lo siguiente. Esta definición aplica a todo el Incremento.

- [ ] **Cumple los criterios de aceptación** de la historia.
- [ ] **Sin errores de sintaxis:** `php -l archivo.php` pasa en todos los archivos modificados.
- [ ] **Probada manualmente** en XAMPP con los datos de ejemplo: al menos un caso exitoso y uno de error, y la evidencia (capturas o pasos) queda en el Pull Request.
- [ ] **Seguridad básica** (ver sección 4).
- [ ] **Sin secretos:** no se versionan contraseñas, claves ni datos reales.
- [ ] **Base de datos coherente:** si cambió el esquema, se actualizaron `db_9eleven.sql` y el script de migración.
- [ ] **Documentación actualizada** (README, diagramas de `Resources/` o actas) cuando corresponde.
- [ ] **Pull Request revisado y aprobado** por otro integrante.
- [ ] **Integrada a `main`** y el issue movido a *Done*.

> Cuando exista el flujo de integración continua (Backlog #16), `php -l` y las pruebas automáticas se ejecutarán en cada Pull Request y pasarán a ser requisito.

## 4. Checklist de seguridad para PHP (en cada Pull Request)

- [ ] La página protegida llama `requerirLogin()` en la primera línea.
- [ ] Toda consulta con datos del usuario usa `prepare()` y parámetros; **nunca** se concatenan variables en el SQL.
- [ ] Todo dato que se imprime en HTML pasa por `h()`.
- [ ] Los formularios que modifican datos usan `POST` (no `GET`).
- [ ] Las operaciones de varias tablas (ventas, entradas) van dentro de una **transacción**.
- [ ] Las excepciones de PDO se capturan y se muestra un mensaje claro, no un error técnico.
- [ ] Los números se validan (no negativos, tipo correcto) en el servidor.
- [ ] No hay `var_dump`, `print_r` ni código de depuración.

## 5. Estados al validar en la Sprint Review

| Estado | Significado |
|---|---|
| **Cumplido** | El criterio se demostró y funciona. |
| **Parcial** | Funciona con limitaciones; se registra la justificación y lo faltante vuelve al Backlog. |
| **No cumplido** | No funciona o no se demostró; vuelve al Backlog. |

## 6. Aceptación del proyecto

Al final del semestre el Product Owner decide la aceptación con [`Records/project-acceptance.md`](../Records/project-acceptance.md). Allí se define el escenario manual de 9 pasos y los criterios de decisión.
