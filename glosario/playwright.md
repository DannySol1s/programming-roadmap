# Playwright

**Categoría:** Frontend / Testing
**Visto en:** _(pendiente — agrega aquí el proyecto donde lo uses)_

## Definición

Playwright es un framework de Microsoft para escribir **pruebas end-to-end (E2E)**: revisa que el sistema completo funcione desde los ojos del usuario. En lugar de probar una función aislada, abre un navegador real (Chromium, Firefox o WebKit), navega por la aplicación, hace clic, llena formularios y verifica lo que aparece en pantalla.

Es la capa más alta de la pirámide de pruebas:

```
        /\
       /E2E\      ← Playwright: flujo completo como usuario (pocas, lentas)
      /------\
     /Integra-\   ← Varias piezas juntas (API + BD)
    /----------\
   /  Unitarias \ ← Funciones aisladas (muchas, rápidas)
  /--------------\
```

Ventajas: espera automáticamente a que los elementos estén listos (menos pruebas "frágiles"), soporta varios navegadores y graba trazas para depurar fallos. Desventaja: son más lentas y costosas de mantener que las unitarias, así que se reservan para los flujos críticos (login, compra, registro).

## Ejemplo

Instalar y crear la configuración inicial:

```bash
npm init playwright@latest
```

Probar que un usuario puede iniciar sesión:

```typescript
import { test, expect } from "@playwright/test";

test("el usuario inicia sesión correctamente", async ({ page }) => {
  await page.goto("http://localhost:3000/login");
  await page.getByLabel("Correo").fill("usuario@ejemplo.com");
  await page.getByLabel("Contraseña").fill(process.env.TEST_PASSWORD!);
  await page.getByRole("button", { name: "Entrar" }).click();

  await expect(page.getByText("Bienvenido")).toBeVisible();
});
```

Ejecutar las pruebas:

```bash
npx playwright test
```

## Relacionado

_(ninguno todavía)_
