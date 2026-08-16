# POST

**Categoría:** Backend / API
**Visto en:** Finvia V2

## Definición
Verbo HTTP para crear un nuevo recurso, o para ejecutar una acción que no encaja en los otros verbos (como invocar un RPC). **No es idempotente**: repetir la misma petición POST puede crear múltiples recursos duplicados.

## Ejemplo
`POST /categorias` con `{nombre: "Comida"}` en el body crea una categoría nueva cada vez que se ejecuta. Si el bot de Telegram reintenta un POST por timeout de red sin ningún control de idempotencia (ej. una idempotency key o una verificación previa de "¿ya existe?"), puede terminar duplicando un gasto.

## Relacionado
- [Verbos HTTP](verbos-http.md)
- [PUT](put.md) — contraste de idempotencia
- [API](api.md)
