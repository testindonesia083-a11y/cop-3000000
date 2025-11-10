# COP 30 - Static WordPress Export

## Overview
This project is a static HTML export of a WordPress page about COP 30 (Conference of the Parties), originally from atividadesdepedagogia.com.br. It's served as a standalone static website using Python's built-in HTTP server.

## Project Details
- **Language**: Portuguese (pt-BR)
- **Type**: Static HTML website
- **Original Source**: WordPress/Elementor page export
- **Setup Date**: November 10, 2025

## Project Structure
```
.
├── attached_assets/     # User-uploaded images and assets
│   └── image_1762811901028.png  # COP 30 banner image
├── index.html          # Main HTML file (exported WordPress page)
├── .gitignore          # Python-related ignore patterns
└── replit.md           # This documentation file
```

## Technical Details

### Architecture
- **Server**: Python 3.11 HTTP server (static file serving)
- **Port**: 5000 (configured for Replit webview)
- **Dependencies**: Python's built-in `http.server` module (no external dependencies)

### External Dependencies
The HTML file references many external resources hosted on CDNs and the original WordPress site:
- CSS/JS from atividadesdepedagogia.com.br
- WordPress plugins (Elementor, WooCommerce, etc.)
- Google Fonts
- Various WordPress assets and libraries

**Important**: An internet connection is required for the page to display properly, as most assets are loaded from external sources.

### How It Works
The Python HTTP server serves the static `index.html` file on port 5000. The page includes all necessary inline styles and scripts, with additional resources loaded from external CDNs.

## Development

### Running Locally
The workflow is pre-configured. Simply click the "Run" button, and the server will start automatically on port 5000.

### Manual Start
```bash
python -m http.server 5000
```

## Deployment
The project is configured for Replit's autoscale deployment:
- **Type**: Autoscale (static website)
- **Command**: `python -m http.server 5000`
- No build step required

## Recent Changes (November 10, 2025)
1. **Text Update**: Changed "SUPER OFERTA" to "ESCOLHA SEU PACOTE:"
2. **Button Animation**: Added pulsing animation to "COMPRAR AGORA" buttons using existing pulseGlow keyframes
3. **Image Replacement**: Replaced main GIF banner with new static image (image_1762811901028.png)
4. **Review Stars Fix**: Added CSS styling to display star ratings in testimonials section (gold stars, 18px)
5. **Background Color**: Changed APOSTILA COP 30 section background to light yellow (#FFF4B0) for better visibility

## Notes
- This is a **static export** - no backend functionality or WordPress features are available
- Some interactive WordPress features (forms, comments, etc.) may not work as expected
- The page is optimized for display only, not for editing
- JavaScript console may show errors from WordPress plugins attempting to make API calls
- All custom styles are in the `<style id="custom-cop30-styles">` section of index.html
