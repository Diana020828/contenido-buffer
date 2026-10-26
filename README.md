# contenido-buffer

Hosting público de las imágenes que se publican por la API de Buffer.

Buffer no acepta rutas locales ni archivos: `create_post` solo recibe `assets[].url` con una
URL pública descargable. Este repo existe para eso, nada más. No es un sitio web.

## URL de un archivo

```
https://raw.githubusercontent.com/Diana020828/contenido-buffer/main/<cuenta>/<pieza>/<archivo>.png
```

## Estructura

    vulcano/
      carrusel-01-inventario/     01..08.png + linkedin-v2.pdf
      carrusel-02-facturacion/    01..08.png + linkedin-v2.pdf
      carrusel-03-tablero-comercial/
      carrusel-04-tutores/
      carrusel-05-senales/
      radar-01-php2shell/         01..08.png + linkedin-v2.pdf
    diana/
      semana-2026-10-26/          una imagen por pieza

Cada cuenta va en su carpeta, `vulcano/` y `diana/`, para que las piezas de una marca nunca se
mezclen con las de la otra.

## Reglas

- Solo imágenes finales. La fuente editable vive en
  `OneDrive\Documents\contenido\VULCANO\_fuente` y no se sube aquí.
- No renombrar ni reordenar archivos ya publicados: las URLs quedan dentro de posts de Buffer
  programados y se rompen si el archivo cambia de ruta.
- Si se corrige una pieza ya publicada o programada, se sube con un nombre nuevo (`-v2`) y se
  actualiza el asset del post en Buffer. Así el CDN no devuelve la versión vieja.
- Tamaño: las piezas de carrusel son 1080×1350 px (4:5).
