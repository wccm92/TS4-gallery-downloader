# TS4 Gallery Downloader (Modified)
![Version](https://img.shields.io/badge/version-v3.1-blue?style=flat-square)
![Userscript](https://img.shields.io/badge/works%20on-EA%20Gallery-5cba47?logo=ea&logoColor=white&style=flat-square)
![Status](https://img.shields.io/badge/status-actively%20maintained-brightgreen?style=flat-square)
![Built](https://img.shields.io/badge/built%20with-%E2%9D%A4%EF%B8%8F%20by%20nrksu1tan-orange?style=flat-square)


A **modified version** of the widely used and highly respected [**“TS4 Gallery Downloader” script by anadius**](https://anadius.su/sims-4-gallery-downloader) — a trusted name in the Sims modding community known for tools that make *The Sims 4* more accessible and customizable.

This version preserves all the powerful functionality of the original script, which allows players to **download households, lots, and rooms directly** from *The Sims 4* Gallery website.

🔧 **What’s new in this fork?**  
Fixed crashes when EA gives broken files — now the script just skips them and keeps downloading what works.  
Plus: new design with smoother cards, a better-looking page, and a bright custom **Download** button that’s easy to find.  
Same great features — just more stable and stylish!


---

## 🛠️ What’s New in This Fork (v3.1)

- 🚫 **No more errors when downloading** — if a lot is broken or removed from the Gallery, the script just skips it without crashing.
- 📁 **More reliable downloads** — everything that can be downloaded is saved into a `.zip` file, just like before.
- 💬 **Helpful messages in the browser console** — if something doesn’t work, you’ll get a clear explanation (check DevTools).
- 🎨 **New cleaner look!** Lot cards now have rounded corners, soft shadows, and a nicer background — more modern and easier to browse.
- 🔘 **Improved Download button** — bigger, brighter, and easier to find and click.
- 🧠 **Better compatibility with older/custom lots** — even rare or unusual uploads should download without issues now.
- ✅ Everything else works the same — just more stable, more polished, and more user-friendly.

---

## 🔄 Original vs Modded
| Feature                     | Original Script | This Fork |
|----------------------------|-----------------|-----------|
| Download from Gallery      | ❌              | ✅        |
| Skips broken lots          | ❌              | ✅        |
| Custom Download button     | ❌              | ✅        |
| New UI design              | ❌              | ✅        |
| Helpful console messages   | ❌              | ✅        |
| Actively maintained        | ❌              | ✅        |

---

## 📦 Installation

1. **Install a userscript manager**  
   You need one of these browser extensions to run the script:
   - [Tampermonkey](https://tampermonkey.net/) – **recommended**
   - [Violentmonkey](https://violentmonkey.github.io/) – alternative option

2. **Choose your version**



| Version | Description | Link |
|--------|-------------|------|
| ✨ **Modded Version (Recommended)** | Includes the bugfix **+** a better UI and a styled "Download" button | [Install](https://github.com/nrksu1tan/TS4-gallery-downloader/raw/refs/heads/main/mod%20versions/TS4%20Gallery%20Downloader%20—%20Fixed%20&%20Enhanced.user.js) |


> 🟢 **Regular players should pick the *Modded Version*** — it's easier, looks better, and works the same.  

3. **Go to the Sims 4 Gallery**  
   Open [The Sims 4 Gallery website](https://www.ea.com/games/the-sims/the-sims-4/pc/gallery) and wait a few seconds.

4. **Use the "Download" button**  
   You’ll now see a custom **Download** button on every lot, room, or household. Click it — and a `.zip` will download automatically.

5. **Install the downloaded content**  
   - Unzip the file  
   - Put all extracted files (`.trayitem`, `.blueprint`, `.bpi`, `.hhi`, `.sgi`, etc.) into:  
     `Documents\Electronic Arts\The Sims 4\Tray`

6. **Start the game**  
   Open Sims 4 and check your Library in Build/Buy mode. Don’t forget to enable **"Include Custom Content"** in the filter if needed.

---

## 📸 Button Preview

Screenshot from the Gallery page with enhanced design:


> ![image](https://raw.githubusercontent.com/nrksu1tan/TS4-gallery-downloader/refs/heads/main/assets/demo.png)
> 




---

## ⚠️ Usage Notes

- If you see warnings like `Truncated .dat file` in the browser console, that means the Gallery item was removed or the file is corrupted on EA’s servers.
- The script still downloads what it can, even for broken items.

---

## ✉️ Found a Bug or Issue?

If you notice something broken, a missing button, or a specific lot that refuses to download — feel free to report it!

📬 **Contact / Report Issues**:
- [Open an issue on GitHub](https://github.com/nrksu1tan/TS4-gallery-downloader/issues)
- Or message me directly on **Telegram**: [@nrksu1tan](https://t.me/nrksu1tan)

Your feedback helps make the script better for everyone 💛

---

## 🙏 Credits

- 👨‍💻 **Original author**: [anadius](https://github.com/anadius)  
  All core logic belongs to the original creator. This fork only includes a small bug fix.
- ✍️ **Modified by**: [Nursultan](https://github.com/nrksu1tan)  
  Added custom download button and improved fallback behavior.

- 📚 Libraries used:  
  - [`protobufjs`](https://www.npmjs.com/package/protobufjs)  
  - [`jszip`](https://www.npmjs.com/package/jszip)  
  - [`file-saver`](https://www.npmjs.com/package/file-saver)  
  - [`long`](https://www.npmjs.com/package/long)

---

## 📜 Disclaimer

> This project is not affiliated with or endorsed by Electronic Arts or Maxis.  
> “The Sims” and related assets are trademarks of Electronic Arts Inc.  
> This script is for personal backup and educational use only. Use responsibly.


## 📦 Bulk Downloader (Download All Results at Once)

In addition to the per-item Download button, this repo includes a
**bulk downloader script** that downloads every result from your active
Gallery search in a single run.

### What it does

- Reads your active search filters directly from the page URL
- Fetches **all pages** of results from EA's Gallery API (no scrolling needed)
- For each item, generates a game-ready ZIP containing:
  - `.trayitem` — the binary metadata file the game indexes
  - `.blueprint` / `.householdbinary` / `.room` — the actual content data
- Files are named and structured identically to the per-item downloader

### Installation

1. Make sure the main TS4 Gallery Downloader script is installed first
2. In Tampermonkey Dashboard, click **+** to add a new script
3. Paste the contents of `TS4-Gallery-Bulk-Downloader.user.js` and save

### Usage

1. Go to the [EA Gallery](https://www.ea.com/games/the-sims/the-sims-4/pc/gallery)
2. Apply a search or filter (by creator, category, hashtag, etc.)
3. Click the green **📦 Download All Results** button (bottom-right corner)
4. Wait for all ZIPs to download — a progress bar shows current status
5. Unzip all files into `Documents\Electronic Arts\The Sims 4\Tray`
6. Launch the game — items will appear in your Library

### Notes

- Chrome will ask "Allow ea.com to download multiple files?" on first run — click **Allow**
- Items that have been removed from the Gallery or have corrupt server files will be skipped
- Progress and any errors are visible in the browser console (`F12 → Console`)
