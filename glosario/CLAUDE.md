# Convención del glosario

Instrucciones para agregar nuevos términos a este glosario. Aplican tanto si el usuario pide agregar un concepto como si detectas que se explicó un término nuevo durante una sesión y vale la pena registrarlo.

## Estructura de cada término

Un archivo por término, en kebab-case (ej. `service-role-key.md`), con esta plantilla:

```markdown
# <Término>

**Categoría:** Seguridad / Frontend / Backend / Arquitectura / Base de datos
**Visto en:** <proyecto donde se aprendió>

## Definición
...

## Ejemplo
...

## Relacionado
- [Otro término](otro-termino.md)
```

## Al agregar un término nuevo

1. Crear el archivo `glosario/<slug>.md` con la plantilla de arriba.
2. Actualizar `glosario/README.md`: agregar el link bajo la letra correspondiente, en orden alfabético. Si la letra no existe aún en el índice, crearla.
3. Si el término se relaciona con uno existente, agregar el link cruzado en ambos archivos (sección "Relacionado" de ida y vuelta), no solo en el nuevo.
4. Los links en "Relacionado" siempre en formato markdown `[Texto](archivo.md)`, nunca texto plano. Si el usuario pega contenido sin ese formato (típico al copiar texto ya renderizado desde el chat), corregirlo antes de guardar.

## Qué NO va en el glosario

- Notas específicas de un solo proyecto sin valor conceptual reutilizable — esas van en el módulo correspondiente (ej. `11-backend/apuntes/`).
- Términos ya cubiertos por otro archivo — si ya existe, actualizar o enlazar en vez de duplicar.
