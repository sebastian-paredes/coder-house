# Portfolio — Sebastián Paredes

Sitio personal estático construido con **HTML5 y CSS3** como parte del curso de
Desarrollo Web. Es un portafolio multipágina que practica estructura semántica,
Flexbox, Grid y diseño responsivo.

## Estructura del proyecto

```
clase-1/
├── index.html              # Página de inicio (hero + demos de Flexbox)
├── pages/
│   ├── bio.html            # Sobre mí
│   ├── projects.html       # Proyectos
│   ├── certifications.html # Certificaciones (layout con CSS Grid)
│   └── contact.html        # Contacto
├── styles/
│   └── styles.css          # Hoja de estilos única para todo el sitio
├── assets/
│   └── img/                # Imágenes y SVGs del sitio
└── README.md
```

## Cómo verlo

No requiere build ni dependencias. Abrí `index.html` en el navegador, o serví
la carpeta con un servidor estático para que las rutas relativas funcionen bien:

```bash
# Python
python3 -m http.server 8000

# o Node
npx serve .
```

Luego entrá a `http://localhost:8000`.

## Convenciones

- **Espaciado en CSS, no en HTML.** Toda la separación entre elementos se maneja
  con `gap`, `margin` y `padding`. No se usan etiquetas `<br>` para crear espacio.
- **Una sola hoja de estilos** (`styles/styles.css`) compartida por todas las páginas.
- **Rutas relativas:** las páginas dentro de `pages/` referencian los recursos con `../`.
- **Imágenes** en `assets/img/`. Los SVGs incluidos son placeholders de ejemplo
  pensados para reemplazarse por imágenes reales.

## Layout

- **Header** con logo y navegación, `sticky` en el tope.
- **Inicio** muestra demos de unidades (px / % / vw) y un contenedor Flexbox.
- **Certificaciones** usa **CSS Grid** con `grid-template-areas`.
- **Responsivo** con breakpoints para mobile (`≤480px`) y tablet (`481px–978px`).
