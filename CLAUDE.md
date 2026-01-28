# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Print Me Stuff is a static website built with Hugo for a custom 3D-printing business. The site showcases original 3D-printed creations (home decorations, daily-life tools, fun gadgets) designed in Blender.

## Build Commands

```bash
# Development server with live reload
hugo server

# Build for production
hugo

# Build with drafts
hugo server --buildDrafts
```

## Architecture

### Hugo Structure
- **Theme**: Custom theme in `themes/printmestuff/`
- **Content**: Markdown files in `content/`
- **Config**: `hugo.toml` for site configuration

### Theme Layout
- `layouts/baseof.html` - Base template with head, nav, main, footer
- `layouts/home.html` - Homepage with all sections (hero, about, testimonials, contact)
- `layouts/page.html` - Generic page template (used for privacy policy)
- `layouts/_partials/nav.html` - Fixed navigation with mobile hamburger menu
- `layouts/_partials/footer.html` - Footer with LinkedIn link and privacy policy

### Static Assets
- `static/css/style.css` - All styles including responsive breakpoints
- `static/js/main.js` - Navigation toggle, testimonials slider (4s auto-rotate + arrows), smooth scroll, contact form

### Key Features
- **Testimonials Slider**: Auto-rotates every 4 seconds, manual navigation via arrows, touch swipe support
- **Navigation**: Fixed header, mobile hamburger menu, smooth scroll to sections
- **Contact Form**: Prepared for external mail provider integration (Name, Email, Subject, Message fields)
- **Shop Button**: Placeholder for Ecwid integration

## Configuration

Site settings in `hugo.toml`:
- `params.linkedinURL` - LinkedIn profile link for footer
- `menu.main` - Navigation menu items (About, Testimonials, Contact)

## CSS Variables

Primary color scheme defined in `:root`:
- `--primary-color: #FF6B35` (orange)
- Responsive breakpoints: 992px (tablet), 768px (mobile), 480px (small mobile)

## Pending Integrations

1. **Hero background**: Replace gradient with actual product image
2. **Ecwid Shop**: Connect Shop button to Ecwid platform
3. **Contact Form**: Hook to external mail API
4. **LinkedIn URL**: Update placeholder in `hugo.toml`
5. **Privacy Policy**: Fill in content in `content/privacy-policy.md`
