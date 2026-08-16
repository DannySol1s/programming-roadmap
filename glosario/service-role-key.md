# Service role key

**Categoría:** Seguridad / Supabase
**Visto en:** Finvia V2

## Definición
La segunda llave de API de Supabase. Es la "llave maestra": **ignora RLS por completo** y tiene acceso total a la base de datos.

## Ejemplo
La usaría el backend de Finvia (Hono/Bun) si necesitara operaciones administrativas (ej. el bot creando registros a nombre de cualquier usuario sin pasar por su sesión). Debe vivir solo como variable de entorno en el servidor (Render), **nunca** en el bundle del frontend ni en el repositorio.

## Relacionado
- [Anon key](anon-key.md)
- [RLS](rls.md)
- [Supabase](supabase.md)
- [Gitleaks](gitleaks.md)
