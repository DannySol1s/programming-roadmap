# Gitleaks

**Categoría:** Seguridad / DevOps

## Definición
Herramienta de código abierto (escrita en Go) que escanea repositorios de git — historial completo, working directory, o solo lo que está en staging — buscando secretos hardcodeados: API keys, tokens, contraseñas, llaves privadas, etc. Detecta patrones mediante expresiones regulares y reglas predefinidas por proveedor (AWS, Stripe, Supabase, GitHub, etc.).

## Ejemplo
Se usa comúnmente como hook de pre-commit (bloquea el commit si detecta un secreto antes de que llegue al historial) o como paso de CI en GitHub Actions. Es la herramienta que hubiera detectado automáticamente el caso real de este roadmap: la API key de NewsData.io que estuvo hardcodeada en el repo de BigData antes de moverse a `.env` — el mismo tipo de error que cometería exponer una [service role key](service-role-key.md) por accidente.

## Relacionado
- [Anon key](anon-key.md)
- [Service role key](service-role-key.md)
