# JWT (JSON Web Token)

**Categoría:** Seguridad / Auth
**Visto en:** Finvia V2 (login vía Supabase Auth)

## Definición
Formato del "comprobante de identidad" que Supabase entrega tras un login exitoso. Tiene 3 partes separadas por puntos:

```
eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhYmMxMjMiLCJleHAiOjE3MzAwMDAwMDB9.4f8a2c...
└──────  header  ──────┘└────────  payload (claims) ────────┘└─ firma ─┘
```

- **Header**: algoritmo de firma usado.
- **Payload**: datos del usuario — típicamente `sub` (user id), `exp` (expiración), `role`. **No está cifrado**, solo codificado en base64 — cualquiera puede decodificarlo (probar en jwt.io), así que nunca metas datos sensibles ahí.
- **Firma**: lo que sí importa para seguridad. El servidor firma el token con un secreto que solo él conoce; si alguien altera el payload sin conocer ese secreto, la firma ya no coincide y el servidor lo rechaza.

**Analogía**: es como una carta con sello de cera. Cualquiera puede leer la carta (payload sin cifrar), pero solo el sello original (firma) prueba que nadie la alteró después de que el emisor la cerró.

## Ejemplo
Flujo en Finvia:
```
1. Usuario hace login en el SPA → Supabase Auth verifica credenciales
2. Supabase devuelve un JWT firmado
3. SPA guarda el JWT y lo manda en cada request:
      Authorization: Bearer <jwt>
4. PostgREST (dentro de Supabase) o tu backend Hono verifica la firma
5. Extrae el "sub" (user id) del payload
6. Ese user id es lo que RLS usa para filtrar filas
```

## Relacionado
- [Auth](auth.md)
- [RLS](rls.md)
- [Supabase](supabase.md)
