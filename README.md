# ✎ Pizarra DIY

Una pizarra digital minimalista para móvil, pensada para usar con **lápiz capacitivo común** en Android. Sin dependencias, sin servidor, sin instalación — un solo archivo HTML.

## ¿Qué hace?

- Dibuja con el dedo o lápiz capacitivo
- Tres tipos de fondo: **Lisa**, **Rayada** (cuaderno) y **Pentagrama** (música)
- Selector de **grosor** (fino / medio / grueso)
- Selector de **color**
- Modo **goma de borrar**
- Se adapta a cualquier tamaño de pantalla
- Funciona offline, sin internet

## Uso

1. Descargá `pizarra_diy.html`
2. Abrilo desde el explorador de archivos del celu
3. Listo

No requiere instalación ni servidor local.

## Compatibilidad

Probado en **Motorola Moto G15** (Android). Funciona en cualquier navegador moderno (Chrome, Firefox, Edge). Optimizado para táctil con Pointer Events API — también soporta presión si el lápiz es activo.

## Técnico

- HTML + CSS + Canvas API puro
- Dos capas canvas: fondo (`bgLayer`) + dibujo (`drawCanvas`) — esto resuelve el bug clásico donde el fondo desaparece al redimensionar
- `touch-action: none` + `stopPropagation` en los controles para que los botones no interfieran con el canvas
- Borrado real con `globalCompositeOperation: destination-out`

## Licencia

MIT — hacé lo que quieras.
