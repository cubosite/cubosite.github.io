---
name: Cubosite Builder
description: Manual técnico y estándar de contenido para Cubosite, el blog estático en Astro con estética Dark y gestión mediante Markdown.
---

# 🧊 SKILL: Cubosite Content & Architecture

## 1. Identidad Visual y Estética (Dark Theme)
Cubosite utiliza un diseño minimalista oscuro basado en variables CSS estrictas. No se deben romper estos valores en ningún componente:
- **Fondo base (`--bg-base`):** `#030712` (Negro profundo)
- **Fondo de tarjetas (`--bg-card`):** `#111827` (Azul grisáceo oscuro)
- **Bordes (`--border-color`):** `#1e293b`
- **Texto principal (`--text-main`):** `#f8fafc` (Blanco brillante)
- **Texto secundario (`--text-muted`):** `#94a3b8`
- **Acento (`--accent`):** `#38bdf8` (Azul cian brillante con efectos de brillo sutiles)
- **Tipografía:** *Inter* en todo el sitio.

---

## 2. Estándar de Contenido (Archivos Markdown `.md`)
Todas las publicaciones deben ubicarse obligatoriamente en la ruta `src/content/posts/` y seguir estrictamente esta estructura de Frontmatter:

```markdown
---
title: "Título llamativo del post"
date: YYYY-MM-DD
category: "Peliculas" | "Videos" | "Articulos" | "Noticias"
description: "Breve resumen de 1 o 2 líneas que aparecerá en la tarjeta de la página principal."
---

Aquí va el contenido completo del artículo o reseña en Markdown.
