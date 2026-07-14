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
├── sass/
│   └── main.scss           # Fuente Sass (se edita ACÁ)
├── styles/
│   └── estilos.css         # CSS compilado por Sass (NO editar a mano)
├── assets/
│   └── img/                # Imágenes y SVGs del sitio
├── package.json            # Scripts de compilación de Sass
└── README.md
```

## Estilos con Sass

El CSS se genera a partir de `sass/main.scss`. **No edites `styles/estilos.css`
a mano** — se sobreescribe en cada compilación. Los `<link>` de las páginas
apuntan a `styles/estilos.css`.

Instalá Sass una vez (global) y usá los scripts:

```bash
npm install -g sass        # si aún no lo tenés

npm run sass               # watch: recompila al guardar main.scss
npm run sass:build         # build único, minificado

# equivalente sin npm:
sass --watch sass/main.scss styles/estilos.css
```

## Cómo verlo

Compilá el Sass (arriba) y abrí `index.html` en el navegador, o serví la carpeta
con un servidor estático para que las rutas relativas funcionen bien:

```bash
python3 -m http.server 8000   # o: npx serve .
```

Luego entrá a `http://localhost:8000`.

## Convenciones

- **Espaciado en CSS, no en HTML.** Toda la separación entre elementos se maneja
  con `gap`, `margin` y `padding`. No se usan etiquetas `<br>` para crear espacio.
- **Fuente única de estilos:** se edita `sass/main.scss`; el resto del sitio usa
  el compilado `styles/estilos.css`.
- **Rutas relativas:** las páginas dentro de `pages/` referencian los recursos con `../`.
- **Imágenes** en `assets/img/`. Los SVGs incluidos son placeholders de ejemplo
  pensados para reemplazarse por imágenes reales.

## Layout

- **Header** con logo y navegación, `sticky` en el tope.
- **Inicio** muestra demos de unidades (px / % / vw) y un contenedor Flexbox.
- **Certificaciones** usa **CSS Grid** con `grid-template-areas`.
- **Responsivo** con breakpoints para mobile (`≤480px`) y laptop/tablet (`≤1024px`).
