# 🐬 Dolphin ServiceMenu Tools – KDE Addons Pack

A collection of handy **ServiceMenu addons** for the **Dolphin file manager** (KDE Plasma).  
They extend the right‑click (context) menu with powerful tools for everyday use:

- 📑 **Documents**: Convert PDF to TXT/PNG  
- 🖼 **Images**: Resize, optimize, convert formats  
- 🔤 **OCR**: Extract text from images  
- 🎵🎬 **Multimedia**: Convert/rescale audio & video  
- 📥 **Download videos** from the Internet (`yt-dlp`)  
- 📸 **Screenshots**: Capture directly into the selected folder or modify existing PNG/JPG  

All modules are lightweight **bash scripts** tied to `.desktop` entries in `~/.local/share/kio/servicemenus/`.

---

## ⚙️ Installation & Usage

All modules are distributed as `.txt` files containing ready‑to‑run bash code.  

1. Open a `.txt` file → copy all.  
2. Paste into a terminal → choose `1 Install`.  
3. Restart or refresh Dolphin → the ServiceMenu appears in the context menu.  

To uninstall: run the same script again → choose `2 Uninstall`.  

No root access required — everything is installed into the user’s home (`~/.local/share/`).

---

## 📦 Dependencies

Each tool uses common Linux packages. Install them before using:

### Debian / Ubuntu / KDE Neon / Linux Mint
```bash
sudo apt install ffmpeg ffprobe imagemagick optipng jpegoptim tesseract-ocr poppler-utils yt-dlp spectacle xclip
```

### Arch Linux / Manjaro
```bash
sudo pacman -S ffmpeg imagemagick optipng jpegoptim tesseract poppler yt-dlp spectacle xclip
```

### Fedora
```bash
sudo dnf install ffmpeg ImageMagick optipng jpegoptim tesseract poppler-utils yt-dlp spectacle xclip
```

### openSUSE
```bash
sudo zypper install ffmpeg ImageMagick optipng jpegoptim tesseract poppler-tools yt-dlp spectacle xclip
```

---

## 📂 Modules Overview

### 📑 **Documents Tools**
- **PDF → TXT**: Extract text using `pdftotext`.  
- **PDF → PNG**: Render selected page ranges into images using `pdftoppm`.  

Usage:  
PPM (right‑click) on a PDF → *Modify selected file* → choose desired action.  

---

### 🖼 **Images Tools**
- **Resize % / px**: Scale images proportionally or to fixed dimensions (ImageMagick).  
- **Optimize image**:  
  - PNG → lossless optimization via `optipng`.  
  - JPG → shrink size via `jpegoptim`.  
- **Convert image**: Convert any supported format to: JPG, PNG, WebP, TIFF, BMP, GIF.  

Usage:  
PPM on image files → *Modify selected file* → select action.  

---

### 🔤 **OCR Tools**
- **OCR → TXT**: Recognize text in image files (JPG/PNG/TIFF) using `tesseract`.  
- Automatically creates a `*_ocr.txt` file.  

Usage:  
PPM on an image → *Modify selected file* → «OCR to TXT».  

---

### 🎵🎬 **Multimedia Tools**
- **Convert**: Transform audio/video to common formats: MP3, WAV, FLAC, MP4, MOV, WebM, GIF.  
- **Resize (MB)**: Shrink video/audio to a user‑specified file size, recalculating bitrate dynamically.  

Usage:  
PPM on media file → *Modify selected file* → Convert or Resize.  

---

### 📥 **Download Video Tools**
- **Download video (paste URL)**:  
  - Works on folder context (PPM in empty space).  
  - Reads URL from clipboard (or asks via dialog).  
  - Lets you choose format (MP3 audio / MP4 video with quality options).  
  - Downloads via `yt-dlp` straight into the chosen folder.  

Usage:  
PPM on an empty spot in Dolphin → «Download video (paste URL)».  

---

### 📸 **Screenshot Tools**
1. **Modify Screenshot / Images**  
   - Optimize existing PNG/JPG (optipng/jpegoptim).  
   - Convert image format to JPG/PNG/WebP/TIFF/BMP/GIF.  

2. **Take Screenshot & Save Here**  
   - Appears when right‑clicking on empty folder space.  
   - Runs **Spectacle** in chosen mode: Area / Full Screen / Active Window.  
   - Automatically saves PNG into this folder.  

---

## 🖱️ Usage Summary

- **On files** (PDF, images, videos, audio):  
  PPM → *Modify selected file* → access extra tools.  
- **On empty folder space**:  
  - «Download video (paste URL)»  
  - «Take screenshot and paste here»  

---

## 🌍 Languages

All addons include localized names and messages in:  
- Polish 🇵🇱  
- German 🇩🇪  
- French 🇫🇷  
- Spanish 🇪🇸  
- Italian 🇮🇹  
- Russian 🇷🇺  
- Chinese 🇨🇳  

Fallback to English otherwise.  

---

## 📋 Credits & Development

This pack combines simple **bash scripts** + **KDE ServiceMenus** to extend Dolphin.  
It is designed as a **modular toolkit** – you can install only the modules you want.  
Adding new tools is easy: drop a `.desktop` in `~/.local/share/kio/servicemenus` + add a helper script in `~/.local/share/dolphin-scripts/`.  

Feel free to expand, customize, and share! 🚀  

---
