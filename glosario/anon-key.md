# Anon key

**Categoría:** Seguridad / Supabase
**Visto en:** Finvia V2

## Definición
Una de las dos llaves de API que da Supabase por proyecto. Respeta las políticas de RLS — actúa como un "gafete de visita": solo puede hacer lo que las políticas explícitamente le permitan.

## Ejemplo
La usa el SPA de Finvia (SvelteKit). Aunque esté visible en el código del navegador (inevitable en un SPA), un atacante que la extraiga solo puede hacer lo que RLS le permita — no puede leer datos de otros usuarios.

## Relacionado
- [Service role key](service-role-key.md)
- [RLS](rls.md)
- [Supabase](supabase.md)
- [Gitleaks](gitleaks.md)
