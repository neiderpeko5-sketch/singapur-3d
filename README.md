# 🧮 Singapur 3D para peques

App de juegos 3D para aprender matemáticas con el método Singapur, pensada para niños de 2 a 5 años. Incluye seis juegos (contar, comparar, partes, suma, patrones y formas), un personaje que explica y felicita en voz alta, música y efectos de sonido.

Es una **app web instalable (PWA)**: no necesita compilación ni tienda de aplicaciones. Se instala desde el navegador y luego se abre como cualquier app, incluso sin conexión.

## Qué hay en este repositorio

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` | Toda la app (juego, escena 3D, voz y sonido). |
| `manifest.webmanifest` | Nombre, colores e iconos de la app instalada. |
| `sw.js` | Guarda la app para que funcione sin internet. |
| `icons/` | Iconos (incluido el adaptativo de Android). |
| `.github/workflows/pages.yml` | Publica la app en GitHub Pages al subir cambios. |

## Instalarla en el móvil

Primero la app tiene que estar publicada (siguiente apartado). Cuando tengas la dirección:

- **Android (Chrome):** abre la dirección, toca el menú ⋮ y elige **Instalar aplicación** o **Añadir a pantalla de inicio**.
- **iPhone / iPad (Safari):** abre la dirección, toca **Compartir** y luego **Añadir a pantalla de inicio**.
- **Ordenador (Chrome o Edge):** icono de instalar en la barra de direcciones.

Una vez instalada se abre a pantalla completa y funciona sin conexión, salvo la voz, que usa la del propio dispositivo.

## Publicarla en GitHub Pages

1. Crea un repositorio nuevo en <https://github.com/new> (público, sin README).
2. Sube el contenido de esta carpeta: en el repositorio, **Add file → Upload files**, arrastra todo (incluida la carpeta `icons` y `.github`).
3. Ve a **Settings → Pages** y en *Source* elige **GitHub Actions**.
4. En unos segundos la pestaña **Actions** mostrará la publicación terminada, y la dirección será `https://TU-USUARIO.github.io/TU-REPO/`.

Desde ese momento, cada vez que cambies `index.html` y lo subas, la app se actualiza sola.

## Cómo usarla

- Elige un juego en el menú superior. Numi, el personaje, explica qué hacer en voz alta y felicita al acertar; si lo tocas, repite la indicación.
- 🔊 activa o silencia todo. ⛶ pone la escena a pantalla completa (se sale con ✕ o Esc).
- El progreso (estrellas y nivel) se guarda en el propio dispositivo.

## Notas

- La voz la pone el sistema del dispositivo: si no se oye, revisa el volumen, el interruptor de silencio y que haya una voz en español instalada.
- Los primeros sonidos requieren un toque en la pantalla (norma de los navegadores): por eso aparece el botón «Tocar para oír a Numi».
- Este repositorio no genera un archivo `.apk`. Si algún día quieres publicarla en Google Play, el camino es envolver esta misma carpeta con Capacitor; la app ya está lista para ello.
