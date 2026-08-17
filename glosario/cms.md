# CMS

**Categoría:** Backend / Arquitectura
**Visto en:** ISC-LEGACY

## Definición
CMS (Content Management System / Sistema de Gestión de Contenidos) es una herramienta que permite crear, editar y publicar contenido (texto, imágenes, datos) sin tener que modificar código ni tocar directamente la base de datos. Existen dos grandes enfoques:

- **CMS tradicional (monolítico)** — como WordPress: el CMS genera también el HTML final que ve el usuario. Contenido y presentación viven juntos.
- **CMS headless** — como [Sanity](sanity.md): el CMS solo administra y expone el contenido (normalmente vía API), sin opinar sobre cómo se renderiza. El frontend (React, Next.js, etc.) consume esos datos y decide la presentación.

## Ejemplo
En ISC-LEGACY, el contenido se administra desde un CMS headless en vez de tenerlo hardcodeado en el código o editado a mano en la base de datos — así una persona no técnica puede actualizar textos o imágenes sin tocar el repositorio.

## Relacionado
- [Sanity](sanity.md)
- [API](api.md)
