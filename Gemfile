source "https://rubygems.org"

# GitHub Pages en modo "Deploy from a branch": usamos exactamente el mismo
# conjunto de gemas (y versión de Jekyll) que compila GitHub, en modo seguro.
gem "github-pages", "~> 232", group: :jekyll_plugins

# Plugins soportados por GitHub Pages que sí queremos activos.
group :jekyll_plugins do
  gem "jekyll-remote-theme"
  gem "jekyll-include-cache"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Servidor local para Ruby 3.x (Jekyll 3.x no lo trae).
gem "webrick", "~> 1.9"

# Ajustes de compatibilidad por plataforma.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.2.0", platforms: [:mingw, :x64_mingw, :mswin]
