# Cómo usar el agente de Meta Ads

Ya tienes los creativos hechos (post para todos, story 9:16 para los verticales), así que el agente
**no toca las imágenes**: solo escribe los copys, empareja post + story y te deja la campaña estructurada.

## 1. Prepara los archivos (10 min, una sola vez)
Renombra cada creativo con un código y su formato:

```
C001_post.jpg   C001_story.jpg
C002_post.jpg                     ← sin vertical: irá solo a feed
C003_post.jpg   C003_story.jpg
```

Con esto el agente sabe qué anuncio lleva story y cuál no, sin que se lo expliques.

## 2. Crea el agente en Claude (5 min)
1. claude.ai → **Proyectos** → *Crear proyecto* → "Meta Ads Cornelia".
2. En **Instrucciones**, pega el contenido de [`PROMPT.md`](PROMPT.md) y rellena los `[corchetes]`
   (precio, envío, web, ofertas, edades).
3. En **Conocimiento** del proyecto puedes subir: catálogo/precios, anuncios que ya te funcionaron
   y reseñas reales. El agente las usará como referencia.

## 3. Trabaja por lotes
1. Abre un chat dentro del proyecto y arrastra **10–20 imágenes** (post y story juntas).
2. Escribe solo: `Lote 1`.
3. Te devuelve la tabla CSV + resumen + incidencias.
4. Corrige lo que no te guste ("más corto", "menos emoción") — lo aplica al resto.
5. Primer lote de prueba: 5 creativos variados. Cuando te guste el resultado, sigue con el resto.

## 4. Súbelo a Meta
**Opción rápida (recomendada para empezar):** en el Administrador de anuncios crea la campaña y un
conjunto por grupo; dentro, crea el primer anuncio, y para los demás usa *Duplicar* y pega los textos
de la tabla. En los anuncios con story, activa *Personalizar recursos por ubicación* y asigna la
imagen `_story` a Stories y Reels.

**Opción masiva:** Administrador de anuncios → *Exportar/Importar* → descarga la plantilla de
importación de Meta y copia las columnas de la tabla del agente (texto, título, descripción, CTA, URL,
nombres). Las imágenes se suben antes a la *Biblioteca multimedia*.

## Archivos
- `PROMPT.md` — instrucciones del agente.
- `plantilla-anuncios.csv` — ejemplo del formato de salida.
