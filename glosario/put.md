# PUT

**Categoría:** Backend / API
**Visto en:** Finvia V2

## Definición
Verbo HTTP para reemplazar por completo un recurso existente. Es idempotente: enviar el mismo PUT varias veces deja el recurso en el mismo estado final, porque cada petición sobreescribe el objeto entero, no solo una parte.

## Ejemplo
`PUT /categorias/5` con `{nombre: "Comida", color: "#fff"}` reemplaza toda la categoría 5 — si omites un campo que ya existía (ej. `color`), un PUT estricto lo eliminaría o lo dejaría en su valor por defecto, porque reemplaza el objeto completo, no lo combina con lo anterior.

## Relacionado
- [Verbos HTTP](verbos-http.md)
- [PATCH](patch.md) — contraste: parcial vs. completo
- [POST](post.md) — contraste de idempotencia
