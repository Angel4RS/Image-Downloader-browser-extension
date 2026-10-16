<div align="center">

# 🖼️ Image Downloader

**Detect images on any page and download them in bulk, in the background.**

JPG · PNG · GIF · WebP · AVIF

![Version](https://img.shields.io/badge/version-1.6.1-1a73e8)
![Manifest](https://img.shields.io/badge/Manifest-V3-188038)
![Browser](https://img.shields.io/badge/Chrome-extension-yellow)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-Donate-ff5e5b?logo=ko-fi&logoColor=white)](https://ko-fi.com/angel4kv1)

🌐 [Español](README.md) · [English](README.en.md)

</div>

---

## ✨ What does it do?

Image Downloader scans the page you are on, finds its images, and lets you **pick which ones to download all at once**. It shows the number of images found on the extension icon and lets you keep browsing while everything downloads.

## 🚀 Features

- 🔍 **Automatic detection** of images in `<img>`, `srcset`, `<picture>`, links and inline backgrounds, including pages that load content dynamically.
- 🎞️ **Multiple formats:** JPG, PNG, GIF, WebP and AVIF, with per-format filters and counters.
- 🔎 **Maximum resolution:** tries to download the full-size version instead of the thumbnail (marked with an **HD** tag). Works with links to the full image, gallery attributes, `srcset`, Blogger/Google and WordPress.
- 📦 **Bulk download:** select all, none, or only the ones you want.
- ⏳ **In the background:** you can close the panel or switch tabs; you get a notification when it finishes.
- 🛡️ **Works with protected sites:** sends the original page's *Referer* to avoid the "download interrupted" error on sites with hotlink protection.
- 📁 **Custom folder** inside your Downloads folder (subfolders like `Anime/Screenshots` are supported).
- 🎯 **No quality loss:** files are saved exactly as the site serves them, without recompressing or converting. Animated GIFs stay animated.
- 🌍 **Multilingual:** adapts automatically to the browser language (Spanish, English, Portuguese, French, German and Italian).

## 📥 Installation

> The extension is not on the Chrome Web Store yet, so it is installed in **developer mode**.

### Option A: from the ZIP (recommended)

1. Go to the [**Releases**](../../releases) section and download `Image-Downloader.zip`.
2. **Unzip** it into a folder you won't delete.
3. Open `chrome://extensions` in Chrome.
4. Turn on **Developer mode** (top right).
5. Click **Load unpacked** and choose the `Image-Downloader` folder (the one that contains `manifest.json`).
6. Optional: pin the extension from the puzzle-piece icon 🧩 to keep it at hand.

### Option B: cloning the repository

```bash
git clone https://github.com/Angel4RS/Image-Downloader.git
```

Then follow steps 3 to 6 above, choosing the cloned folder.

> 💡 After installing or updating, **reload any tabs** you already had open so the extension can detect their images.

## 🕹️ How to use it

1. Visit any site with images. The icon shows a **red counter** with the detected images.
2. Click the icon to open the panel.
3. Filter by format, choose the **version** (maximum resolution or page size), and type the destination **folder** if you want to change it.
4. Tick the images you want (or use **All**).
5. Click **Download**. You can close the panel: the download continues in the background and you get a notification when it ends.

Images are saved to `Downloads/<folder>/` (default `Image-Downloader`), numbered in order.

## 🔐 Permissions and privacy

The extension **does not collect or send any data** to any server. Everything happens locally in your browser.

| Permission | What it is used for |
|---|---|
| `host_permissions` (`<all_urls>`) | Detect images on any site and download them. |
| `downloads` | Save files to your Downloads folder. |
| `tabs` | Know the active tab and its address. |
| `storage` | Remember your chosen folder, formats and version. |
| `declarativeNetRequest` | Send the right *Referer* when requesting thumbnails and files. |
| `offscreen` | Prepare files to be saved while the panel is closed. |
| `notifications` | Tell you when the download finishes. |

## ⚠️ Limitations

- Images are detected by the **file extension in the URL** (`.jpg`, `.png`, etc.). If a site serves images without an extension, they won't show up.
- The full-size lookup is pattern-based; on sites with unusual URLs the visible size may be downloaded instead.
- Built for **Google Chrome**. It should work on Chromium-based browsers (Edge, Brave, Opera, Yandex), but it has not been tested on them.
- Files can only be saved to a folder inside *Downloads* (a Chrome limitation for extensions).
- It does not work on internal browser pages (`chrome://`, Chrome Web Store).

## 🗂️ Project structure

```
Image-Downloader/
├── manifest.json       # Extension configuration (Manifest V3)
├── content.js          # Detects the page's images
├── background.js       # Background downloads and counter
├── offscreen.html/js   # Helper document to prepare files
├── popup.html/js       # Extension panel
├── icons/              # Extension icons
└── _locales/           # Translations (en, es, pt, fr, de, it)
```

## 🗺️ Coming soon

- Format conversion on download (for example, WebP/AVIF to PNG or JPG).
- More languages.

Have an idea or found a bug? Open an [issue](../../issues).

## 💜 Support the project

If you find the extension useful, you can buy me a coffee:

[![Ko-fi](https://img.shields.io/badge/☕_Donate_on_Ko--fi-ff5e5b?style=for-the-badge)](https://ko-fi.com/angel4kv1)

## 👤 Author

Created by **[Angel4RS](https://github.com/Angel4RS)**.
