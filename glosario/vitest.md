# Vitest

**Categoría:** Frontend / Testing
**Visto en:** _(pendiente — agrega aquí el proyecto donde lo uses)_

## Definición

Vitest es un framework de **pruebas unitarias** para JavaScript y TypeScript: revisa piezas sueltas del frontend (funciones, hooks, componentes) de forma aislada, sin levantar la aplicación completa ni abrir un navegador real.

Está construido sobre **Vite**, por lo que reutiliza su configuración y es muy rápido. Su API es compatible con Jest (`describe`, `test`, `expect`), así que migrar entre ambos es sencillo.

Ocupa la base de la pirámide de pruebas:

```
        /\
       /E2E\      ← Playwright: flujo completo como usuario
      /------\
     /Integra-\
    /----------\
   /  Unitarias \ ← Vitest: piezas sueltas (muchas, rápidas)
  /--------------\
```

Ventajas: muy rápido, modo *watch* que re-ejecuta solo lo que cambió y soporte nativo para TypeScript. Limitación: no garantiza que las piezas funcionen bien juntas; para eso existen las pruebas E2E.

## Ejemplo

Instalar:

```bash
npm install -D vitest
```

Probar una función que calcula el total de un carrito:

```typescript
// carrito.ts
export function calcularTotal(precios: number[]): number {
  return precios.reduce((suma, precio) => suma + precio, 0);
}
```

```typescript
// carrito.test.ts
import { describe, test, expect } from "vitest";
import { calcularTotal } from "./carrito";

describe("calcularTotal", () => {
  test("suma todos los precios", () => {
    expect(calcularTotal([100, 250, 50])).toBe(400);
  });

  test("devuelve 0 si el carrito está vacío", () => {
    expect(calcularTotal([])).toBe(0);
  });
});
```

Ejecutar:

```bash
npx vitest
```

## Relacionado

- [Playwright](playwright.md)
