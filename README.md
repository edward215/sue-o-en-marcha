# Sueño en Marcha

Temporizador de enfoque, lista de tareas, racha diaria y tips contra la procrastinación. Se instala en el teléfono como una app y abre incluso sin conexión.

## Archivos

- `index.html`: la app completa.
- `sw.js`: guarda la app para que abra sin conexión.
- `manifest.webmanifest`, `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`: lo necesario para instalarla.
- `screenshot-narrow.png`, `screenshot-wide.png`: capturas que se muestran al instalarla.

## 1. Publicarla en GitHub Pages

1. En GitHub, crea un repositorio nuevo (por ejemplo `sueno-en-marcha`). Puede ser público.
2. Descomprime el paquete y, en el repositorio, usa **Add file → Upload files**. Arrastra todos los archivos (no el zip) y confirma con **Commit changes**.
3. Ve a **Settings → Pages**. En **Source** elige **Deploy from a branch**, rama **main** y carpeta **/ (root)**. Guarda.
4. Espera uno o dos minutos. Tu app quedará en `https://TU-USUARIO.github.io/sueno-en-marcha/`.

## 2. Instalarla en el teléfono

- **Android (Chrome):** menú de tres puntos → **Instalar app** (o **Añadir a la pantalla de inicio**).
- **iPhone (Safari):** botón Compartir → **Añadir a pantalla de inicio**.

## Funciones principales

- **Temporizador de enfoque y descanso**, con alarma al terminar cada sesión y aviso si dejas el enfoque en pausa demasiado tiempo.
- **Ciclo automático:** si lo activas, la app encadena sola enfoque y descanso, con un descanso largo de 15 minutos cada 4 rondas. Bajo el reloj ves en qué ronda vas.
- **Siguiente paso:** al terminar una ronda puedes escribir qué harás después. Se añade al inicio de tu lista, y si eliges «Otra ronda de enfoque» queda como tu tarea en curso.
- **Tareas, ciclo de video, metas de la semana y racha diaria.**
- **Respaldo de datos:** copia tus datos como texto (o descárgalos como archivo `.json`) y restáuralos cuando quieras, en este u otro dispositivo.
- **Colores:** 8 colores para la interfaz.
- **Tutorial:** el botón «Tutorial» explica cada función y te deja probarlas.

## Alarmas

La alarma suena mientras la app está abierta. Mientras el temporizador corre, la app pide al teléfono que no apague la pantalla; si cambias de app o bloqueas el teléfono, el navegador puede suspenderla y la alarma no sonar a tiempo. El ciclo automático también depende de que la app siga abierta.

## Actualizar la app

Si cambias `index.html` u otro archivo, abre `sw.js` y sube el número de `CACHE` (por ejemplo de `v3` a `v4`). Así los teléfonos descargan la versión nueva.

## Datos

Tus tareas, racha y ajustes se guardan solo en el navegador de cada dispositivo. No se sincronizan entre el teléfono y la computadora. Para pasarlos de uno a otro, usa «Descargar archivo» (o «Copiar respaldo») en el apartado **Respaldo de datos** y luego «Cargar archivo» (o «Importar respaldo») en el otro dispositivo.
