# ✎ Pizarra DIY

Una pizarra digital minimalista para móvil, pensada para usar con **lápiz capacitivo de punta disco** en Android. Sin servidor, sin instalación — un solo archivo HTML.

## ¿Qué hace?

- Dibuja con el dedo o lápiz capacitivo
- Tres tipos de fondo: **Lisa**, **Rayada** (cuaderno) y **♪ Pentagrama** (música)
- Selector de **grosor** (fino / medio / grueso)
- Selector de **color**
- Modo **goma de borrar**
- **OCR** — reconoce texto manuscrito y lo exporta como .txt o portapapeles
- Se adapta a cualquier tamaño de pantalla
- Funciona offline (excepto la primera vez que usás el OCR)

## Uso

1. Descargá `index.html`
2. Abrilo desde el explorador de archivos del celu
3. Listo

No requiere instalación ni servidor local.

## OCR

Usa [Tesseract.js](https://tesseract.js.org/) con modelo en español. La primera vez descarga el modelo (~10MB), necesitás internet. Después funciona offline. Funciona mejor con letra de imprenta clara.

## Compatibilidad

Probado en **Motorola Moto G15** (Android) con lápiz capacitivo de punta disco. Funciona en cualquier navegador moderno (Chrome, Firefox, Edge).

## Técnico

- HTML5 + CSS + Canvas API + Pointer Events API — sin frameworks, sin dependencias propias
- Dos capas canvas: `bgLayer` (fondo) + `drawCanvas` (trazos) — resuelve el bug de pérdida de fondo al redimensionar
- `touch-action: none` + `stopPropagation` en controles para evitar que los botones disparen trazos
- `globalCompositeOperation: destination-out` para borrado real de píxeles
- Soporte de presión via `e.pressure` para lápices activos
- OCR con Tesseract.js v5, imagen preprocesada sobre fondo blanco antes del reconocimiento

## Licencia

MIT — hacé lo que quieras.
