# Wizz Tutorías — web para padres

Landing de Wizz Tutorías (tutorías 1:1 online para secundaria, Pre-IB y Programa IB, Latinoamérica). Esta primera página está escrita para **padres**. La página para estudiantes se hará después.

## Estado actual (octubre 2026)

### Publicado
- **GitHub repo**: https://github.com/adrianarodriguezzelada-droid/wizz-tutorias
- **GitHub Pages**: https://adrianarodriguezzelada-droid.github.io/wizz-tutorias/
- **GitHub account**: `adrianarodriguezzelada-droid` (autenticado via `gh auth`)
- **Branch de deploy**: `master`, source `/` (GitHub Pages legacy build)

### Formulario de inscripción
- Conectado a **Formsubmit.co** → envía a `adriana.rodriguez.zelada@gmail.com`
- La primera vez que alguien envíe el formulario, llegará un **email de confirmación de Formsubmit** que hay que aceptar para activar la recepción.
- Campos: nombre, WhatsApp, email, programa, materia, nota opcional.
- Envío por AJAX con mensaje de éxito inline (no redirige a otra página).

### Tutores registrados (del spreadsheet)
Solo se usa el primer nombre (sin apellido). Los cursos se cargan dinámicamente desde el Google Sheet (columna E "¿Qué cursos puedes enseñar?").
Asignación foto → tutor (verificada oct 2026):
- `tutor-01.jpg` → **Samira**
- `tutor-02.jpg` → **Sebastián** (registrado como "Sergio Sebastián" en el sheet)
- `tutor-03.jpg` → **Alexandra**
- `tutor-04.jpg` → **Álvaro**
- `tutor-05.jpg` → **Matías**
- `tutor-06.jpg` → **Santiago**

**Spreadsheet de horarios**: https://docs.google.com/spreadsheets/d/1YXIuTiIJqlhCss4Ra6J1VWurS42e6Q1FENe8pL-HmeQ/edit?gid=1630250331#gid=1630250331

### Imágenes colocadas
Todas las imágenes de `Imagenes/` (generadas con Gemini) ya están copiadas y funcionando:
- `assets/img/escenas/img-01.jpg` — madre con hijo estudiando (sección experiencia, 4:5)
- `assets/img/escenas/img-02.jpg` — escritorio panorámico IB (sección divisora, 3:1)
- `assets/img/escenas/img-03.jpg` — estudiante concentrada (sección materias, 4:5)
- `assets/video/vid-01.mp4` — video ambiente (sección cómo funciona)

## Estructura
- `index.html`: página completa (HTML + CSS + JS en un solo archivo).
- `assets/img/logo-wizz.png`: logo con fondo transparente (en modo oscuro se invierte por CSS).
- `assets/img/tutores/tutor-01.jpg … tutor-06.jpg`: fotos REALES de tutores, recortadas 4:5. Los originales están en `assets/img/tutores/originales/`.
- `assets/img/escenas/`: imágenes de ambiente (img-01, img-02, img-03).
- `assets/video/`: vid-01.mp4 (clip de ambiente).
- `Imagenes/`: carpeta original con archivos fuente (no se sube a git, son duplicados).
- `.claude/launch.json`: config del dev server local (`npx serve` en puerto 3000).

## Reglas de diseño (no cambiar sin preguntar)
- Colores: base crema/beige `#F6F1EB`, texto negro `#141413`, acento azul tinta `#1E3A5F`. Forzado a modo claro (`data-theme="light"`). Las secciones `.brand` y `.cta` usan el azul `#1E3A5F` como fondo de contraste.
- Una sola familia tipográfica: Geist (Google Fonts) y Geist Mono para etiquetas pequeñas.
- Texto de cuerpo entre 16 y 18 px.
- Espaciado de 8 en 8 px (tokens `--s1` … `--s24`).
- Composición asimétrica alineada a la izquierda (no centrar todo), con estilo editorial europeo y mucho aire entre frases.

## Reglas de contenido
- No inventar testimonios, cifras de alumnos, resultados, porcentajes, precios ni funciones que no existan.
- Dato real que sí se puede usar: más de 7 años en el mercado.
- No generar tutores con IA. Las fotos de tutores son siempre reales y con el permiso de cada tutor.
- Se tutea al papá o a la mamá ("tu hijo").
- Solo poner el primer nombre del tutor, nunca apellido.
- El contacto es directo con Wizz, no con el tutor.

## Pendientes (próxima sesión)

### Prioridad alta
- [ ] **Conectar dominio GoDaddy**: La web está en GitHub Pages. Falta ir a GoDaddy y apuntar el dominio con registros DNS:
  - Registro `A` apuntando a `185.199.108.153` (y los otros 3 IPs de GitHub Pages)
  - Registro `CNAME` para `www` → `adrianarodriguezzelada-droid.github.io`
  - En el repo de GitHub: Settings → Pages → Custom domain → poner el dominio
- [ ] **Confirmar Formsubmit**: Enviar un test del formulario y confirmar el email de activación de Formsubmit.co.
- [x] **Verificar asignación foto-tutor**: Corregido oct 2026. Fotos reasignadas correctamente.

### Prioridad media
- [ ] Sistema de usuarios: que los padres creen usuario/contraseña y escojan clase según horarios de tutores.
- [ ] Integrar horarios del spreadsheet de Google Sheets para que los padres vean disponibilidad.
- [ ] Mejoras estéticas de la landing.
- [ ] Página para estudiantes.

### Prioridad baja
- [ ] Conectar formulario a CRM o WhatsApp Business API.
- [ ] Video vid-02 (si llega) para reemplazar vid-01 en la sección "Cómo funciona".
