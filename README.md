# Sitio de marca personal — Juan Manuel Bejarano Morales

Sitio web profesional listo para publicarse, gratis, en Netlify.

---

## ¿Qué hay en este paquete?

```
sitio/
├── index.html                    Página principal
├── articulos/                    Los 6 artículos publicados (HTML)
│   ├── espejismo-crecimiento-bolivia.html
│   ├── oficio-decidir-incertidumbre.html
│   ├── ciclo-conversion-efectivo.html
│   ├── crecer-no-es-escalar.html
│   ├── posicionar-es-renunciar.html
│   └── reestructurar-antes-crisis.html
├── assets/
│   └── style.css                 Hoja de estilos (paleta crema-navy-dorado)
├── img/
│   ├── articulos/                (vacía — para imágenes futuras)
│   └── LEEME-foto-perfil.txt     Instrucciones para tu foto
├── content/articulos/            Mismos artículos en formato Markdown
│   └── (6 archivos .md)            (para edición desde el panel CMS opcional)
├── admin/                        Panel de administración Decap CMS
│   ├── index.html
│   └── config.yml
├── _data/                        Textos editables del home
│   ├── sitio.yml
│   └── cita.yml
├── netlify.toml                  Configuración de Netlify
├── _redirects                    Reglas de redirección
└── README.md                     Este archivo
```

---

## PARTE 1 — Publicar el sitio en Netlify (30 minutos)

Esta parte la haces UNA sola vez. Después tu sitio queda en línea para siempre.

### Paso 1. Crear cuenta en GitHub

1. Entra a **https://github.com**
2. Clic en **Sign up**
3. Usa tu correo profesional. Elige un nombre de usuario corto (ej: `jmbejarano`).
4. Verifica el correo y entra.

GitHub es donde vivirá el código de tu sitio. Es gratis para siempre.

### Paso 2. Crear el repositorio

1. Una vez dentro de GitHub, clic en el botón verde **New** (arriba a la izquierda) o ve a https://github.com/new
2. Llena así:
   - **Repository name:** `juanmanuelbejarano`
   - **Description:** Sitio personal — Juan Manuel Bejarano Morales
   - Deja en **Public** (necesario para el plan gratis de Netlify)
   - **NO** marques ninguna de las casillas de "Add README", "gitignore" ni "license"
3. Clic en **Create repository**.

### Paso 3. Subir los archivos del sitio

1. En la página que se abre, busca el enlace que dice **"uploading an existing file"**.
2. Arrastra TODA la carpeta `sitio/` desde tu computadora hacia esa ventana.
   - Importante: arrastra el **contenido** de la carpeta, no la carpeta envoltorio. Es decir, lo que se sube debe ser `index.html`, `articulos/`, `assets/`, etc., en la raíz del repositorio.
3. Abajo, en el campo **Commit changes**, escribe: `Versión inicial del sitio`
4. Clic en **Commit changes**.

Espera 30 segundos a que termine la subida. Verás todos tus archivos listados.

### Paso 4. Subir tu fotografía profesional

1. Dentro del repositorio en GitHub, entra a la carpeta `img/`.
2. Clic en **Add file → Upload files**.
3. Arrastra tu foto. **Asegúrate de que el archivo se llame exactamente `perfil.jpg`** (todo en minúsculas, sin acentos, sin espacios).
4. Commit changes.
5. Borra el archivo `LEEME-foto-perfil.txt` (clic en él → ícono de basura → Commit).

### Paso 5. Crear cuenta en Netlify

1. Entra a **https://netlify.com**
2. Clic en **Sign up**.
3. Elige **Sign up with GitHub** (te ahorras crear otra contraseña).
4. Autoriza el acceso.

### Paso 6. Conectar tu repositorio de GitHub a Netlify

1. Ya dentro de Netlify, clic en **Add new site → Import an existing project**.
2. Elige **GitHub**.
3. Autoriza el acceso a tu cuenta (te abrirá una ventana de GitHub para confirmar).
4. Te aparece una lista de tus repositorios. Selecciona **`juanmanuelbejarano`**.
5. En la pantalla de configuración:
   - **Branch to deploy:** `main`
   - **Build command:** déjalo vacío
   - **Publish directory:** déjalo vacío o pon `.`
6. Clic en **Deploy site**.

Espera 1-2 minutos. Verás en pantalla un nombre raro tipo `wonderful-cookie-12abc.netlify.app`.

### Paso 7. Cambiar el nombre del sitio

1. En Netlify, dentro de tu sitio recién creado, ve a **Site configuration → General → Site details**.
2. Clic en **Change site name**.
3. Escribe: **`juanmanuelbejarano`**
4. Guarda.

Tu sitio ahora vive en: **https://juanmanuelbejarano.netlify.app**

Ábrelo. Debe verse exactamente igual al diseño que armamos.

---

## PARTE 2 — Editar el sitio después de publicado

Tienes dos formas. Empieza con la simple.

### Método A — Editar directamente desde GitHub (recomendado para empezar)

GitHub tiene un editor visual que es muy parecido a un Word básico. No necesitas instalar nada.

**Para editar un artículo o el home:**

1. Entra a tu repositorio en GitHub: `https://github.com/TU-USUARIO/juanmanuelbejarano`
2. Navega al archivo que quieres editar (ejemplo: `articulos/espejismo-crecimiento-bolivia.html`).
3. Clic en el **ícono del lápiz** (arriba a la derecha del archivo).
4. Haz tus cambios.
5. Abajo de la pantalla, escribe un mensaje corto (ej: "Corregí typo en intro").
6. Clic en **Commit changes**.

Netlify detecta el cambio automáticamente y republica tu sitio en 30 segundos.

**Para subir un nuevo artículo:**

1. Copia uno de los 6 artículos como plantilla (descarga, modifica, sube con otro nombre).
2. O, más simple: pídeme el HTML del nuevo artículo (yo te lo entrego listo) y lo subes a `articulos/` con el nombre que prefieras.
3. Edita `index.html` para agregar la card del nuevo artículo en la sección de listado.

### Método B — Panel de administración Decap CMS (avanzado)

Tu sitio ya viene preparado con un panel en `https://juanmanuelbejarano.netlify.app/admin` que permite escribir artículos como en Word.

Activarlo requiere unos pasos adicionales:

1. **Activar Netlify Identity** (sistema de login del panel):
   - En Netlify: **Site configuration → Identity → Enable Identity**
   - En **Registration**: cambia a **Invite only** (para que solo tú puedas entrar)
   - En **External providers**: opcional, puedes activar Google
2. **Activar Git Gateway**:
   - En **Identity → Services → Git Gateway → Enable Git Gateway**
3. **Invitarte a ti mismo**:
   - En **Identity**, clic en **Invite users** → tu correo
   - Te llega un correo con un enlace; haz clic y elige una contraseña.
4. Ahora puedes entrar a `https://juanmanuelbejarano.netlify.app/admin` con ese correo y contraseña.

**Limitación importante a entender:** Decap permite editar y crear archivos `.md` con formato bonito. PERO tu sitio actual sirve los artículos como `.html` (no se renderean automáticamente desde el `.md`). Esto significa que Decap es más útil como:
- Editor de los textos del home (sección "Configuración del sitio")
- Borrador editorial donde escribes artículos nuevos antes de pasarlos a HTML

Si quieres un flujo completamente automático (escribir un `.md` y que aparezca como página HTML al instante), necesitarás migrar el sitio a un generador estático tipo Eleventy o Astro. Es un paso natural más adelante, pero por ahora el flujo simple del Método A te va a servir muy bien.

---

## PARTE 3 — Cosas que vas a querer hacer pronto

### Comprar un dominio propio

`juanmanuelbejarano.netlify.app` funciona bien, pero algo como `jmbejarano.com` o `bejaranomorales.com` es más profesional.

1. Compra el dominio en cualquier registrador (Namecheap, Cloudflare Registrar son baratos y serios).
2. En Netlify: **Site configuration → Domain management → Add a domain**.
3. Sigue las instrucciones de Netlify para apuntar el dominio (te dan unos registros DNS que pegas en el panel del registrador).
4. En 24-48 horas tu sitio aparece en `tu-dominio.com`.

### Activar HTTPS

Netlify lo hace automáticamente. Cuando agregas dominio propio, el certificado se emite solo en pocos minutos.

### Activar el formulario de newsletter

El formulario de newsletter en el sitio está listo para usar Netlify Forms (gratis hasta 100 envíos al mes).

1. En el HTML, en la sección del newsletter, agrega `data-netlify="true"` al tag `<form>`.
2. En Netlify: **Forms** → verás los correos que se inscriban.

### Conectar Google Analytics o Plausible

Edita `index.html` y agrega el script de tu herramienta de analítica antes del `</head>`.

---

## ¿Algo no funciona?

**El sitio se ve sin estilos (texto plano, todo blanco):**
Probablemente la carpeta `assets/` no se subió. Verifica en GitHub que existe `assets/style.css`.

**La foto no aparece:**
Asegúrate de que el archivo se llame exactamente `perfil.jpg` (minúsculas) y esté en la carpeta `img/`.

**Los artículos dan error 404:**
Verifica en GitHub que la carpeta se llama exactamente `articulos` (sin tilde, plural).

**El panel /admin no carga:**
Confirma que activaste Netlify Identity y Git Gateway (Parte 2, Método B).

---

## Resumen del flujo de trabajo diario

1. Tienes una idea para un artículo o quieres corregir algo.
2. Entras a GitHub, editas el archivo, commit.
3. Netlify republica solo en 30 segundos.
4. Listo.

Sin servidores que mantener, sin actualizaciones de software, sin facturas mensuales.

Bienvenido a tu nueva plataforma editorial.
