# Fase 0 — Descubrimiento ART³ Shopify

Fecha de revisión: 2026-09-21

## Fuentes identificadas

- `Backup BASE CENTRA DE ART  V1 14092026.xlsx`: fuente operativa local revisada. Contiene `MAESTRO DE PRODUCTOS`, `STOCK`, `ENTRADASYSALIDAS`, `INVENTARIO`, `REGISTRO`, `Pedidos`, `Clientes`, `Producción`, `Gastos`, `LISTAS` y otras hojas.
- `catalogo_shopify_ART3_MEJORADO.csv`: exportación preparada para Shopify, todavía no publicada.
- `ART3_PRODUCT_MEDIA_MAPPING.csv`: asociación preliminar de códigos con carpetas de medios.
- `ROPA.zip`: biblioteca entregada por el usuario. Fue extraída a `ropa_art_assets` y organizada en `ART3_MEDIA_SHOPIFY`.
- Metricool: marca `ART al Cubo`, TikTok `@art.al.cubo`, Instagram `artalcubooficial`. Se observaron publicaciones de hoodie navy y camiseta esmerilada azul claro.
- Código operativo ART³: numerosos `.gs`, `.js`, `.ps1`, reportes y pruebas relacionados con ventas, stock, producción y finanzas.
- Tema Shopify preliminar: `shopify_art3_theme`, todavía candidato no publicado.

## Inventario de archivos

El inventario recursivo actual contiene aproximadamente 4.980 archivos, incluyendo 1.680 PNG, 1.344 JPG/JPEG, 290 MP4, 641 Apps Script, 307 JavaScript, 228 Markdown, 22 Excel y 42 ZIP. Parte de este recuento incluye históricos, backups y la extracción de medios.

## Datos verificados

- Maestro: 19 referencias de producto.
- Stock: 94 variantes con registro de stock no vacío; el exportador Shopify conserva además filas de producto sin variante para evitar perder referencias del maestro.
- Catálogo Shopify preparado: 19 productos y 96 filas de variante/exportación.
- Precio comercial tomado de `PRECIO`/`PRECIO_REAL`, no del costo interno.
- Costos y datos operativos no se exponen en la tienda.

## Bloqueos actuales

- La carpeta de trabajo no contiene un repositorio Git detectable; por eso no fue posible crear branch ni usar historial Git como backup. Los archivos históricos existentes se conservaron y los entregables se generaron en archivos nuevos.
- La sesión de Shopify requiere autenticación humana y la carga/publicación final debe hacerla el propietario o un colaborador autorizado.
- Las imágenes locales necesitan cargarse a Shopify Files o asociarse mediante URLs públicas antes de que `Image Src` funcione en una importación CSV.
- No se inventan códigos de diseño, medidas, políticas legales, datos tributarios, métodos de pago ni valores de envío.

## Próximo trabajo

1. Consolidar el manifiesto de medios y separar imágenes mapeadas de `UNMAPPED`.
2. Completar la arquitectura de catálogo y metafields.
3. Ampliar el tema Online Store 2.0 con PDP, búsqueda, colecciones, carrito y páginas de contenido.
4. Preparar la importación Shopify y documentar los pasos humanos restantes.
