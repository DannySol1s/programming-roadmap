# Vercel

**Categoría:** Frontend / Arquitectura / DevOps
**Visto en:** programming-roadmap

## Definición

Vercel es una plataforma de hosting especializada en aplicaciones frontend y full-stack basadas en **Next.js**. Está optimizada para desplegar aplicaciones estáticas (SSG) y con renderizado del lado del servidor (SSR) con máximo rendimiento.

Fue creada por los mismos autores de Next.js y se integra perfectamente con el framework.

## Ejemplo

Desplegar un sitio Next.js:

1. Hacer push del código a GitHub
2. Vercel detecta automáticamente que es un proyecto Next.js
3. Ejecuta `next build` y optimiza el output
4. Despliega en la red global de CDN de Vercel
5. Cada push redeploy automáticamente

```javascript
// next.config.js — Vercel lo detecta automáticamente
module.exports = {
  reactStrictMode: true,
  // Vercel configura esto implícitamente
}
```

## Ventajas

- Optimización automática para Next.js
- Redeploy instantáneo en cada push
- Excelente rendimiento (CDN global)
- Vista previa en cada Pull Request
- Integración perfecta con GitHub
- Plan gratuito generoso

## Desventajas

- Menos flexible fuera del ecosistema Next.js
- No es la mejor opción para APIs complejas o backends standalone
- Serverless tiene limitaciones de tiempo de ejecución

## Cuándo usar Vercel vs Render

| Escenario | Usar |
|-----------|------|
| Frontend con Next.js | Vercel |
| API REST independiente | Render |
| Full-stack con Next.js | Vercel |
| Base de datos + Backend | Render |
| Landing page estática | Vercel |

## Relacionado

- [Render](render.md) — Alternativa para backends completos
- [Deployment](deployment.md) — Concepto general
- [Next.js](next-js.md) — Framework web que Vercel optimiza
- [CDN](cdn.md) — Tecnología que Vercel utiliza para distribución global