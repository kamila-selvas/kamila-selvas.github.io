# Devblog estático

Sitio estático de una sola página con 4 secciones (inicio, últimas entradas, último post, redes) más páginas individuales para cada post. Sin frameworks ni build: HTML y CSS puros, listo para GitHub Pages.

## Estructura

```
index.html                 → página principal (las 4 secciones)
css/style.css               → estilos compartidos
posts/*.html                 → cada entrada del blog
images/avatar.svg            → placeholder de foto, reemplázalo
robots.txt / sitemap.xml     → SEO técnico
rss.xml                       → feed enlazado en "Redes"
```

## Antes de publicar: reemplaza estos datos

Búscalos y cámbialos en **todos** los archivos `.html`:

- `Kamila Selvas` → tu nombre real
- `kamila-selvas` / `tu-repo` → tu usuario y nombre de repositorio de GitHub
- `kamilaselvas@gmail.com`, enlaces de GitHub/LinkedIn/X → tus redes reales
- `images/avatar.svg` → sube tu foto (ej. `avatar.jpg`) y actualiza el `src` en `index.html`

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub y sube todo el contenido de esta carpeta a la raíz del repo (o a una rama `main`).
2. En GitHub: **Settings → Pages → Source**, selecciona la rama `main` y la carpeta `/ (root)`.
3. Espera 1–2 minutos. Tu sitio quedará publicado en `https://kamila-selvas.github.io/tu-repo/`.
4. Actualiza las URLs de `sitemap.xml`, `robots.txt` y las etiquetas `canonical`/`og:url` en cada HTML con tu dominio real.

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
