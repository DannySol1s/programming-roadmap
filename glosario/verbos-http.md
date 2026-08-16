# Verbos HTTP

**Categoría:** Backend / API
**Visto en:** Finvia V2 (API REST de categorías)

## Definición
Cada verbo comunica una intención sobre un recurso.

| Verbo | Intención | Ejemplo | ¿Idempotente?* |
|---|---|---|---|
| `GET` | Leer, sin efectos secundarios | `GET /categorias` → listar todas | Sí |
| `POST` | Crear algo nuevo (o ejecutar una acción, como un RPC) | `POST /categorias {nombre: "Comida"}` | No |
| `PUT` | Reemplazar el recurso completo | `PUT /categorias/5 {nombre: "Comida", color: "#fff"}` | Sí |
| `PATCH` | Actualizar parcialmente | `PATCH /categorias/5 {color: "#fff"}` | Depende |
| `DELETE` | Eliminar | `DELETE /categorias/5` | Sí |

*Idempotente = repetir la misma petición N veces produce el mismo resultado final que hacerla una vez.

## Ejemplo
Si el bot de Telegram reintenta una petición por timeout de red, un `DELETE` repetido no rompe nada, pero un `POST` repetido podría crear duplicados si no lo controlas.

## Relacionado
- [SPA](spa.md)
- [API](api.md)
- [GET](get.md)
- [POST](post.md)
- [PUT](put.md)
- [PATCH](patch.md)
- [DELETE](delete.md)
