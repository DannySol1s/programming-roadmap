# RLS (Row Level Security)

**Categoría:** Base de datos / Seguridad
**Visto en:** Finvia V2 (tabla `gastos`)

## Definición
Función nativa de PostgreSQL (no exclusiva de Supabase) que aplica un filtro a nivel de fila, **dentro de la base de datos**, no en el código de la aplicación.

Sin RLS, la seguridad depende de que TODO el código backend recuerde escribir `WHERE user_id = ?` en cada consulta — un solo endpoint que lo olvide es una fuga de datos entre usuarios. Con RLS, la base de datos lo garantiza siempre, sin importar quién o qué hace la consulta.

## Ejemplo
```sql
alter table gastos enable row level security;

create policy "cada usuario ve solo sus gastos"
on gastos for select
using (auth.uid() = user_id);

create policy "cada usuario inserta solo a su propio nombre"
on gastos for insert
with check (auth.uid() = user_id);
```

`auth.uid()` lee el `sub` del JWT de la petición actual. Aunque el bot de Telegram use la `anon key` (pública) para leer gastos, RLS impide que el usuario A vea los gastos del usuario B — incluso si alguien manipulara las llamadas directamente contra la API REST de Supabase sin pasar por el backend.

## Relacionado
- [JWT](jwt.md)
- [Anon key](anon-key.md)
- [Service role key](service-role-key.md)
- [Supabase](supabase.md)
