# 🐬 Dolphin ServiceMenu Tools – KDE Addons Pack

This is a collection of handy **ServiceMenu addons** for the **Dolphin file manager** (KDE Plasma).  
They extend the right‑click (context) menu with powerful utilities for everyday use:

- 📑 **Documents**: Convert PDF to TXT or PNG  
- 🖼 **Images**: Resize, optimize, convert formats  
- 🔤 **OCR**: Extract text from images  
- 🎵🎬 **Multimedia**: Convert or resize audio & video  
- 📥 **Download videos** from the Internet (`yt-dlp`)  
- 📸 **Screenshots**: Capture directly into selected folder or modify existing PNG/JPG  

All modules are lightweight **bash scripts** with corresponding `.desktop` entries in `~/.local/share/kio/servicemenus/`.

---

## ⚙️ Installation & Usage

1. Open the `.txt` file of a tool (see links below).  
2. Copy the entire contents.  
3. Paste into a terminal and press Enter.  
4. Wait a few seconds.  
5. Choose option `1 Install`.  
6. Restart/refresh Dolphin – the new context menu entries are ready.  

To uninstall: rerun the script → choose option `2 Uninstall`.  

📌 Note: No root access required – everything installs to the user’s home (`~/.local/share/`).  

---

# 📋 Quick Overview

| Module | Actions | Dependencies |
|--------|---------|--------------|
| **[Documents Tools](./Documents-tools-terminal_paste_code.txt)** | `PDF → TXT`, `PDF → PNG (page range)` | `poppler-utils` (`pdftotext`, `pdftoppm`), `kdialog` |
| **[Images Tools](./Images-tools-terminal_paste_code.txt)** | `Resize (%)`, `Resize (px)`, `Optimize`, `Convert (JPG/PNG/WebP/TIFF/BMP/GIF)` | `imagemagick (convert/magick)`, `optipng`, `jpegoptim`, `kdialog` |
| **[Images Modify Tools](./Images-modify-tools-terminal_paste_code.txt)** | Modify existing images: Optimize PNG/JPG, Convert to other formats | `imagemagick`, `optipng`, `jpegoptim`, `kdialog` |
| **[OCR Tools](./OCR-to-TXT-terminal_paste_code.txt)** | `OCR → TXT` (from PNG/JPG/TIFF) | `tesseract-ocr`, `kdialog` |
| **[Multimedia Tools](./Multimedia-tools-terminal_paste_code.txt)** | `Convert (audio/video)`, `Resize (target MB)` | `ffmpeg`, `ffprobe`, `kdialog` |
| **[Download Video Tools](./Download-video-yt-dlp-terminal-paste-code.txt)** | `Download video (paste URL)` → MP4 (quality) / MP3 | `yt-dlp`, `xclip`/`xsel`, `konsole` *(optional)*, `kdialog` |
| **[Take Screenshot Tools](./Take-screenshot-terminal_paste_code.txt)** | Take screenshot & save into folder (Spectacle: Area / Full / Window) | `spectacle`, `xclip`/`xsel`, `kdialog` |

---

## 📦 Dependencies

Each module uses common Linux packages. Please install them first:

### Debian / Ubuntu / KDE Neon / Linux Mint
```bash
sudo apt install ffmpeg ffprobe imagemagick optipng jpegoptim \
tesseract-ocr poppler-utils yt-dlp spectacle xclip
```

### Arch Linux / Manjaro
```bash
sudo pacman -S ffmpeg imagemagick optipng jpegoptim \
tesseract poppler yt-dlp spectacle xclip
```

### Fedora
```bash
sudo dnf install ffmpeg ImageMagick optipng jpegoptim \
tesseract poppler-utils yt-dlp spectacle xclip
```

### openSUSE
```bash
sudo zypper install ffmpeg ImageMagick optipng jpegoptim \
tesseract poppler-tools yt-dlp spectacle xclip
```

---

## 📂 Modules Overview

### 📑 [Documents Tools](./Documents-tools-terminal_paste_code.txt)
- **PDF → TXT**: Extract text using `pdftotext`.  
- **PDF → PNG**: Render selected page ranges into images using `pdftoppm`.  

**Usage:** Right‑click a PDF → *Modify selected file* → choose desired action.  

---

### 🖼 [Images Tools](./Images-tools-terminal_paste_code.txt)
- **Resize % / px**: Scale images proportionally or to fixed dimensions (ImageMagick).  
- **Optimize**:  
  - PNG → `optipng` (lossless)  
  - JPG → `jpegoptim` (quality ≈85%)  
- **Convert**: output to JPG, PNG, WebP, TIFF, BMP, GIF.  

**Usage:** Right‑click on an image → *Modify selected file*.  

---

### 🖼 [Images Modify Tools](./Images-modify-tools-terminal_paste_code.txt)
- **Optimize**: compress PNG (optipng) or JPG (jpegoptim).  
- **Convert**: convert screenshots/images between JPG, PNG, WebP, TIFF, BMP, GIF.  

**Usage:** Right‑click existing image (e.g. a screenshot) → *Modify selected file*.  

---
### 🔤 [OCR Tools](./OCR-to-TXT-terminal_paste_code.txt)
- **OCR → TXT**: Recognize text in image files (PNG/JPG/TIFF) using `tesseract`.  
- Saves result as `*_ocr.txt`.  

**Usage:** Right‑click an image → *Modify selected file* → OCR to TXT.  

---

### 🎵🎬 [Multimedia Tools](./Multimedia-tools-terminal_paste_code.txt)
- **Convert**: Transform audio/video into MP3, WAV, FLAC, MP4, MOV, WebM, GIF.  
- **Resize (MB)**: Shrink file size to a user‑chosen MB value, using ffmpeg/ffprobe.  

**Usage:** Right‑click a media file → *Modify selected file*.  

---

### 📥 [Download Video Tools](./Download-video-yt-dlp-terminal-paste-code.txt)
- Adds context entry **“Download video (paste URL)”** available on folders.  
- Reads URL from clipboard or prompt.  
- Lets you choose MP3 (audio) or MP4 (video with quality).  
- Downloads via `yt-dlp` directly into the folder.  

**Usage:** Right‑click empty space in a folder → Download video.  

---

### 📸 [Take Screenshot Tools](./Take-screenshot-terminal_paste_code.txt)
- **Take Screenshot & Save Here**:  
  - Appears when right‑clicking **empty space** in a folder.  
  - Launches **Spectacle** in chosen mode: Area / Full Screen / Active Window.  
  - Automatically saves PNG into the folder with timestamp name.  

**Usage:** Right‑click empty folder space → *Take screenshot and paste here*.  

---

## 🖱️ Usage Summary

- **On files** (PDF, images, media):  
  Right‑click → *Modify selected file* → choose tool.  

- **On empty folder area**:  
  - *Download video (paste URL)*  
  - *Take screenshot and paste here*  

---

## 🌍 Language Support

Each module is localized into:  
- 🇵🇱 Polish  
- 🇩🇪 German  
- 🇫🇷 French  
- 🇪🇸 Spanish  
- 🇮🇹 Italian  
- 🇷🇺 Russian  
- 🇨🇳 Simplified Chinese  

Fallback = English if `$LANG` not matched.  

---

## 📋 Development

This is a **modular toolkit** – install whatever modules you want.  
To add your own tool:  
- Create `.desktop` entry in `~/.local/share/kio/servicemenus/`.  
- Place the script in `~/.local/share/dolphin-scripts/`.  

Everything is transparent, editable, and user‑level.  

Feel free to expand, customize, and share 🚀  
```
