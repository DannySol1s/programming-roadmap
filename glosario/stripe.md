# Stripe

**Categoría:** Backend / Procesamiento de pagos
**Visto en:** programming-roadmap

## Definición
Stripe es una plataforma para procesar pagos en línea. **Checkout Sessions** permite crear una sesión de pago y dirigir al cliente a Stripe Checkout; los **webhooks** notifican al backend cuando ocurre un evento, como la confirmación de un pago.

## Ejemplo
El backend crea una Checkout Session y devuelve su URL para que el cliente complete el pago. Después, Stripe envía un webhook al backend con el resultado; el servidor procesa ese evento para actualizar el estado del pedido.

## Relacionado
- [API](api.md)
