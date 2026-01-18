# Christian Sánchez - Abogado Laboralista

Sitio web profesional para Christian Sánchez, abogado especializado en derecho laboral y argumentación jurídica.

## Tecnologías

- **Hugo** - Generador de sitios estáticos
- **PaperMod** - Tema de Hugo
- **Netlify** - Hosting y despliegue

## Desarrollo Local

```bash
# Clonar el repositorio
git clone [url-del-repo]
cd christian-sanchez-abogado

# Inicializar submodulos (tema)
git submodule update --init --recursive

# Iniciar servidor de desarrollo
hugo server -D
```

El sitio estará disponible en `http://localhost:1313`

## Estructura

```
christian-sanchez-abogado/
├── content/
│   ├── _index.md          # Página de inicio
│   ├── about.md           # Sobre mí
│   ├── services.md        # Servicios
│   ├── contact.md         # Contacto
│   ├── blog/              # Artículos del blog
│   └── publications/      # Publicaciones académicas
├── assets/css/extended/   # Estilos personalizados
├── layouts/partials/      # Componentes personalizados
├── static/                # Archivos estáticos
└── hugo.toml              # Configuración
```

## Agregar Contenido

### Nuevo Post de Blog

```bash
hugo new blog/mi-nuevo-post.md
```

O crear manualmente en `content/blog/`:

```yaml
---
title: "Título del Post"
date: 2026-01-17
description: "Descripción breve"
tags: ["tag1", "tag2"]
categories: ["Categoría"]
author: "Christian Sánchez"
draft: false
---

Contenido del post en Markdown...
```

### Nueva Publicación

Mismo proceso en `content/publications/`

## Despliegue

El sitio se despliega automáticamente en Netlify cuando se hace push a la rama principal.

## Personalización

### Colores

Editar `assets/css/extended/custom.css`:

```css
:root {
    --primary-blue: #1a365d;
    --secondary-gold: #c9a227;
}
```

### Información de Contacto

Editar `hugo.toml` para actualizar:
- URL base
- Redes sociales
- Información del sitio

## Licencia

Todos los derechos reservados © Christian Sánchez
