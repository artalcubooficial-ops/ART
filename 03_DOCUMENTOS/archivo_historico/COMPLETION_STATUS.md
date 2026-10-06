# Estado de entrega ART³ Shopify

## Verificado

- Catálogo operativo en Shopify con 22 productos visibles.
- Variantes importadas mediante Matrixify, sin errores en el trabajo `#750199575`.
- Productos importados con 7, 7 y 17 variantes para PM-OS-01, PM-OS-04 y PM-OS-03.
- Tres registros históricos de una sola variante conservados por decisión del propietario.
- Tema Online Store 2.0 preparado en `ART3_SHOPIFY_THEME_UPLOAD.zip`.
- Home, catálogo, producto, búsqueda, páginas de contenido y carrito incluidos en el tema.
- Carrito lateral, carrito completo y checkout nativo implementados.
- Galería de producto multiimagen con miniaturas, ALT y carga diferida.
- Inventario multimedia generado en `data/media_manifest.json`.

## Pendiente antes de publicar

- Subir el ZIP actualizado al tema borrador de Shopify.
- Verificar imágenes reales en cada producto.
- Configurar y revisar colecciones comerciales.
- Probar checkout y métodos de pago reales.
- Configurar datos legales, dominio y analítica/píxeles.
- Ejecutar QA móvil y escritorio en el tema cargado.
- Publicar solo después de autorización explícita.

## Última revisión técnica (2026-09-21)

- Validación del paquete: PASS. Todos los JSON de plantillas son válidos; el ZIP contiene `layout/theme.liquid` y 20 entradas.
- Catálogo y variantes: PASS según Matrixify `#750199575` (1 nuevo, 2 actualizados, 0 errores).
- Duplicados históricos: conservados intencionalmente por decisión del propietario.
- Colecciones: no se guardaron colecciones vacías o engañosas; el editor exige seleccionar atributos y valores reales en Shopify.
