# Supabase

**Categoría:** Backend / BaaS (Backend as a Service)
**Visto en:** Finvia V2

## Definición
Plataforma de "Backend as a Service" construida sobre PostgreSQL. En vez de programar un servidor desde cero, Supabase da, sobre una base de datos Postgres real:

- **Auth** — login y manejo de usuarios, con tokens JWT.
- **API REST autogenerada** (PostgREST) — cada tabla queda expuesta como endpoint sin escribir backend.
- **RLS** — seguridad a nivel de fila directamente en la base de datos.
- **Realtime** — suscripciones en vivo a cambios en las tablas (vía websockets).
- **Storage** — almacenamiento de archivos.
- **Edge Functions** — funciones serverless para lógica personalizada.

## Ejemplo
En Finvia, Supabase resuelve a la vez: el login de usuarios (Auth), la persistencia de gastos (Postgres), que cada usuario solo vea sus propios datos (RLS) y la sincronización en vivo del dashboard (Realtime) — sin que el proyecto tuviera que construir cada una de esas piezas por separado.

Igual que Render, el plan free de Supabase **pausa el proyecto tras 7 días sin actividad de API** — de ahí la necesidad de un keep-alive (ver [UptimeRobot](uptimerobot.md)).

## Relacionado
- [Auth](auth.md)
- [JWT](jwt.md)
- [RLS](rls.md)
- [Anon key](anon-key.md)
- [Service role key](service-role-key.md)
- [API](api.md)
- [UptimeRobot](uptimerobot.md)
