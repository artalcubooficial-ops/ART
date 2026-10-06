# Guía de carga Shopify ART³

## 1. Tema

En `Tienda online → Temas → Importar → Subir archivo ZIP`, subir únicamente `ART3_SHOPIFY_THEME_UPLOAD.zip`. No subir el paquete completo como tema: el paquete completo contiene documentación y el tema dentro de otro ZIP.

## 2. Productos

En `Productos → Importar`, subir `products_master.csv`. Mantener `Published=FALSE` durante la revisión. Verificar que Shopify reconoce las opciones de color/talla y que el inventario se carga por SKU.

## 3. Colecciones

Crear colecciones automáticas con las reglas de `data/shopify_collections.csv`. No crear colecciones que no estén respaldadas por el maestro.

## 4. Medios

Subir las imágenes seleccionadas desde `ART3_MEDIA_SHOPIFY` a Shopify Files o asociarlas desde una herramienta de importación que acepte archivos locales. Las rutas `C:\...` no funcionan como `Image Src` públicas.

## 5. Validación antes de publicar

- Revisar producto, precio, SKU, talla, color y stock.
- Confirmar las asociaciones marcadas `REVISAR_ASIGNACION`.
- Configurar pagos, envíos, impuestos y políticas reales.
- Probar carrito y checkout.
- Publicar solo después de aprobar el checklist de pre-lanzamiento.
