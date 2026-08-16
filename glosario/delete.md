# DELETE

**Categoría:** Backend / API
**Visto en:** Finvia V2

## Definición
Verbo HTTP para eliminar un recurso. Es idempotente: borrar el mismo recurso una vez o varias veces deja el mismo resultado final (ya no existe) — las peticiones repetidas normalmente responden 404 en vez de error, pero el estado del sistema no cambia entre la primera y las siguientes.

## Ejemplo
`DELETE /categorias/5` elimina la categoría 5. Por su idempotencia, es seguro que el bot de Telegram reintente un DELETE si hubo timeout de red, sin riesgo de "doble borrado" — a diferencia de un POST, donde reintentar sí puede duplicar datos.

## Relacionado
- [Verbos HTTP](verbos-http.md)
- [POST](post.md) — contraste de idempotencia
