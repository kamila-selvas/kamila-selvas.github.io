# Devblog estático — Kamila Selvas

Sitio estático de una sola página con 4 secciones (inicio, últimas entradas, último post, redes) más páginas individuales para cada post. Sin frameworks ni build: HTML y CSS puros, listo para GitHub Pages.

Este sitio está preparado para publicarse en el repositorio especial `kamila-selvas.github.io`, que GitHub sirve directamente en `https://kamila-selvas.github.io/` (sin subcarpeta).

## Estructura

```
index.html                 → página principal (las 4 secciones)
style.css                    → estilos compartidos
*.html (menos index)          → cada entrada del blog
avatar.jpg, thumb-*.svg       → foto e imágenes
robots.txt / sitemap.xml     → SEO técnico
rss.xml                       → feed enlazado en "Redes"
```

## Publicar en GitHub Pages

1. En GitHub, crea un repositorio nuevo llamado exactamente `kamila-selvas.github.io` (público).
2. Sube todo el contenido de esta carpeta a la raíz del repo, en la rama `main`.
3. Ve a **Settings → Pages** y confirma que el **Source** sea la rama `main`, carpeta `/ (root)`.
4. Espera 1–2 minutos. El sitio queda publicado en `https://kamila-selvas.github.io/`.

## Agregar un nuevo post

1. Duplica cualquier archivo dentro de `posts/`.
2. Cambia el título, la fecha (`<time datetime="...">` y `article:published_time`), el contenido y el JSON-LD `BlogPosting`.
3. Añade una entrada nueva en el carrusel de `index.html` (sección `#blog`, dentro de `.post-carousel`), con su propia miniatura en `images/`, y actualiza `#ultimo-post` si es el más reciente.
4. Añade la URL nueva a `sitemap.xml` y `rss.xml`.

## SEO ya incluido

- Meta `description`, `canonical`, Open Graph y Twitter Cards en cada página.
- Datos estructurados JSON-LD (`Person` en inicio, `BlogPosting` en cada post).
- HTML semántico (`header`, `nav`, `main`, `section`, `article`, `time`).
- `robots.txt` + `sitemap.xml`.
- Diseño responsive y accesible (foco visible, `prefers-reduced-motion`).
