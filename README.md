# AML-Omics Cast Player

A web-based terminal recording player for viewing AML (Acute Myeloid Leukemia) multi-omics analysis pipeline demonstrations. Built with asciinema player and featuring a modern, customizable interface.

## Features

- **Multiple Cast Files**: 12 recordings showing different parts of the AML-omics analysis pipeline
- **Playback Controls**: Play/pause, speed adjustment (0.5x to 5x), seek forward/backward
- **Theme Selection**: Multiple terminal themes (asciinema, tango, solarized, monokai)
- **Terminal Customization**: Adjustable terminal size (columns/rows)
- **Keyboard Controls**:
  - `j` or `J`: Play/Pause
  - `h` or `H`: Seek backward 3 seconds
  - `l` or `L`: Seek forward 3 seconds
- **Responsive Design**: Optimized for different screen sizes
- **JetBrains Mono Font**: Professional monospace font with Nerd Font icons

## Quick Start

### Option 1: Simple HTTP Server (Recommended)

```bash
# Start a local web server
python3 -m http.server 8000

# Open in browser
open http://localhost:8000/player.html
```

### Option 2: Node.js Server

```bash
# Install a simple HTTP server
npm install -g http-server

# Start server
http-server -p 8000

# Open in browser
open http://localhost:8000/player.html
```

### Option 3: Using Live Server (VS Code)

1. Install the "Live Server" extension in VS Code
2. Right-click on `player.html`
3. Select "Open with Live Server"

## Cast Files

The player includes 12 recordings demonstrating the AML-omics pipeline:

| File             | Description                           | Size   |
| ---------------- | ------------------------------------- | ------ |
| `part-01.cast`   | Environment setup and data download   | 15 MB  |
| `part-02.cast`   | Data preprocessing                    | 19 MB  |
| `part-03.cast`   | Quality control and feature selection | 59 MB  |
| `part-04.cast`   | Multi-omics integration               | 23 MB  |
| `part-05.cast`   | Unsupervised clustering               | 16 MB  |
| `part-06.cast`   | Clinical validation                   | 7.8 MB |
| `part-07.cast`   | Pathway analysis                      | 14 MB  |
| `part-08.cast`   | Drug sensitivity prediction           | 2.9 MB |
| `part-09.cast`   | Visualization generation              | 15 MB  |
| `part-10.cast`   | Report generation                     | 9.9 MB |
| `part-11.cast`   | Complete pipeline run                 | 11 MB  |
| `part-test.cast` | Test recording                        | 13 KB  |

## File Structure

```
cast/
├── player.html              # Main player interface
├── cast-files.json          # List of available cast files
├── README.md                # This file
├── nerdfonts-minimal/       # Font files
│   ├── JetBrainsMonoNerdFontMono-Regular.ttf
│   └── SymbolsNerdFontMono-Regular.ttf
└── *.cast                   # Terminal recording files
```

## Browser Compatibility

- **Chrome/Chromium**: Full support
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support

## Troubleshooting

### Player not loading

- Ensure you're serving the files over HTTP/HTTPS (not file://)
- Check browser console for JavaScript errors
- Verify all cast files are present

### Fonts not displaying correctly

- Ensure the `nerdfonts-minimal/` directory contains the font files
- Check browser font loading in developer tools

### Playback issues

- Try refreshing the page
- Check if the cast file is corrupted
- Use browser developer tools to check network requests

## Development

The player is built with vanilla HTML, CSS, and JavaScript. Key dependencies:

- **asciinema-player**: v3.0.1 (loaded from CDN)
- **JetBrains Mono**: v4.5.0 (loaded from CDN)
- **Nerd Fonts**: Local files for icon support

### Customization

You can modify the appearance by editing the CSS in `player.html`:

- **Colors**: Update the CSS custom properties
- **Layout**: Modify the grid and flexbox layouts
- **Themes**: Add new terminal themes in the theme selector
- **Fonts**: Replace font files in the `nerdfonts-minimal/` directory

## About AML-Omics Pipeline

This cast player demonstrates a comprehensive AML (Acute Myeloid Leukemia) multi-omics analysis pipeline that:

1. Downloads TCGA-LAML data
2. Performs quality control and preprocessing
3. Integrates multiple omics data types (RNA-seq, methylation, mutations)
4. Identifies patient subtypes using unsupervised clustering
5. Validates findings with clinical data
6. Performs pathway enrichment analysis
7. Predicts drug sensitivity

The pipeline uses advanced bioinformatics tools including MOFA2 for multi-omics integration, consensus clustering for robust subtype identification, and comprehensive survival analysis for clinical validation.

## Credits

- **Asciinema Player**: Terminal recording playback
- **JetBrains Mono**: Professional monospace font
- **Nerd Fonts**: Extended glyph support
- **Created by**: Hsieh-Ting Lin 🦎

## License

This project is part of the AML-omics analysis pipeline research.
