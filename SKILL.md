---
name: Cubosite Builder
description: Manual técnico y estándar de contenido para Cubosite, el blog estático en Astro con estética Dark y gestión mediante Markdown.
---

# 🧊 SKILL: Cubosite Content & Architecture

## 1. Identidad Visual y Estética (Dark Theme)
Cubosite utiliza un diseño minimalista oscuro basado en variables CSS estrictas:
- **Fondo base (`--bg-base`):** `#030712`
- **Fondo de tarjetas (`--bg-card`):** `#111827`
- **Bordes (`--border-color`):** `#1e293b`
- **Texto principal (`--text-main`):** `#f8fafc`
- **Acento (`--accent`):** `#38bdf8`
- **Tipografía:** *Inter* en todo el sitio.

---

## 2. Estándar de Contenido (`src/content/posts/*.md`)
Toda publicación debe seguir esta estructura exacta en su Frontmatter:

```markdown
---
title: "Título del post"
date: YYYY-MM-DD
category: "Peliculas" | "Videos" | "Articulos" | "Noticias"
description: "Resumen corto para la tarjeta principal."
---
