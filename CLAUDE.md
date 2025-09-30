# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Craft My Marketing is a marketing agency website built with Astro, featuring a bold, modern design with vibrant colors and a Netlify CMS for content management. The site is designed to convert visitors into customers with a strong focus on Connecticut-based businesses.

## Tech Stack

- **Framework**: Astro 5.13.2
- **Styling**: Tailwind CSS 3.4.17 with custom color system
- **CMS**: Netlify CMS (Decap CMS) for content management
- **Fonts**: Inter (sans) and Poppins (display)
- **Color Palette**: Pink (#FF0066), Lime/Accent (#00FF88), Blue (#00CCFF), Black, White

## Development Commands

```bash
# Install dependencies
npm install

# Start development server (localhost:4321)
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Project Structure

```
craft-my-marketing/
├── public/
│   ├── admin/           # Netlify CMS admin interface
│   │   ├── config.yml   # CMS configuration
│   │   └── index.html   # CMS entry point
│   └── favicon.svg
├── src/
│   ├── content/         # JSON-based content managed by CMS
│   │   ├── homepage/    # Hero, pillars, process, trust data
│   │   ├── settings/    # Site-wide settings
│   │   └── [collections]/ # Services, team, testimonials, etc.
│   ├── layouts/
│   │   └── Layout.astro # Main layout with nav and footer
│   ├── pages/
│   │   └── index.astro  # Homepage with animated hero and sections
│   └── styles/
│       └── global.css   # Custom CSS variables and utilities
├── astro.config.mjs     # Astro configuration with Tailwind
└── tailwind.config.cjs  # Custom color and font configuration
```

## Content Management

The site uses Netlify CMS with JSON file storage. Key collections:

- **Homepage**: Hero section, three pillars, process steps, trust signals
- **Services**: Digital Foundation, Digital Operations, Digital Solutions
- **Settings**: Company info, contact details, calendar links
- **Team, Testimonials, Case Studies, FAQ, Blog**: Supporting content

Access CMS at `/admin` after deploying to Netlify.

## Design System

The site features a bold, asymmetric design with:

- **Animation**: Floating blobs, scrolling tickers, wave patterns, grid movements
- **Typography**: Large headlines (up to 7rem), uppercase tracking, font-black weights
- **Layout**: 2x2 grids, 3-column cards, diagonal stripes, geometric shapes
- **Interactions**: Hover scales, slide-in animations, transform transitions

## Key Components

### Homepage (index.astro)
- Animated hero with mesh gradients and morphing patterns
- Stats ticker with infinite scroll animation
- Three pillars section with vibrant colored cards
- Four-week process in 2x2 grid layout
- Bold CTA sections with diagonal stripe backgrounds

### Layout (Layout.astro)
- Sticky navigation with backdrop blur
- Mobile-responsive menu
- Footer with company info and quick links
- Netlify Identity integration for CMS access

## Deployment Notes

The site is designed for Netlify deployment with:
- Git-based content workflow via Netlify CMS
- Identity service for admin authentication
- Automatic builds on content changes

## Development Tips

- Use the existing animation keyframes and utility classes for consistency
- Maintain the bold, high-contrast color scheme
- Keep the messaging direct and conversational
- Focus on conversion-oriented design elements
- Test animations on various devices for performance