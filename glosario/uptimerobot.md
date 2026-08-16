# UptimeRobot

**Categoría:** DevOps / Monitoreo
**Visto en:** Finvia V2 (monitor de `finviav2-backend.onrender.com`)

## Definición
Servicio externo de monitoreo de disponibilidad ("uptime monitoring"). Hace peticiones periódicas (HTTP, ping, puerto, etc.) a una URL y alerta si deja de responder. También se usa, de forma no oficial, como truco de "keep-alive" — mantener despierto un servicio que se duerme por inactividad (ej. Render free tier, que hiberna tras ~15 minutos sin tráfico).

## Ejemplo / limitación real
El plan free permite decenas de monitores con intervalo de 5 minutos, pero **no incluye headers HTTP personalizados** (función de pago). Eso impide usarlo directamente contra un endpoint de [Supabase](supabase.md) que exige headers `apikey`/`Authorization` — habría que exponer antes un endpoint público sin autenticación (ej. una Edge Function con `verify_jwt = false`).

Un monitor pausado no da ningún error visible por sí solo — hay que revisar el estado manualmente en el dashboard (icono + texto "Paused"), como pasó en este proyecto.

## Relacionado
- [API](api.md)
- [Supabase](supabase.md)
