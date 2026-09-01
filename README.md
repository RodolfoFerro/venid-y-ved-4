# Venid y Ved

Sitio de documentación estático hecho con [Jekyll](https://jekyllrb.com) y el tema
[Just the Docs](https://just-the-docs.com), desplegado en GitHub Pages.

## Desarrollo local

Requiere Ruby 3.x y Bundler. Localmente se usa el gem `github-pages`, que fija
Jekyll a la misma versión que usa GitHub (3.10.x).

```bash
bundle install          # instala dependencias
bundle exec jekyll serve   # http://localhost:4000/venid-y-ved-4/
```

Opcional, con recarga automática del navegador:

```bash
bundle exec jekyll serve --livereload
```

## Despliegue

Modo **"Deploy from a branch"**: GitHub compila el Jekyll automáticamente en
cada push a `master`. No hay GitHub Actions.

El tema se carga con `remote_theme` (no con el gem), porque el build de GitHub
Pages corre en modo seguro y sólo admite temas/plugins de su lista blanca.

Configuración necesaria una sola vez en GitHub:
**Settings → Pages → Build and deployment → Source: *Deploy from a branch* →
Branch: `master` / `(root)`**.

## Estructura

| Ruta | Qué es |
|------|--------|
| `_config.yml` | Configuración de Jekyll y del tema (`remote_theme`) |
| `index.md` | Portada |
| `docs/` | Páginas de documentación |
| `_sass/custom/custom.scss` | Estilos propios |
| `_sass/color_schemes/venid.scss` | Esquema de color propio (opcional) |

Más detalles en la sección **Estructura del sitio** de la propia documentación.
