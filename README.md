# 3DS Tile Library

Biblioteca pública de tiles para aplicaciones homebrew de Nintendo 3DS. El repositorio no está vinculado a ningún juego concreto: puedes organizar colecciones para cualquier proyecto cuyas licencias permitan distribuir los recursos.

## Punto de entrada para la 3DS

Tu aplicación puede descargar el catálogo con una petición HTTPS GET a:

```text
https://raw.githubusercontent.com/pedrotobiasbleda/3ds-tile-library/main/catalog.json
```

Cada colección enlazada desde ese archivo tiene su propio `manifest.json`; sus tiles se descargan desde las URL indicadas en el manifiesto.

## Añadir una colección

1. Copia `collections/_template` a `collections/<id-de-la-coleccion>`.
2. Sube tus archivos de imagen a `collections/<id-de-la-coleccion>/tiles/`.
3. Actualiza el `manifest.json` de esa colección con los nombres, tamaños, formato y URL de cada tile.
4. Añade la colección a `catalog.json`.

Usa identificadores estables en minúsculas, por ejemplo `rpg-forest`, `ui-icons` o `platformer-desert`.

## Formatos recomendados

Para 3DS, PNG es el formato de intercambio más cómodo. Para reducir descargas, usa tiles de 8×8, 16×16 o 32×32 píxeles y conserva el tamaño de archivo razonable. La aplicación de 3DS decide después cómo convertir o cargar los datos en VRAM.

## Licencias

Solo publiques recursos propios, de dominio público o cuya licencia permita redistribución. Este repositorio no debe incluir recursos extraídos de juegos comerciales sin autorización.
