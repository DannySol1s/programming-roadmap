# Hono

**Categoría:** Backend / Arquitectura

**Visto en:** programming-roadmap

## Definición
Hono es un framework web ligero para crear APIs y aplicaciones del lado del servidor utilizando JavaScript o TypeScript. Está basado en estándares web como `Request` y `Response`, por lo que puede ejecutarse en distintos runtimes, incluyendo Bun, Node.js, Deno y Cloudflare Workers.

## Ejemplo

Crear una API básica con Hono y Bun:

````typescript
import { Hono } from "hono";

const app = new Hono();

app.get("/", (c) => {
  return c.json({ mensaje: "Hola desde Hono" });
});

export default app;