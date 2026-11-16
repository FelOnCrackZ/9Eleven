# Flujo de trabajo en GitHub

> **Repositorios:** El desarrollo activo, ramas, issues y Pull Requests se gestionan en el fork del equipo (`https://github.com/PatinoMiguel-22/9Eleven`) y su tablero (`https://github.com/users/PatinoMiguel-22/projects/1`). El repositorio original (`https://github.com/FelOnCrackZ/9Eleven`) se mantiene como línea base *upstream* del Product Owner.

## 1. Tablero (GitHub Project)

| Columna | Significado |
|---|---|
| **Backlog** | Elementos del Product Backlog aún no seleccionados |
| **Ready** | Seleccionados para el Sprint; cumplen la Definition of Ready |
| **In progress** | Alguien está trabajando (máximo 2 issues por persona) |
| **In review** | Pull Request abierto, esperando revisión |
| **Done** | Integrado a `main` y cumple la Definition of Done |

Campos recomendados en el proyecto: **Sprint**, **Story Points** y **Responsable**.

## 2. Issues

- Una historia y sus tareas se registran como issues. Título: `[US-301] Nueva venta con descuento de stock`.
- Las tareas se enlazan a su historia (`Parte de #12`) o se listan en ella como casillas.
- Etiquetas: `feature`, `bug`, `security`, `database`, `docs`, `devops`, `refactor`, `good first issue`, y la prioridad `prioridad: alta`, `prioridad: media` o `prioridad: baja`.
- Descripción mínima: contexto, qué se espera y **criterios de aceptación**. El contenido ya redactado está en [`product-backlog.md`](product-backlog.md).
- Crea los issues **en orden numérico** (#1, #2, #3…) para que las referencias «Backlog #N» coincidan con la numeración de GitHub.

## 3. Ramas

La rama `main` siempre debe funcionar. Nunca se trabaja directo en `main`.

| Tipo | Patrón | Ejemplo |
|---|---|---|
| Historia | `feature/US-XXX-nombre-corto` | `feature/US-301-nueva-venta` |
| Corrección | `fix/descripcion-corta` | `fix/error-eliminar-producto` |
| Documentación | `docs/descripcion-corta` | `docs/ACT-SP-002` |

```bash
git checkout main
git pull
git checkout -b feature/US-301-nueva-venta
```

## 4. Commits

Mensajes cortos, en presente y con prefijo:

```text
feat(ventas): guardar venta y descontar stock en una transacción
fix(productos): mostrar mensaje al eliminar un producto con ventas
docs(records): agregar acta ACT-SP-002
refactor(config): leer credenciales desde variables de entorno
```

Prefijos: `feat`, `fix`, `docs`, `refactor`, `chore`.

## 5. Pull Requests

1. Abre el PR hacia `main` cuando la historia cumpla los criterios.
2. Título igual al del commit principal; en la descripción pon `Closes #N` para cerrar el issue al integrar.
3. Asigna **al menos un revisor** que no sea quien escribió el código.
4. El revisor prueba la rama, no solo lee el código.
5. Se integra solo con la revisión aprobada y los comentarios resueltos.

### Plantilla para la descripción del PR

```markdown
## Qué cambia
[Resumen breve]

## Issue relacionado
Closes #N

## Cómo probarlo
1. [Paso]
2. [Paso]

## Evidencia
[Capturas o descripción de lo que se vio]

## Checklist (Definition of Done)
- [ ] Cumple los criterios de aceptación
- [ ] `php -l` sin errores en los archivos modificados
- [ ] Probado en XAMPP: caso exitoso y caso de error
- [ ] `requerirLogin()`, consultas preparadas y `h()` donde corresponde
- [ ] Sin contraseñas ni credenciales
- [ ] Documentación y SQL actualizados si cambió el esquema
```

## 6. Versiones (releases)

Al terminar cada Sprint, el Scrum Master publica una versión del Incremento aceptado:

| Sprint | Versión |
|---|---|
| 1 | `v0.1.0` |
| 2 | `v0.2.0` |
| 3 | `v0.3.0` |
| 4 | `v1.0.0` |

```bash
git tag -a v0.1.0 -m "Sprint 1: base segura y reproducible"
git push origin v0.1.0
```

Luego se crea el *Release* en GitHub con un resumen de lo entregado y lo pendiente.

## 7. Protección de `main` (recomendado)

En **Settings → Branches → Add rule** para `main`:

- [x] Require a pull request before merging
- [x] Require approvals (1)

## 8. Qué NO subir al repositorio

- Contraseñas, claves ni archivos `.env` con datos reales.
- Copias de la base de datos con información real.
- Archivos temporales del editor o del sistema (`.vscode/`, `.idea/`, `Thumbs.db`, `.DS_Store`).
- Carpetas con archivos subidos por usuarios, si se agregan en el futuro.

## 9. Documentos y actas

Las actas de `Records/` también se suben por Pull Request (`docs/ACT-…`), y su aprobación queda como revisión o comentario en ese PR.
