# 🐬 Dolphin ServiceMenu Tools – KDE Addons Pack

This is a collection of handy **ServiceMenu addons** for the **Dolphin file manager** (KDE Plasma).  
They extend the right‑click (context) menu with powerful utilities for everyday use:

- 📑 **Documents**: Convert PDF to TXT or PNG  
- 🖼 **Images**: Resize, optimize, convert formats  
- 🔤 **OCR**: Extract text from images  
- 🎵🎬 **Multimedia**: Convert or resize audio & video  
- 📥 **Download videos** from the Internet (`yt-dlp`)  
- 📸 **Screenshots**: Capture directly into selected folder or modify existing images  

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
| **[OCR Tools](./OCR-to-TXT-terminal_paste_code.txt)** | `OCR → TXT` (from PNG/JPG/TIFF) | `tesseract-ocr`, `kdialog` |
| **[Multimedia Tools](./Multimedia-tools-terminal_paste_code.txt)** | `Convert (audio/video)`, `Resize (target MB)` | `ffmpeg`, `ffprobe`, `kdialog` |
| **[Download Video Tools](./Download-video-yt-dlp-terminal-paste-code.txt)** | `Download video (paste URL)` → MP4 (quality) / MP3 | `yt-dlp`, `xclip`/`xsel`, `konsole` *(optional)*, `kdialog` |
| **[Screenshot Tools](./Screenshot-tools-terminal_paste_code.txt)** | **Modify:** Optimize PNG/JPG, Convert.<br>**Take Screenshot:** Save new image via Spectacle | `spectacle`, `xclip`/`xsel`, `optipng`, `jpegoptim`, `imagemagick`, `kdialog` |

---

## 📦 Dependencies

Each module uses common Linux packages. Please install them first:

### Debian / Ubuntu / KDE Neon / Linux Mint
```bash
sudo apt install ffmpeg ffprobe imagemagick optipng jpegoptim \
tesseract-ocr poppler-utils yt-dlp spectacle xclip

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

## 📂 Modules in Detail

### 📑 [Documents Tools](./Documents-tools-terminal_paste_code.txt)
- **PDF → TXT**: extract text with `pdftotext`.  
- **PDF → PNG**: render page ranges to images (`pdftoppm`).  

**Usage:** Right‑click a PDF → *Modify selected file* → select action.  

---

### 🖼 [Images Tools](./Images-tools-terminal_paste_code.txt)
- **Resize % / px**: scale proportionally or to fixed dimensions (ImageMagick).  
- **Optimize**:  
  - PNG → `optipng` (lossless)  
  - JPG → `jpegoptim` (quality ≈85%)  
- **Convert**: output to JPG, PNG, WebP, TIFF, BMP, GIF.  

**Usage:** Right‑click on an image → *Modify selected file*.  

---

### 🔤 [OCR Tools](./OCR-to-TXT-terminal_paste_code.txt)
- **OCR → TXT**: recognizes text in PNG/JPG/TIFF using `tesseract`.  
- Results saved as `*_ocr.txt`.  

**Usage:** Right‑click an image → *Modify selected file* → OCR to TXT.  

---

### 🎵🎬 [Multimedia Tools](./Multimedia-tools-terminal_paste_code.txt)
- **Convert**: transform audio/video into MP3, WAV, FLAC, MP4, MOV, WebM, GIF.  
- **Resize (MB)**: shrink multimedia file to specified size, recalculating bitrate dynamically.  

**Usage:** Right‑click a media file → *Modify selected file* → Convert/Resize.  

---

### 📥 [Download Video Tools](./Download-video-yt-dlp-terminal-paste-code.txt)
- Adds context entry **“Download video (paste URL)”** available on folders.  
- Reads URL from clipboard or prompt.  
- Lets you choose: MP3 (audio) or MP4 (video, quality options).  
- Downloads via `yt-dlp` into chosen folder.  

**Usage:** Right‑click empty space in a folder → Download video.  

---

### 📸 [Screenshot Tools](./Screenshot-tools-terminal_paste_code.txt)
1. **Modify Screenshot/Images**  
   - Optimize (optipng/jpegoptim)  
   - Convert format (JPG/PNG/WebP/TIFF/BMP/GIF)  

2. **Take Screenshot & Save Here**  
   - Context action in empty folder space.  
   - Runs **Spectacle**: Area / Full Screen / Active Window.  
   - Saves screenshot PNG into this folder automatically.  

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

---
