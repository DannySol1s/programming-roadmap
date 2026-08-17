# API

**Categoría:** Backend / Conceptos generales

## Definición
API (Application Programming Interface) es un contrato que define cómo dos programas se comunican entre sí — qué operaciones puedes pedir, qué datos debes enviar y en qué formato recibes la respuesta. No es una tecnología específica: puede ser una API REST (sobre HTTP), la API de una librería (funciones que importas), o un webhook.

## Ejemplo
El backend de Finvia expone una API REST (`/api/bot`, `/categorias`) que el frontend y Telegram consumen. Supabase expone su propia API REST autogenerada (PostgREST) sobre cada tabla de la base de datos, sin que nadie tenga que escribir esos endpoints a mano.

## Relacionado
- [Verbos HTTP](verbos-http.md)
- [Supabase](supabase.md)
- [UptimeRobot](uptimerobot.md)
- [CMS](cms.md)
- [Sanity](sanity.md)
