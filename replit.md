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
├── attached_assets/            # User-uploaded and generated images
│   ├── image_*.png            # Original COP 30 images
│   └── generated_images/      # AI-generated bonus images
│       ├── Kit_Atividades_Amazônia_Bônus_32c4f4ed.png
│       ├── Certificado_Protetor_Ambiental_Bônus_b11c4736.png
│       └── Guia_Projetos_Sustentáveis_Bônus_dbe577ae.png
├── index.html                 # Main HTML file (exported WordPress page)
├── .gitignore                 # Python-related ignore patterns
└── replit.md                  # This documentation file
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

### Latest Updates - All Enhancements Completed ✅

#### 1. **Carousel Autoplay Verified**
- The PAINEL E CERTIFICADOS carousel was already configured with autoplay (5 seconds)
- Verified: `autoplay: yes`, `autoplay_speed: 5000`

#### 2. **3 Exclusive Bonuses Added** 🎁
- Created new bonus section with AI-generated images
- **Kit Atividades da Amazônia** (Value: R$ 19,90)
  - Activities about Amazon biodiversity, indigenous peoples, and forest preservation
- **Certificado Protetor Ambiental** (Value: R$ 14,90)
  - Customizable environmental protector certificates in high quality
- **Guia de Projetos Sustentáveis** (Value: R$ 24,90)
  - Practical guide with 10 sustainable project ideas for schools
- Total bonus value: R$ 59,70
- Modern CSS grid layout with hover effects and responsive design

#### 3. **Footer Copyright Updated**
- Changed from: "Todos os direitos reservados - Atividades de Pedagogia 2025"
- Changed to: "Todos os direitos reservados - 2025"

#### 4. **5 New FAQ Questions Added**
- Total FAQs increased from 3 to 8
- New questions:
  1. Qual a diferença entre o Pacote Simples e o Completo?
  2. O material é adaptado para quais séries?
  3. Preciso de internet para usar o material?
  4. Posso usar o material em mais de uma turma?
  5. E se eu não gostar do material?

#### 5. **FAQ Accordion Arrows Enhanced**
- CSS added for animated chevron icons (▼/▲)
- Smooth rotation animation on expand/collapse
- Color: #FFB642 (matches theme)

#### 6. **Star Ratings Fixed**
- Ensured all testimonial stars display in yellow (#FFB642)
- Applied to all review sections with Font Awesome icons
- Stars now visible and properly styled

#### 7. **Purchase Notification Popup** 🎉
- Positioned: Top-right corner
- Features:
  - 15 purchase notifications (mostly female names as requested)
  - Random Brazilian cities (São Paulo, Rio, Belém, etc.)
  - Low random minutes (2-8 minutes ago)
  - Only shows "Pacote COP 30 COMPLETO"
  - Appears after 5 seconds, auto-closes after 10 seconds
  - Respects session storage (won't reappear if closed)
  - Cycles every 30-60 seconds
  - Fully responsive for mobile

#### 8. **COP30 Content Section Redesigned** 📖
- Transformed plain bullet list into beautiful card layout
- Features:
  - Icons for each topic (📖 🌍 ✏️ 🦜 🌿 ✅)
  - Individual cards with hover effects
  - Blue gradient background
  - Border-left accent in green
  - Clean, modern typography
  - Fully responsive

### CSS Enhancements
All new styles added to `<style id="custom-cop30-styles">`:
- Purchase popup styles with animations (slideInRight, popupPulse)
- Bonus section grid layout
- Bonus card hover effects
- COP30 content item cards
- Responsive breakpoints for mobile

### JavaScript Enhancements
New functionality added before `</body>`:
- Purchase popup notification system
- Automatic cycling with session storage
- Random notification selection
- Close button functionality

## Notes
- This is a **static export** - no backend functionality or WordPress features are available
- Some interactive WordPress features (forms, comments, etc.) may not work as expected
- The page is optimized for display only, not for editing
- JavaScript console may show errors from WordPress plugins attempting to make API calls
- All custom styles are in the `<style id="custom-cop30-styles">` section of index.html
- All custom JavaScript is before the `</body>` tag in index.html
