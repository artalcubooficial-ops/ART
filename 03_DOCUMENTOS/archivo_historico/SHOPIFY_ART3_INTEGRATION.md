# Integración Shopify ↔ ART³ CONTROL

## Eventos a contemplar

- `orders/create`
- `orders/updated`
- `orders/paid`
- `orders/cancelled`
- `fulfillments/create`
- `refunds/create`

## Diseño seguro

El pedido debe conservar SKU, referencia, color, talla, cantidad, precio, cliente y origen Shopify. La operación ART³ debe ser idempotente y registrar un identificador de evento. El motor existente debe validar antes de modificar las hojas operativas.

## Estado

Tema y CSV preparados. Webhook/API no activados: requieren credenciales, endpoint de producción, pruebas y autorización.
