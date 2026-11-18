# Sueño en Marcha

Temporizador de enfoque, lista de tareas, racha diaria y tips contra la procrastinación. Se instala en el teléfono como una app y puede avisarte cuando termina una ronda aunque la tengas cerrada.

## Archivos

- `index.html`: la app completa.
- `sw.js`: guarda la app para que abra sin conexión.
- `manifest.webmanifest`, `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`: lo necesario para instalarla.

## 1. Publicarla en GitHub Pages

1. En GitHub, crea un repositorio nuevo (por ejemplo `sueno-en-marcha`). Puede ser público.
2. Descomprime el paquete y, en el repositorio, usa **Add file → Upload files**. Arrastra todos los archivos (no el zip) y confirma con **Commit changes**.
3. Ve a **Settings → Pages**. En **Source** elige **Deploy from a branch**, rama **main** y carpeta **/ (root)**. Guarda.
4. Espera uno o dos minutos. Tu app quedará en `https://TU-USUARIO.github.io/sueno-en-marcha/`.

## 2. Instalarla en el teléfono

- **Android (Chrome):** menú de tres puntos → **Instalar app** (o **Añadir a la pantalla de inicio**).
- **iPhone (Safari):** botón Compartir → **Añadir a pantalla de inicio**.

## 3. Activar los avisos al teléfono con la app cerrada

Los avisos usan [ntfy](https://ntfy.sh), un servicio gratuito de notificaciones.

1. Instala la app **ntfy** en tu teléfono (Play Store, F-Droid o App Store).
2. En Sueño en Marcha, abre **Alarmas**, marca **Avisarme en el teléfono con ntfy** y pulsa **Generar nombre**.
3. En la app ntfy, pulsa **+** y suscríbete a ese mismo nombre de canal.
4. Pulsa **Enviar aviso de prueba** en Sueño en Marcha y cierra la app. En unos 15 segundos debe llegarte la notificación.

Cómo funciona: al iniciar una ronda, la app le pide a ntfy que te envíe un aviso a la hora exacta en que termina. Si pausas, reinicias o cambias de modo, cancela ese aviso. Si la app está abierta y a la vista cuando termina, suena la alarma de la app y el aviso del teléfono se cancela para no duplicarlo.

Importante:

- El nombre del canal funciona como una contraseña. Quien lo conozca puede leer tus avisos, así que usa el que genera la app (largo y aleatorio) y no lo compartas.
- Los avisos necesitan conexión a internet en el momento de iniciar la ronda.
- El servicio gratuito de ntfy.sh tiene límites diarios de mensajes. Para uso personal sobra.

## Actualizar la app

Si cambias `index.html` u otro archivo, abre `sw.js` y sube el número de `CACHE` (por ejemplo de `v1` a `v2`). Así los teléfonos descargan la versión nueva.

## Datos

Tus tareas, racha y ajustes se guardan solo en el navegador de cada dispositivo. No se sincronizan entre el teléfono y la computadora.
