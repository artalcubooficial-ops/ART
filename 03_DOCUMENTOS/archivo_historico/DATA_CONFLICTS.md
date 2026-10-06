# Conflictos y diferencias de datos

## Convenciones observadas

| Campo | Fuente A | Fuente B | Decisión |
|---|---|---|---|
| Nombre de modelo | Maestro Excel | Metricool/redes | Se conserva el modelo/código del Excel; el texto de Metricool se usa como descripción comercial cuando coincide. |
| Precio | `MAESTRO DE PRODUCTOS.PRECIO` | Textos sociales | Se usa el precio vigente del Excel; los textos sociales no sustituyen el precio. |
| Stock | `STOCK.STOCK_ACTUAL` | Publicaciones sociales | Se usa `STOCK` y movimientos; una publicación no demuestra disponibilidad actual. |
| Hoodie navy | `PM-OS-06`/`PM-OS-07` | Metricool | Coincidencia provisional con `PM-OS-07`; requiere confirmación antes de publicar. |
| Camiseta esmerilada azul claro | `PM-OS-03` | Metricool | Coincidencia compatible con `PM-OS-03`; se conserva como asociación revisable. |
| Variantes duplicadas | Maestro Excel/CSV | `PM-OS-01` contiene `PM-OS-01-Negro-L` repetido; `PM-OS-03` repite `PM-OS-03-Negro-M`; `PM-OS-04` repite `PM-OS-04-Negro-M` | No se crean variantes duplicadas en Shopify; se conserva una sola fila por SKU y se deja la discrepancia documentada para conciliación de inventario. |
| Stock negativo | Maestro Excel/CSV | `PM-OS-04-Marfil-S` tiene `-1` | No se convierte en stock positivo. Requiere ajuste operativo en ART³ CONTROL antes de habilitar venta de esa variante. |

No se encontraron razones para alterar históricamente los códigos existentes.

## Archivo de conciliación de variantes

Se generaron `data/products_missing_01_03_04_variants_deduped.csv` (31 SKU únicos) y `data/products_missing_01_03_04_variant_conflicts.csv` (9 filas repetidas/conflictivas). El archivo deduplicado conserva la primera fila de cada SKU; las diferencias de inventario no se suman ni se corrigen automáticamente. Deben validarse contra ART³ CONTROL antes de una carga final.
