---
title: Inicio
layout: home
nav_order: 1
description: "Página principal de la documentación de Venid y Ved 4."
permalink: /
---

# Venid y Ved 4
{: .fs-9 }

Documentación del proyecto, construida con [Jekyll](https://jekyllrb.com) y el tema
[Just the Docs](https://just-the-docs.com), desplegada en GitHub Pages.
{: .fs-6 .fw-300 }

[Empezar]({% link docs/inicio.md %}){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Ver en GitHub](https://github.com/rodolfoferro/venid-y-ved-4){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Cómo trabajar en local

```bash
bundle install        # instala las dependencias
bundle exec jekyll serve   # levanta el sitio en http://localhost:4000/venid-y-ved-4/
```

## Estructura del contenido

- La navegación lateral se genera a partir del front matter (`nav_order`, `parent`, `has_children`) de cada archivo.
- Las páginas viven como `.md` en la raíz o dentro de `docs/`.
- Consulta la [guía de estructura]({% link docs/estructura.md %}) para agregar secciones nuevas.
