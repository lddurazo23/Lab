LABORATORIO QUÍMICO 3D — Paquete instalable (PWA)
=================================================

Este paquete contiene:
  index.html      -> el simulador (idéntico al archivo único, funciona offline)
  manifest.json   -> datos de la app (nombre, íconos, modo pantalla completa)
  sw.js           -> service worker (hace que funcione 100% sin conexión ya instalada)
  icon-192.png / icon-512.png / icon-180.png / favicon-32.png -> íconos

USO SIN INSTALAR
----------------
Abre index.html con doble clic: funciona igual, offline, en cualquier navegador.
(En este modo el navegador NO ofrece "instalar"; para eso sírvelo por una URL, abajo.)

CÓMO VOLVERLO APP INSTALABLE (elige UNA opción)
-----------------------------------------------

OPCIÓN A — Netlify Drop (la más fácil, sin cuenta ni comandos):
  1. Entra a  https://app.netlify.com/drop
  2. Arrastra TODA la carpeta pwa_bundle a la página.
  3. Te da una URL pública (https://algo.netlify.app).
  4. Abre esa URL en el teléfono o PC:
       - Android/Chrome: menú (⋮) -> "Instalar app" o "Añadir a pantalla de inicio".
       - iPhone/Safari: compartir -> "Añadir a inicio".
       - PC Chrome/Edge: ícono de instalar en la barra de direcciones.
  Queda con ícono propio, pantalla completa y funcionando offline.

OPCIÓN B — GitHub Pages (gratis, permanente):
  1. Crea un repositorio en github.com y sube estos archivos.
  2. Settings -> Pages -> Branch: main / root -> Save.
  3. Te da una URL https://usuario.github.io/repo/ ; instálala igual que arriba.

OPCIÓN C — Probar en tu propia PC (local):
  En la carpeta pwa_bundle ejecuta uno de estos y abre http://localhost:8000
     python3 -m http.server 8000
     npx serve .
  (Sirve para probar la instalación en la misma red; el teléfono puede abrir
   http://IP-de-tu-PC:8000)

CONVERTIR A .APK (Android) o .EXE/.MSIX (Windows)
-------------------------------------------------
Una vez publicada la URL (opción A o B), usa PWABuilder (gratis, de Microsoft):
  1. Entra a  https://www.pwabuilder.com
  2. Pega tu URL y pulsa "Start".
  3. Descarga el paquete Android (.apk/.aab) o Windows (.msix).
  El .apk se instala en Android; el paquete Windows se instala como app de escritorio.

Nota: un .apk para publicarse en tiendas o instalarse sin "orígenes desconocidos"
necesita una firma; PWABuilder explica el paso. Para uso personal, el .apk firmado
de prueba que genera se instala activando "instalar apps desconocidas".
