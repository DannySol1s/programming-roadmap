# Render

**Categoría:** Backend / Arquitectura / DevOps
**Visto en:** programming-roadmap

## Definición

Render es una plataforma de hosting en la nube (PaaS — Platform as a Service) que permite desplegar aplicaciones web, APIs REST, servicios en background y bases de datos PostgreSQL sin necesidad de gestionar infraestructura.

Simplifica el deployment permitiendo conectar directamente un repositorio Git. Cada commit en la rama configurada dispara un redeploy automático.

## Ejemplo

Desplegar una API Node.js:

1. Conectar repositorio GitHub a Render
2. Configurar la rama (`main`)
3. Definir el comando de inicio (`npm start`)
4. Render ejecuta el build, instala dependencias y mantiene la app en línea
5. Las variables de entorno se configuran en el dashboard (no en el código)

## Ventajas

- Fácil de usar para principiantes
- Hosting automático con redeploy en cada push
- Base de datos PostgreSQL integrada
- Plan gratuito con limitaciones
- Soporte HTTPS automático

## Desventajas

- Rendimiento limitado en plan gratuito (puede "dormir" la app)
- Menos control sobre infraestructura que servidores VPS
- Costos pueden aumentar rápidamente con alto tráfico

## Cuándo usar Vercel vs Render

| Escenario | Usar |
|-----------|------|
| Frontend con Next.js | Vercel |
| API REST independiente | Render |
| Full-stack con Next.js | Vercel |
| Base de datos + Backend | Render |
| Landing page estática | Vercel |

## Relacionado

- [Vercel](vercel.md) — Alternativa especializada en frontend
- [Deployment](deployment.md) — Concepto general
- [Variables de entorno](variables-de-entorno.md) — Cómo manejar secretos en Render