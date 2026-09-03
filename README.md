# Qualyderm — Web

Sitio web del centro **Qualyderm · Medicina & Estética** (zona Retiro, Madrid).

Web pública de referencia: https://qualyderm.es

## Estructura del proyecto

```
Qualyderm/
├── index.html            → Home (página de inicio). Versión vigente.
├── paginas/              → Páginas interiores (se irán creando y enlazando entre sí)
├── assets/
│   ├── img/              → Imágenes (fotos de tratamientos Qualyderm)
│   └── video/            → qualyderm.mp4
├── borradores/          → Versiones anteriores del diseño (histórico, no publicar)
│   ├── v1-remodelacion.html
│   ├── v2-remodelacion.html
│   └── v3-remodelacion.html   (= copia de index.html)
├── tema-wordpress/       → Tema WordPress "qualyderm" (basado en _s / underscores)
└── README.md
```

## index.html — cómo está montado

- HTML único, autónomo. Ábrelo con doble clic para previsualizarlo.
- CSS y JS embebidos en el propio archivo (`<style>` y `<script>`).
- Tipografías: Google Fonts (Fraunces + Work Sans).
- Hero: imagen `assets/img/hero-inicio.jpg` (titular impreso en la propia imagen). El `<h1>` real vive en `.hero-copy` — oculto (sr-only) en escritorio, visible en móvil.
- Imágenes de las secciones interiores del home: de Unsplash (temporales, sustituir por las de `assets/img/` o la Biblioteca de medios de WordPress).
- Paleta (variables CSS en `:root`): verde `#1E3226`, marfil `#FBF9F5`, rosa `#DBB3A6`, bronce `#AB8B5F`.
- Sistema de reservas: bloque de demostración (widget "Velsy"), sin backend real todavía.

## Secciones de la home (anclas)

`#tratamientos` · `#medicina` · `#reserva` · `#laser` · `#equipo` · `#consulta` · `#contacto`

## Páginas interiores (`paginas/`)

Las páginas de tratamientos comparten estilo mediante `assets/css/interior.css` y
`assets/js/interior.js` (no llevan CSS embebido, a diferencia de `index.html`).
Reutilizan la paleta, tipografías, `<header>` y `<footer>` de la home.

| Archivo                    | Estado | Contenido                                              |
|----------------------------|--------|-------------------------------------------------------|
| `estetica-facial.html`     | ✅     | Área 01 — higiene, hidratación, manchas, RF, HIFU, láser, pestañas… |
| `estetica-corporal.html`   | ✅     | Área 02 — remodelación, grasa localizada, celulitis, reafirmación, antiestrías, depilación láser… |
| `medicina-estetica.html`   | ✅     | Área 03 — líneas de expresión, contorno de ojos/labios, grasa localizada, hiperhidrosis, revitalización capilar |
| `depilacion-laser.html`    | ⬜     | Láser diodo Atenea SFS + IPL SHR (por ahora ancla `#laser` en la home) |
| `equipo.html`              | ⬜     | Estética / medicina / cirugía (SECPRE)                |
| `contacto.html`            | ⬜     | Dirección, teléfonos, mapa, formulario                |

Fuente del contenido de tratamientos: folleto tríptico del centro (Estética Facial /
Estética Corporal / Medicina Estética). Las descripciones cortas están redactadas para
web, sin nombres comerciales de productos y sin promesas de resultado.

La home enlaza a estas páginas desde: la sección `#tratamientos` (3 tarjetas), el
submenú "Tratamientos" del header y la columna "Explora" del footer.

## Contacto del centro

- Dirección: Calle Julio Rey Pastor, Madrid (zona Retiro)
- Teléfonos: 914 33 40 65 · 635 82 96 74
- Email: info@qualyderm.es
- Facebook: facebook.com/qualyderm.medicinaestetica

## Origen de los archivos

Todo provenía de `C:\Users\inmac\Downloads` (`qualyderm-remodelacion*.html`, `qualyderm.zip`,
`qualyderm.mp4`, imágenes `*Qualyderm*.jpg`). Consolidado aquí el 2026-09-02.
