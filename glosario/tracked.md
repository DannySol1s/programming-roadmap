# Tracked (Git)

**Categoría:** Git / Control de versiones

## Definición
Un archivo "tracked" (rastreado) es uno que git ya conoce — porque formó parte de un commit anterior, o porque se agregó explícitamente con `git add`. Git vigila estos archivos y detecta cualquier cambio en su contenido al correr `git status` o `git diff`.

## Ejemplo
En este mismo repo, `README.md` está tracked — al editarlo para agregar la sección del glosario, `git status` lo mostró como `modified`, no como `untracked`, porque ya existía en un commit anterior.

## Relacionado
- [Untracked](untracked.md)
