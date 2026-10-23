# BlockWorld: web app instalable

BlockWorld es un juego de construir con bloques para niños de 5 a 8 años. Es una web app instalable (PWA): se instala desde el navegador en Android y en iPhone/iPad, queda con su ícono en la pantalla de inicio, abre a pantalla completa y funciona sin internet después de la primera vez.

## Archivos

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` y carpeta `assets/` | El juego completo |
| `manifest.webmanifest` | Nombre, ícono, colores y modo pantalla completa de la app |
| `sw.js` | Guarda el juego en el teléfono para jugar sin conexión |
| `icons/`, `favicon.png` | Íconos de la app (Android, iPhone y pestaña del navegador) |

## 1. Publicarlo en internet (obligatorio para instalar)

Los teléfonos solo instalan web apps que se abren desde una dirección `https://`. Cualquiera de estas opciones gratuitas sirve.

**GitHub Pages**
1. Crea un repositorio y sube el contenido de esta carpeta (que `index.html` quede en la raíz).
2. En el repositorio: Settings → Pages → Branch: `main` → carpeta `/ (root)` → Save.
3. La dirección será `https://tu-usuario.github.io/nombre-del-repo/`.

**Netlify Drop**
1. Entra a https://app.netlify.com/drop
2. Arrastra esta carpeta completa a la página.

## 2. Instalarlo en el celular

**Android (Chrome)**
- En el menú del juego aparece el botón 📲. Tócalo y confirma.
- Si no aparece: menú ⋮ de Chrome → **Instalar app** (o **Agregar a pantalla principal**).

**iPhone / iPad (Safari)**
- Abre la dirección en **Safari** (en iPhone, Chrome no instala web apps).
- Toca **Compartir** (cuadrado con flecha) → **Agregar a pantalla de inicio** → **Agregar**.

El juego se juega con el teléfono **horizontal**. Si está vertical, aparece un aviso para girarlo.

## 3. Publicar una actualización

Desde la carpeta del proyecto ejecuta `npm run webapp`: vuelve a compilar el juego y actualiza esta carpeta. Después sube los archivos de nuevo. Antes de compilar, cambia la línea `const VERSION = 'blockworld-v2'` de `public/sw.js` (por ejemplo a `blockworld-v3`) para que los teléfonos renueven la copia guardada.

## Controles

| Acción | Teclado | Celular |
| --- | --- | --- |
| Caminar | WASD o flechas | Dedo en la mitad izquierda |
| Mirar | Arrastrar con el ratón | Dedo en la mitad derecha |
| Poner / quitar bloque | Clic (clic derecho quita) | Tocar el lugar |
| Cambiar PONER / QUITAR | R | Botón verde/rojo |
| Saltar / volar | Espacio / F (Q baja) | Botones SALTAR y VOLAR |
| Mochila de bloques | B o números 1-8 | Botón 🎒 |

Los mundos y las medallas se guardan solos en cada teléfono. No hay anuncios, compras ni chat.
