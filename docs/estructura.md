---
title: Estructura del sitio
layout: default
nav_order: 3
description: "Cómo se organizan los archivos y cómo agregar páginas nuevas."
---

# Estructura del sitio
{: .no_toc }

## Contenido
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Árbol de archivos

```text
.
├── _config.yml            # configuración de Jekyll y del tema
├── Gemfile                # dependencias Ruby
├── index.md               # portada (layout: home)
├── docs/                  # páginas de documentación
│   ├── inicio.md
│   ├── estructura.md
│   └── componentes/       # sección con subpáginas
│       ├── index.md
│       └── botones.md
└── _sass/
    ├── custom/
    │   └── custom.scss    # reglas Sass propias (el tema lo importa solo)
    └── color_schemes/
        └── venid.scss     # esquema de color propio (opcional)
```

El tema no está en el repo: se descarga en cada build vía `remote_theme` en
`_config.yml`. El despliegue lo hace GitHub Pages compilando la rama `master`.

## Agregar una página

Crea un archivo `.md` con front matter:

```yaml
---
title: Mi página
layout: default
nav_order: 4
---
```

## Crear una sección con subpáginas

1. Crea una carpeta, p. ej. `docs/api/`.
2. Añade `docs/api/index.md` con `has_children: true`.
3. En cada subpágina pon `parent: <title del index>`.

```yaml
# docs/api/index.md
---
title: API
layout: default
nav_order: 5
has_children: true
---
```

```yaml
# docs/api/autenticacion.md
---
title: Autenticación
layout: default
parent: API
nav_order: 1
---
```

## Personalizar estilos

Reglas Sass adicionales van en `_sass/custom/custom.scss` (el tema lo importa
automáticamente). Para cambiar colores del tema, edita el esquema
`_sass/color_schemes/venid.scss` y actívalo con `color_scheme: venid` en
`_config.yml`.
