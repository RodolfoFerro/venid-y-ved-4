---
title: Empezar
layout: default
nav_order: 2
description: "Requisitos e instrucciones para levantar el sitio en local."
---

# Empezar
{: .no_toc }

## Contenido
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Requisitos

- Ruby 3.x (probado con 3.4.1)
- Bundler (`gem install bundler`)

## Instalación

```bash
bundle install
```

## Servir en local

```bash
bundle exec jekyll serve
```

El sitio queda en <http://localhost:4000/venid-y-ved-4/>. Con `--livereload` se
recarga el navegador al guardar cambios:

```bash
bundle exec jekyll serve --livereload
```

## Build de producción

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

El resultado se genera en `_site/`. En GitHub no hace falta ejecutarlo: al hacer
push a `master`, GitHub Pages compila el sitio automáticamente
("Deploy from a branch").
