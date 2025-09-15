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
| **[Images Tools](./Images-tools-terminal_paste_code.txt)** | `Resize (%)`, `Resize (px)` | `imagemagick (convert/magick)`, `kdialog` |
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

**Usage:** Right‑click on an image → *Modify selected file* → Resize (%), Resize (px)

---

### 🖼 [Images Modify Tools](./Images-modify-tools-terminal_paste_code.txt)
- **Optimize**: compress PNG (optipng) or JPG (jpegoptim).  
- **Convert**: convert screenshots/images between JPG, PNG, WebP, TIFF, BMP, GIF.  

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

### 📥 [Download Video Tools](./Download-video-yt-dlp-terminal_paste_code.txt)
- Adds context entry **“Download video (paste URL)”** available on folders.  
- Reads URL from clipboard or prompt.  
- Lets you choose MP3 (audio) or MP4 (video with quality).  

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

# ❓ FAQ – Dolphin ServiceMenu Tools

### 🔹 Do I need root privileges to install these addons?
**No.** All scripts install into your user directory (`~/.local/share/`).  
No system packages are touched. You can add or remove them anytime.

---

### 🔹 Does installing these modify Dolphin or Plasma?
**No.** They only add `.desktop` entries (ServiceMenu files) and small bash scripts.  
If you uninstall → Dolphin goes back to its default menus unchanged.

---

### 🔹 What dependencies are needed?
Each tool uses well‑known open source packages:
- `ffmpeg`, `ffprobe` → audio/video handling  
- `imagemagick`, `optipng`, `jpegoptim` → images  
- `poppler-utils` → PDF manipulation  
- `tesseract-ocr` → OCR text recognition  
- `yt-dlp` (+ `ffmpeg`) → video/audio downloader  
- `spectacle`, `xclip`/`xsel` → screenshots & clipboard  

Install instructions for each distro are listed above in [Dependencies](#-dependencies).

---

### 🔹 What video sites can be downloaded?
The **Download Video Tools** use `yt-dlp`. Despite its name, this is **not only YouTube**.  
It supports **thousands of websites**, including:
- YouTube, Vimeo, Twitch, DailyMotion  
- Facebook Reels, Instagram, TikTok, Twitter/X  
- SoundCloud, Bandcamp, Mixcloud  
- News/media sites and any `.m3u8`/HLS based streaming  

If your browser can play it → `yt-dlp` can usually download it.  
It automatically merges best video + audio into one MP4 or extracts MP3 if you wish.

---

### 🔹 What apps can I uninstall now?
These ServiceMenus replace most one-purpose GUI tools or browser plugins, for example:
- Flatpak **VideoDownloader**, ClipGrab, youtube-dl GUIs, browser download add-ons  
- Online PDF converters (“PDF → JPG → upload → download”)  
- GUI image converters/resizers like XnConvert (for basic tasks)  
- Online OCR web pages or heavy desktop OCR GUIs  
- HandBrake (for simple conversions), online audio/video converters  
- Manual workflows with Spectacle + moving files  

👉 Everything is now available **integrated in Dolphin**: right click → *Modify selected file* or → *Download video / Take screenshot*.

---

### 🔹 Can I use these safely on system files?
Yes – they only act on the files you explicitly click.  
New results are created as separate files (with suffix `_conv`, `_resize`, `_ocr`, etc.).  
Your original files remain untouched unless you manually delete them.

---

### 🔹 Can I extend these tools?
Absolutely ✅  
The system is modular:
- New tools can be added by creating a `.desktop` file in `~/.local/share/kio/servicemenus`  
- Scripts go into `~/.local/share/dolphin-scripts`  

All scripts here are open bash, so you can easily adjust them or write your own.

---

## 🚀 In Short
These addons turn Dolphin into a **Swiss‑army knife** for documents, images, videos, audio, screenshots, OCR and downloads – no extra software GUIs or browser extensions needed.  
Right click → Done. 🎉 
