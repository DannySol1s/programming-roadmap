# PATCH

**Categoría:** Backend / API
**Visto en:** Finvia V2

## Definición
Verbo HTTP para actualizar parcialmente un recurso — solo los campos que envías se modifican, el resto queda igual. A diferencia de PUT, no necesitas mandar el objeto completo.

## Ejemplo
`PATCH /categorias/5` con `{color: "#fff"}` cambia solo el color de la categoría 5, sin tocar su nombre. Es la opción más común en APIs REST reales porque evita mandar datos que no cambiaron.

**Sobre idempotencia**: depende de la operación. `PATCH {color: "#fff"}` es idempotente (repetirlo deja el mismo color). Un `PATCH {contador: contador + 1}` (incremento relativo) **no** lo sería — cada repetición cambia el resultado.

## Relacionado
- [Verbos HTTP](verbos-http.md)
- [PUT](put.md) — contraste: parcial vs. completo
