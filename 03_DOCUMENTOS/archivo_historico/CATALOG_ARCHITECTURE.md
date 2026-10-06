# Arquitectura de catálogo ART³

## Regla principal

Una referencia de prenda (`PM-OS-01` … `PM-OS-19`) no es lo mismo que un diseño gráfico. La referencia identifica la base/modelo y sus combinaciones de color y talla. El diseño identifica el arte o estampado que puede aplicarse a una base.

## Shopify

- Producto: combinación comercial de modelo/base + diseño confirmado.
- Variante: color + talla + SKU + precio + inventario.
- Metafields previstos: `custom.art3_reference`, `custom.fit`, `custom.grammage`, `custom.fabric`, `custom.print_type`, `custom.care`, `custom.size_guide`, `custom.design_code`, `custom.collection_name`, `custom.gender`, `custom.photography_group`.
- Tags: familia de prenda, clasificación, colección confirmada y estado de disponibilidad.
- Colecciones: se crearán solo cuando existan referencias reales en el maestro.

## Fuente de verdad

Excel ART³ CONTROL es la fuente de códigos, precios y stock inicial. Metricool y las carpetas de medios sirven para naming, storytelling y material visual. No se reemplaza el identificador del Excel por nombres de redes.

## Privacidad

Clientes, teléfonos, direcciones, costos, márgenes, gastos y datos financieros permanecen fuera del frontend y del CSV público.

## Regla de asociación de medios

Una imagen se asigna automáticamente solo cuando el código o la coincidencia de modelo/diseño es suficientemente clara. El resto queda `UNMAPPED` o `REQUIERE_REVISION`; no se fuerza una asociación.
