# ART³ — Modelo de datos

## Fuente de verdad

El catálogo se generó desde la base operativa de ART³ CONTROL y el maestro de productos. Shopify recibe únicamente datos comerciales; la información privada de clientes, pedidos, cobros y gastos permanece fuera del frontend.

## Entidades

| Entidad | Identificador | Uso |
|---|---|---|
| Producto comercial | `PM-OS-01` … `PM-OS-19` | Referencia de la prenda base/modelo |
| Variante | SKU del maestro | Combinación de color y talla con precio e inventario |
| Diseño ART³ | Por clasificar | Arte/estampado; no se confunde con la referencia de prenda |
| Colección | Handle de Shopify | Agrupación navegable por familia o lanzamiento |
| Medio | SHA-256 y ruta original | Fotografía o video; requiere mapeo antes de publicarse |

## Estado actual verificado

- 19 referencias comerciales.
- 96 filas de variantes en `data/products_master_SHOPIFY_LISTO.csv`.
- 1.512 imágenes inventariadas en `data/media_manifest.json`.
- Familias detectadas en el maestro: Oversize (7), Camiseta (5), Buzo (4) y Esqueleto (3).
- Precios, colores, tallas y existencias se conservan desde la fuente operativa; no se rellenan valores ausentes.

## Mapeo Shopify

- `Handle`: referencia estable del producto.
- `Title`, `Body (HTML)`, `Vendor`, `Type`, `Tags`: presentación comercial.
- `Variant SKU`, `Option1`, `Option2`, `Variant Price`, `Variant Inventory Qty`: variante operativa.
- Imágenes: se mantienen fuera del CSV de importación hasta contar con URLs públicas y una asociación confirmada; las rutas locales no son válidas para Shopify.

## Metafields previstos

`custom.art3_reference`, `custom.fit`, `custom.grammage`, `custom.fabric`, `custom.print_type`, `custom.care`, `custom.size_guide`, `custom.design_code`, `custom.collection_name`, `custom.gender`, `custom.photography_group`.

Los metafields que no estén respaldados por la base o por una ficha aprobada quedan pendientes y no se muestran como hechos.

## Reglas de integridad

1. No duplicar una referencia por cada fotografía.
2. No publicar una variante sin SKU, precio y stock verificados.
3. No publicar fotografías con producto, diseño o derechos sin confirmar.
4. Los movimientos de inventario se realizan en ART³ CONTROL/Shopify según la integración aprobada, nunca editando históricos manualmente.
