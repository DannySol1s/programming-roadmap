# Auth (Autenticación vs Autorización)

**Categoría:** Seguridad
**Visto en:** Finvia V2

## Definición
Dos preguntas distintas que a veces se confunden:

- **Autenticación (Authentication)**: "¿quién eres?" — verificar identidad (login con contraseña, OAuth, etc.)
- **Autorización (Authorization)**: "¿qué puedes hacer?" — una vez sabemos quién eres, decidir qué recursos puedes leer/modificar.

## Ejemplo
Supabase Auth resuelve la autenticación (te da un usuario verificado); RLS resuelve la autorización (decide qué filas de la tabla ve ese usuario).

## Relacionado
- [JWT](jwt.md)
- [RLS](rls.md)
- [Supabase](supabase.md)
