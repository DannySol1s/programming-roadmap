# Sanity

**Categoría:** Backend / CMS
**Visto en:** ISC-LEGACY

## Definición
Sanity es un [CMS](cms.md) headless: administra el contenido (texto, imágenes, referencias entre documentos) y lo expone a través de una API (GROQ o GraphQL), pero no genera el HTML final — eso lo decide el frontend que consume esos datos. Se compone principalmente de dos piezas:

- **Sanity Studio** — el editor de contenido (una app de React configurable con "schemas" que definen qué campos tiene cada tipo de documento).
- **Content Lake** — donde vive el contenido, consultable vía API con GROQ (su lenguaje de queries propio) o GraphQL.

## Ejemplo
En ISC-LEGACY, en vez de guardar el contenido editable directamente en la base de datos de la app o hardcodeado en el código, se administra desde Sanity Studio y el frontend lo consume vía [API](api.md) — así el contenido se puede actualizar sin hacer deploy ni tocar la base de datos de la aplicación.

## Relacionado
- [CMS](cms.md)
- [API](api.md)
