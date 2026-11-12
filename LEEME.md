# Floristería · Cuentas — guía de instalación

Contenido de la carpeta: `index.html` (la app), `firebase-config.js` (tus datos de Firebase),
`firestore.rules` (seguridad), `manifest.webmanifest`, `sw.js` e íconos.

## Parte 1 — Crear la base de datos en Firebase (gratis, ~10 min, se puede hacer desde el iPad)

1. Entra a https://console.firebase.google.com con tu cuenta de Google y toca **Crear un proyecto**.
   Nombre: `floristeria`. Desactiva Google Analytics. Crear.
2. Menú **Compilación > Firestore Database > Crear base de datos**. Elige **modo producción**
   y una ubicación (por ejemplo `nam5` o `us-east1`). Habilitar.
3. En Firestore, pestaña **Reglas**: borra lo que hay y pega el contenido de `firestore.rules`,
   cambiando los dos correos por el tuyo y el de tu mamá. Toca **Publicar**.
4. Menú **Compilación > Authentication > Comenzar > Correo electrónico/contraseña > Habilitar**.
   Luego pestaña **Usuarios > Agregar usuario**: crea dos usuarios (tu correo y el de tu mamá) con
   una contraseña cada uno. Anótalas para entregárselas.
   (Opcional, más seguro: Authentication > Configuración > Acciones del usuario > desactiva
   "Habilitar creación (registro)".)
5. Rueda dentada **Configuración del proyecto > General > Tus apps > ícono web `</>`**. Registra la app
   (nombre `floristeria`, sin Hosting). Copia el bloque `firebaseConfig` y pégalo en
   `firebase-config.js` (o envíaselo a Claude para que lo complete).

## Parte 2 — Poner la app en internet (necesita https)

**Opción A, con computadora:** entra a https://app.netlify.com/drop y arrastra la carpeta completa.
Te da un enlace `https://algo.netlify.app`.

**Opción B, sin computadora (GitHub Pages):** crea una cuenta en github.com, crea un repositorio
público `floristeria`, toca **Add file > Upload files** y sube todos los archivos de esta carpeta.
Luego **Settings > Pages > Branch: main > Save**. El enlace será `https://TU_USUARIO.github.io/floristeria/`.

Es normal que el código sea público: los datos NO lo son, están protegidos por las reglas del paso 3
y por el inicio de sesión.

## Parte 3 — Instalarla en cada teléfono

- **iPhone:** abre el enlace en **Safari** > botón Compartir > **Añadir a pantalla de inicio**.
- **Android:** abre el enlace en Chrome > menú ⋮ > **Instalar app** o **Añadir a pantalla de inicio**.

Entra con tu correo y contraseña. La primera vez te pedirá tu nombre.
Funciona aunque se vaya el internet: lo que anoten se sincroniza solo al volver la conexión.

## Si cambias la app
Sube de nuevo los archivos modificados. Si no ves el cambio, cierra y vuelve a abrir la app.
