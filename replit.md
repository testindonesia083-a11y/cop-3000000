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

### Latest Updates - All Tasks Completed ✅
1. **Hero Image Restored**: Reverted "Atividades e conteúdos exclusivos" section to original animated GIF (Gif-PV-COP-30.gif)
2. **Extended Yellow Background**: CSS added to extend #FFF4B0 background across entire section 4d63732
3. **Gabarito Image Updated**: Replaced image below "Gabarito incluso" with image_1762812634794.png
4. **FAQ Accordion Arrows**: Added Font Awesome chevron icons (▼/▲) to FAQ accordion with rotation animation
5. **Bonus Carousel Navigation**: Added styled navigation arrows (◄/►) to bonus content carousel
6. **Star Ratings Fixed**: Ensured all testimonial stars display in yellow (#FFB642) across all review sections
7. **7-Day Money-Back Guarantee**: New prominent section with gradient background (#FFB642-#FF8C42) inserted before "VEJA COMO É SIMPLES O ACESSO!"
8. **Installment Payment Info**: 
   - Pacote Básico: "ou 3x de R$ 4,97"
   - Pacote Completo: "ou 6x de R$ 4,98"
9. **Enhanced Complete Package**: Added 8 benefits including:
   - Suporte Personalizado
   - Bônus Exclusivos (3 materiais)
   - Atualizações Gratuitas
   - Certificado Digital
   - Material Editável (Word)
   - Suporte por WhatsApp
   - Acesso VITALÍCIO
10. **Smooth Scroll Functionality**: All "COMPRAR AGORA" buttons now smoothly scroll to package selection (#pacotes)
11. **Responsive Design**: Mobile-optimized CSS for pricing cards, installment text, and all interactive elements

## Notes
- This is a **static export** - no backend functionality or WordPress features are available
- Some interactive WordPress features (forms, comments, etc.) may not work as expected
- The page is optimized for display only, not for editing
- JavaScript console may show errors from WordPress plugins attempting to make API calls
- All custom styles are in the `<style id="custom-cop30-styles">` section of index.html
