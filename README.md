# Asciinema Cast Player

A web-based terminal recording player for analysis pipeline demonstrations. Built with asciinema player and featuring a modern, customizable interface.

## Features 

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

## Credits

- **Asciinema Player**: Terminal recording playback
- **JetBrains Mono**: Professional monospace font
- **Nerd Fonts**: Extended glyph support
- **Created by**: Hsieh-Ting Lin 🦎

## License

This project is part of the AML-omics analysis pipeline research.
