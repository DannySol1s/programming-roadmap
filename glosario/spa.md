# SPA (Single Page Application)

**Categoría:** Frontend / Arquitectura
**Visto en:** Finvia V2 (SvelteKit)

## Definición
Patrón de arquitectura frontend donde el navegador descarga una sola vez un HTML mínimo + el bundle de JavaScript. A partir de ahí, la navegación entre "páginas" no recarga el documento completo — el JS reescribe el DOM en el cliente y pide solo los datos (JSON) al backend vía API.

```
Modelo tradicional (multi-page):          Modelo SPA:
Click → GET /dashboard                    Click → JS intercepta, cambia vista
       → servidor renderiza HTML                → fetch("/api/gastos") → JSON
       → navegador recarga TODO                 → JS actualiza solo esa sección
```

## Ejemplo
En Finvia V2, "SvelteKit SPA" significa que SvelteKit compila a archivos estáticos (HTML/CSS/JS) que Vercel sirve como un CDN, y todo el trabajo de traer datos ocurre en el navegador del usuario, llamando al backend en Render.

**Trade-off**: navegación interna muy rápida tras la primera carga, pero el SEO es débil (los crawlers ven un HTML casi vacío hasta que el JS ejecuta) — irrelevante para un dashboard financiero privado.

## Relacionado
- [Verbos HTTP](verbos-http.md)
- [API](api.md)
