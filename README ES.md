<div align="center">

# 🖼️ Image Downloader

**Detecta imágenes en cualquier página y descárgalas en lote, en segundo plano.**

JPG · PNG · GIF · WebP · AVIF

![Versión](https://img.shields.io/badge/versión-1.6.1-1a73e8)
![Manifest](https://img.shields.io/badge/Manifest-V3-188038)
![Navegador](https://img.shields.io/badge/Chrome-extensión-yellow)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-Donar-ff5e5b?logo=ko-fi&logoColor=white)](https://ko-fi.com/angel4kv1)

🌐 Español

</div>

---

## ✨ ¿Qué hace?

Image Downloader escanea la página en la que estás, encuentra sus imágenes y te deja **elegir cuáles descargar de una sola vez**. Muestra el número de imágenes encontradas en el ícono de la extensión y te permite seguir navegando mientras todo se descarga.

## 🚀 Características

- 🔍 **Detección automática** de imágenes en `<img>`, `srcset`, `<picture>`, enlaces y fondos en línea, incluso en páginas que cargan contenido de forma dinámica.
- 🎞️ **Varios formatos:** JPG, PNG, GIF, WebP y AVIF, con filtros por formato y contador de cada uno.
- 🔎 **Máxima resolución:** intenta descargar la versión grande en lugar de la miniatura (marcadas con la etiqueta **HD**). Funciona con enlaces a la imagen completa, atributos de galerías, `srcset`, Blogger/Google y WordPress.
- 📦 **Descarga múltiple:** selecciona todas, ninguna o solo las que quieras.
- ⏳ **En segundo plano:** puedes cerrar el panel o cambiar de pestaña; recibirás una notificación al terminar.
- 🛡️ **Compatible con sitios protegidos:** envía el *Referer* de la página original para evitar el error de "descarga interrumpida" en sitios con protección anti-hotlink.
- 📁 **Carpeta personalizable** dentro de tu carpeta de Descargas (admite subcarpetas como `Anime/Capturas`).
- 🎯 **Sin pérdida de calidad:** los archivos se guardan tal cual los sirve el sitio, sin recomprimir ni convertir. Los GIF animados siguen animados.
- 🌍 **Multilenguaje:** se adapta automáticamente al idioma del navegador (español, inglés, portugués, francés, alemán e italiano).

## 📥 Instalación

> La extensión aún no está en Chrome Web Store, así que se instala en **modo desarrollador**.

### desde el ZIP 

1. Ve a la sección [**Releases**](../../releases) y descarga `Image-Downloader.zip`.
2. **Descomprime** el archivo en una carpeta que no vayas a borrar.
3. Abre `chrome://extensions` en Chrome.
4. Activa el **Modo de desarrollador** (arriba a la derecha).
5. Pulsa **Cargar descomprimida** y elige la carpeta `Image-Downloader` (la que contiene el archivo `manifest.json`).
6. Opcional: fija la extensión desde el ícono de la pieza de rompecabezas 🧩 para tenerla siempre a mano.

> 💡 Después de instalar o actualizar, **recarga las pestañas** que ya tenías abiertas para que la extensión pueda detectar sus imágenes.

## 🕹️ Cómo se usa

1. Entra a cualquier sitio con imágenes. El ícono mostrará un **contador rojo** con las imágenes detectadas.
2. Haz clic en el ícono para abrir el panel.
3. Filtra por formato, elige la **versión** (máxima resolución o tamaño de la página) y escribe la **carpeta** de destino si quieres cambiarla.
4. Marca las imágenes que quieras (o usa **Todas**).
5. Pulsa **Descargar**. Puedes cerrar el panel: la descarga continúa en segundo plano y verás una notificación al terminar.

Las imágenes se guardan en `Descargas/<carpeta>/` (por defecto `Image-Downloader`), numeradas en orden.

## 🔐 Permisos y privacidad

La extensión **no recopila ni envía datos** a ningún servidor. Todo ocurre localmente en tu navegador.

| Permiso | Para qué se usa |
|---|---|
| `host_permissions` (`<all_urls>`) | Detectar imágenes en cualquier sitio y descargarlas. |
| `downloads` | Guardar los archivos en tu carpeta de Descargas. |
| `tabs` | Saber cuál es la pestaña activa y su dirección. |
| `storage` | Recordar tu carpeta, formatos y versión elegidos. |
| `declarativeNetRequest` | Enviar el *Referer* correcto al pedir miniaturas y archivos. |
| `offscreen` | Preparar los archivos para guardarlos mientras el panel está cerrado. |
| `notifications` | Avisarte cuando termina la descarga. |

## ⚠️ Limitaciones

- Detecta imágenes por la **extensión en la URL** (`.jpg`, `.png`, etc.). Si un sitio sirve imágenes sin extensión, no aparecerán.
- La búsqueda de la versión grande se basa en patrones; en sitios con URLs especiales puede descargarse el tamaño visible.
- Pensada para **Google Chrome**. Debería funcionar en navegadores basados en Chromium (Edge, Brave, Opera), pero no está probada en ellos.
- Solo se descarga a una carpeta dentro de *Descargas* (limitación de Chrome para las extensiones).
- No funciona en páginas internas del navegador (`chrome://`, Chrome Web Store).

## 🗂️ Estructura del proyecto

```
Image-Downloader/
├── manifest.json       # Configuración de la extensión (Manifest V3)
├── content.js          # Detecta las imágenes de la página
├── background.js       # Descargas en segundo plano y contador
├── offscreen.html/js   # Documento auxiliar para preparar los archivos
├── popup.html/js       # Panel de la extensión
├── icons/              # Íconos de la extensión
└── _locales/           # Traducciones (en, es, pt, fr, de, it)
```

## 🗺️ Próximamente

- Conversión de formatos al descargar (por ejemplo, WebP/AVIF a PNG o JPG).
- Más idiomas.

¿Tienes una idea o encontraste un error? Abre un [issue](../../issues).

## 💜 Apoya el proyecto

Si la extensión te resulta útil, puedes invitarme un café:

[![Ko-fi](https://img.shields.io/badge/☕_Donar_en_Ko--fi-ff5e5b?style=for-the-badge)](https://ko-fi.com/angel4kv1)

## 👤 Autor

Creado por **[Angel4RS](https://github.com/Angel4RS)**.
