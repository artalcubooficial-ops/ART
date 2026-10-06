# Sincronización de inventario

Fuente inicial: hoja `STOCK` del Excel ART³ CONTROL.

Flujo objetivo:

`Shopify orders/create` → validación de SKU/variante → operación ART³ → movimiento de inventario → actualización de `STOCK` → confirmación/fulfillment.

No se debe escribir directamente sobre históricos. La integración debe pasar por el router y motores operativos existentes, con `ID_EVENTO_ORIGEN`/`ID_EVENTO` e idempotencia. Antes de activarla se requiere prueba controlada, manejo de cancelaciones, devoluciones, reembolsos y conflictos de stock.
