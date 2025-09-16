# Encrypt/Decrypt Tool - Base64 with High Compression ZIP

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/YOUR_USERNAME/encrypt-decrypt-tool?style=social)](https://github.com/YOUR_USERNAME/encrypt-decrypt-tool)

A lightweight, client-side web tool for encrypting and decrypting files using high-compression ZIP archiving combined with Base64 encoding. Perfect for securely sharing files (e.g., MP3, PNG, ZIP, documents) via text-based channels like email, chat, or code snippets, while minimizing file size.

This tool runs entirely in the browser—no server required. It supports files up to 10MB and uses DEFLATE compression at level 9 for optimal size reduction.

## Features

- Encryption: Select any file (up to 10MB), compress it into a ZIP with high compression (level 9), and encode it to Base64. Output as copyable text or downloadable `.b64` file.
- Decryption: Paste Base64 text or upload a `.b64` file to decode, unzip, and extract original files. View file contents as Base64, download individually, or re-zip everything.
- Re-Encryption: After decryption, re-encrypt extracted files with high compression for easy resharing.
- User-Friendly Interface: Tabbed UI with drag-and-drop support, progress bars, error handling, and responsive design (mobile-friendly).
- Security Notes: This is not cryptographic encryption—it's compression + encoding for size reduction and text portability. For sensitive data, use proper encryption tools (e.g., AES).
- File Support: Handles any file type (images, audio, documents, etc.). Multiple files can be handled post-decryption.
- Performance: Processes files client-side using Web APIs; high compression may take a few seconds for larger files.

## Demo

- Live Demo: [View on GitHub Pages](https://YOUR_USERNAME.github.io/encrypt-decrypt-tool/) (Replace with your actual repo URL once deployed).
- Screenshots:
- Encryption tab: Drag/drop a file, click "Encrypt" to get Base64 output.
- Decryption tab: Paste/upload Base64, extract and download files.

## Usage

1. Open the Tool:
- Download `index.html` (this file) and open it in any modern web browser (Chrome, Firefox, Safari, Edge).
- Or clone the repo and serve it locally (e.g., via `python -m http.server` or GitHub Pages).

2. Encrypt a File:
- Switch to the "Encrypt" tab.
- Drag & drop a file (max 10MB) or click "Choose File".
- Click Encrypt to High Comp Base64.
- Copy the Base64 string or download as `.b64` file.
- Example: A 5MB PNG might compress to ~2-3MB ZIP + Base64 (~4MB text).

3. Decrypt Base64:
- Switch to the "Decrypt" tab.
- Paste Base64 text into the textarea or upload a `.b64` file.
- Click Decrypt & Unzip.
- View extracted files, download individually, or download all as a high-comp ZIP.
- Optional: Click Re-Encrypt to get a new Base64 output.

4. Tips:
- High compression (level 9) reduces size but increases processing time—ideal for text-heavy or compressible files.
- For multiple files: Decrypt first, then use "Download All as High Comp ZIP" or "Re-Encrypt".
- Errors: Check console (F12) for details; invalid Base64 will show warnings.

## Installation

No installation needed! This is a single HTML file with embedded CSS and JavaScript.

- Local Setup:
1. Clone the repo: `git clone https://github.com/YOUR_USERNAME/encrypt-decrypt-tool.git`
2. Open `index.html` in your browser.

- GitHub Pages:
1. Push to a GitHub repo.
2. Enable Pages in repo settings (source: main branch, `/docs` or root).
3. Access at `https://YOUR_USERNAME.github.io/encrypt-decrypt-tool/`.

- Development:
- Edit `index.html` directly.
- Test in browser; no build tools required.

## Technologies Used

- Frontend: Vanilla HTML5, CSS3 (with gradients, flexbox, media queries for responsiveness), JavaScript (ES6+).
- Libraries:
- [JSZip 3.10.1](https://stuk.github.io/jszip/) - For ZIP compression/decompression (DEFLATE, level 9).
- [Font Awesome 6.4.0](https://fontawesome.com/) - Icons for UI polish.
- Browser APIs: FileReader, Blob, URL.createObjectURL, atob/btoa for Base64, Drag & Drop API.
- Compatibility: Modern browsers (IE11+ with polyfills if needed). No backend/server.

## Limitations

- File size limit: 10MB (browser memory constraints; adjustable in code).
- Compression: Best for compressible files (e.g., text, images). Already-compressed files (e.g., MP3, JPEG) see minimal gains.
- No password protection on ZIP (add via JSZip options if needed).
- Client-side only: All processing happens in-browser; large files may slow down on low-end devices.

## Contributing

Contributions welcome! Fork the repo and submit a pull request.

1. Fork/clone the repo.
2. Make changes (e.g., add features like password ZIPs or larger file support).
3. Test in multiple browsers.
4. Commit with clear messages (e.g., "Add password support to ZIP").
5. Push and open a PR.

Issues? Open a GitHub issue with details (browser, file type, error message).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with love using open-source tools.
- Inspired by common needs for file sharing in developer workflows.
- Thanks to the JSZip and Font Awesome teams!
