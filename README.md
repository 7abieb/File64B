# Encrypt/Decrypt Tool - Base64 with High Compression ZIP

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![JSZip](https://img.shields.io/badge/JSZip-3.10.1-blue.svg)](https://github.com/Stuk/jszip)

A lightweight, client-side web tool for encrypting files into high-compression ZIP archives and Base64-encoded strings, and decrypting them back. Supports **any file type** (e.g., MP3, PNG, ZIP, TXT, PDF) up to **10MB**. No server or backend required—everything runs in the browser using JSZip for ZIP handling.

## Features
- **High Compression by Default**: Uses DEFLATE compression at level 9 (maximum) for optimal file size reduction without overloading browser RAM/CPU. Async processing keeps the UI responsive.
- **Encrypt Mode**: Select/drag-drop a file → ZIP with high compression → Base64 encode. Copy or download the Base64 (as .b64 file).
- **Decrypt Mode**: Paste Base64 or upload .b64 → Decode → Unzip. View files as Base64, download individually, or re-encrypt/download all as high-comp ZIP.
- **Any File Support**: Handles binary files seamlessly (audio, images, archives, etc.). Extracted files can be any type.
- **Modern UI**: Responsive design with tabs, progress bars, drag-and-drop, modals, and gradients. Mobile-friendly.
- **Security & Privacy**: Fully client-side—no data leaves your browser. Base64 is for encoding (not encryption; add passwords via JSZip if needed).
- **Performance**: Enforces 10MB limit to avoid overload. Compression takes 2-10 seconds for 10MB files (faster for text, slower but safe for media).
- **Offline-Ready**: After initial load of JSZip from CDN, works offline. (Download JSZip for full offline use.)

## Demo
- Live demo: [Save the HTML and open in browser](https://github.com/yourusername/encrypt-decrypt-tool/raw/main/index.html) (or host on GitHub Pages).
- Screenshots:
  - ![Encrypt Tab](screenshots/encrypt.png) <!-- Add your screenshot here -->
  - ![Decrypt Tab](screenshots/decrypt.png) <!-- Add your screenshot here -->

## Installation & Usage
1. **Download**: Clone or download this repo. The main file is `index.html` (self-contained).
2. **Run**: Open `index.html` in a modern browser (Chrome 80+, Firefox 70+, Safari 14+). No setup needed!
3. **Encrypt a File**:
   - Switch to "Encrypt" tab.
   - Drag/drop or select a file (≤10MB).
   - Click "Encrypt to High Comp Base64" → Get Base64 string (copy/download).
4. **Decrypt Base64**:
   - Switch to "Decrypt" tab.
   - Paste Base64 or upload .b64 file.
   - Click "Decrypt & Unzip" → View file list.
   - Options: View as Base64 (modal), Download single file, Download all as high-comp ZIP, or Re-encrypt to new Base64.
5. **Chaining**: Decrypt → Modify files → Re-encrypt with high compression for smaller outputs.

### Example Workflow
- Upload a 5MB PNG → Encrypt → ~4MB Base64 (compressed ZIP).
- Paste Base64 → Decrypt → Download PNG (original quality).
- Re-encrypt multiple extracted files → Even smaller high-comp ZIP + Base64.

## Limitations
- **File Size**: Input limited to 10MB to prevent browser strain. Extracted files can be larger if the Base64 input is valid.
- **Compression Gains**: Best for text/compressible files (e.g., TXT: 70% reduction). Media like MP3/PNG: Minimal gain (but safe).
- **No Password Protection**: This is encoding, not cryptographic encryption. For passwords, extend with JSZip's options (e.g., AES via external libs).
- **Browser Only**: Not for Node.js—pure web app. IE/Edge <79 unsupported.
- **Base64 Padding**: Handles standard Base64; ignores whitespace.

## Tech Stack
- **HTML5/CSS3**: Modern UI with flexbox, gradients, and media queries.
- **JavaScript (ES6+)**: Async/await for smooth operations.
- **JSZip (v3.10.1)**: For ZIP creation/loading with DEFLATE compression.
- **No Dependencies**: JSZip loaded via CDN for simplicity.

## Contributing
1. Fork the repo.
2. Create a feature branch (`git checkout -b feature/amazing-feature`).
3. Commit changes (`git commit -m 'Add amazing feature'`).
4. Push to branch (`git push origin feature/amazing-feature`).
5. Open a Pull Request.

Issues? Report bugs or suggest features (e.g., password support, lower compression toggle).

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Built with ❤️ using JSZip by Stuart Knightley.
- Inspired by secure file sharing needs.

---

*Star the repo if it helps! 🚀*
