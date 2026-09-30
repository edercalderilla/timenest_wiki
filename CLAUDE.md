# TimeNest — reglas de ramas y documentación

Este repo es la documentación para usuarios de TimeNest (Mintlify). El código vive en los repos hermanos `../app_citas_web`, `../timenest` y `../app_citas`.

## Ramas

TimeNest usa `dev` como rama principal de desarrollo y `main` como rama de producción.

- `dev` contiene cambios en desarrollo o pendientes de publicación (= próxima versión de TimeNest).
- `main` representa el estado publicado en producción (= versión actual).
- Mintlify publica la documentación desde `main`.

## Regla de publicación

Una funcionalidad se considera disponible para los usuarios únicamente cuando:

1. El código fue mergeado de `dev` a `main`.
2. El cambio fue desplegado en producción.
3. La documentación correspondiente también está en `main`.

## Regla de documentación

- Toda funcionalidad nueva visible para el usuario debe incluir su documentación antes de llegar a `main`.
- La documentación puede actualizarse directamente mientras se trabaja en `dev`. No se crean ramas independientes solo para documentación.
- No se documentan cambios internos que no afecten al usuario final.
- Nunca publiques documentación sobre una funcionalidad que todavía no esté destinada a producción.

## Antes de hacer merge de `dev` → `main`

Revisa los cambios que llegarán a producción y verifica si:

- Se agregó una funcionalidad visible para el usuario.
- Se modificó el comportamiento de una funcionalidad existente.
- Se agregó o modificó alguna configuración que el usuario deba conocer.
- Se modificaron límites, permisos, planes o flujos de usuario.

Si alguno aplica, la documentación correspondiente debe estar actualizada antes del merge.

**Principio:** el código y la documentación llegan juntos a `main` cuando forman parte de una funcionalidad destinada a producción.
