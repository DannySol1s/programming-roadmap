# GET

**Categoría:** Backend / API
**Visto en:** Finvia V2

## Definición
Verbo HTTP para leer/recuperar un recurso sin producir efectos secundarios. Es "seguro" (safe — no debería modificar estado en el servidor) e idempotente: pedir el mismo GET N veces devuelve el mismo resultado, salvo que el dato subyacente cambie por otra razón ajena a la petición.

## Ejemplo
`GET /categorias` devuelve la lista completa de categorías de Finvia; `GET /categorias/5` devuelve solo la categoría con id 5. Los parámetros van en la URL (query string o path), nunca en el body — por convención, un GET con body es ignorado o directamente rechazado por muchos servidores.

## Relacionado
- [Verbos HTTP](verbos-http.md)
- [API](api.md)
