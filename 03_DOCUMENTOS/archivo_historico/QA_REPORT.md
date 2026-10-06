# QA inicial del candidato Shopify

## PASS

- ZIP válido con estructura Online Store 2.0.
- `layout/theme.liquid` presente en la raíz del ZIP.
- Templates JSON para home, producto, colección, búsqueda y carrito.
- Carrito y checkout usan rutas nativas de Shopify.
- Tema responsive con breakpoints móvil/tablet/desktop.
- Productos no están hardcodeados en el tema; se leen de Shopify.
- JSON templates válidos para home, producto, colección, carrito, búsqueda y páginas.
- CSV verificado con 96 filas, 19 handles únicos y 19 textos ALT no vacíos.
- ZIP verificado con `layout/theme.liquid` y secciones de carrito/producto.

## PENDING

- Prueba dentro de Shopify con productos importados.
- Prueba de imágenes reales, variantes y stock.
- Prueba de checkout y métodos de pago.
- Lighthouse y Core Web Vitals en dominio real.
- Integración webhook con ART³ CONTROL.
- Revisión legal y publicación.

## CATÁLOGO SHOPIFY — VERIFICACIÓN 2026-09-21

- PASS: Matrixify job `#750199575` terminó sin errores: 1 producto nuevo y 2 actualizados.
- PASS: Shopify refleja variantes en los tres productos importados: 7, 7 y 17 variantes respectivamente.
- RESOLVED BY OWNER: Shopify muestra 22 productos porque permanecen 3 registros antiguos de una sola variante para PM-OS-01, PM-OS-03 y PM-OS-04. El propietario confirmó conservarlos; no se eliminarán.
