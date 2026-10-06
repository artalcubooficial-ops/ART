# Auditoría de estado ART³ — 2026-09-22

## Shopify verificado

- Tienda: `1101kw-m7.myshopify.com`.
- Tema publicado: `Horizon`, ID `201689268305`.
- Tema borrador con carrusel ART³: `art3-shopify-theme-variant-carousel`, ID `201739894865`.
- Producto auditado: `Boxy fit PM-OS-04`, ID `16325511577681`.
- Variantes verificadas: Beige/M; Marfil/L, M, S; Negro/L, M, S.
- Imágenes multimedia cargadas en Shopify.
- Imágenes asignadas a los grupos de variantes Marfil y Negro.
- La política de inventario para venta por encargo fue activada en las variantes auditadas.

## Hallazgo principal

El tema Horizon publicado muestra toda la multimedia del producto en un único carrusel, aunque el cliente cambie de color. Por eso la selección Marfil puede seguir mostrando una imagen negra.

El tema borrador `art3-shopify-theme-variant-carousel` contiene lógica Liquid/JavaScript de filtrado por alias de color, pero su vista previa actual solo encuentra las imágenes Beige porque los nombres/ALT de las imágenes de Marfil y Negro no contienen aliases confiables.

## Corrección requerida

1. Normalizar los ALT de las imágenes de producto con el color real, o usar la relación de media de cada variante como fuente primaria.
2. Ajustar la galería del tema borrador para filtrar por la media asociada al `selected_or_first_available_variant`, con fallback por ALT.
3. Probar Beige, Marfil y Negro en escritorio y móvil.
4. Publicar solo después de autorización explícita y QA.

## Bloqueadores no inventados

- No se publica el tema borrador automáticamente.
- Checkout, pagos, dominio, datos legales y píxeles requieren revisión/configuración del propietario.
