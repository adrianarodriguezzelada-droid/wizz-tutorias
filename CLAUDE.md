# Wizz Tutorías — web para padres

Landing de Wizz Tutorías (tutorías 1:1 online para secundaria, Pre-IB y Programa IB, Latinoamérica). Esta primera página está escrita para **padres**. La página para estudiantes se hará después.

## Estructura
- `index.html`: página completa (HTML + CSS + JS en un solo archivo).
- `assets/img/logo-wizz.png`: logo con fondo transparente (en modo oscuro se invierte por CSS).
- `assets/img/tutores/tutor-01.jpg … tutor-06.jpg`: fotos REALES de tutores, recortadas 4:5 a la máxima resolución que permite cada original (560–1024 px de ancho), con el mismo tono cálido. Los originales sin editar están en `assets/img/tutores/originales/`; si llega una versión de mejor calidad, se recorta y edita igual.
- `assets/img/escenas/`: imágenes de ambiente (IMG-01, IMG-02, IMG-03).
- `assets/video/`: videos (VID-01, VID-02).

## Reglas de diseño (no cambiar sin preguntar)
- Colores: base crema `#F6F1EB`, texto negro `#141413`, acento azul tinta `#1E3A5F`. Están definidos como tokens en `:root`, con modo oscuro.
- Una sola familia tipográfica: Geist (Google Fonts) y Geist Mono para etiquetas pequeñas.
- Texto de cuerpo entre 16 y 18 px.
- Espaciado de 8 en 8 px (tokens `--s1` … `--s24`).
- Composición asimétrica alineada a la izquierda (no centrar todo), con estilo editorial europeo y mucho aire entre frases.

## Reglas de contenido
- No inventar testimonios, cifras de alumnos, resultados, porcentajes, precios ni funciones que no existan.
- Dato real que sí se puede usar: más de 7 años en el mercado.
- No generar tutores con IA. Las fotos de tutores son siempre reales y con el permiso de cada tutor.
- Se tutea al papá o a la mamá ("tu hijo").

## Espacios de medios pendientes
Cada espacio pendiente es un `<figure class="media">` con una etiqueta (`.tag`):
- IMG-01 (4:5) → `assets/img/escenas/img-01.jpg`
- IMG-02 (3:1) → `assets/img/escenas/img-02.jpg`
- IMG-03 (4:5) → `assets/img/escenas/img-03.jpg`
- VID-02 (4:5) → `assets/video/vid-02.mp4`
- Opcional: `assets/video/vid-01.mp4` (clip de ambiente, sin caras) intercalado en la franja de tutores.

Cuando exista el archivo, reemplaza el placeholder por `<img>` o `<video autoplay muted loop playsinline>` con `object-fit: cover`, manteniendo la proporción.

## Pendientes
- Nombre y materia de cada tutor (hoy dice "Tutor/a Wizz" y "Materia").
- Conectar el formulario `#lead` a un destino real.
- Publicar la página y conectarla al dominio.
