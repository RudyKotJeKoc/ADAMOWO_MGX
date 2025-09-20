# Radio Adamowo - AI Coding Agent Instructions

## Project Overview

Radio Adamowo is a Polish educational Progressive Web App (PWA) focused on analyzing toxic relationships and psychological manipulation. It combines a web radio with 546 music tracks across 4 categories, 16 educational podcasts, and interactive educational tools.

## Architecture & Tech Stack

- **Core**: Vanilla HTML5/CSS/JavaScript (no frameworks)
- **Build Tool**: Vite 6.3.5 with PNPM package management
- **PWA**: Service Worker (`sw.js`) with comprehensive caching strategy
- **Audio**: Web Audio API + HLS.js for streaming capabilities
- **Styling**: Custom CSS with Tailwind-like utility classes + CSS custom properties

## Critical File Structure

```
├── index.html              # Single-page application entry point
├── script.js               # Main application logic (618 lines)
├── style.css               # All styles with PWA animations (546 lines)
├── sw.js                   # Service Worker with multi-cache strategy
├── playlist.json           # Music catalog (546 tracks)
├── public/data/playlist.json # Enhanced playlist with metadata
├── manifest.json           # PWA configuration
└── vite.config.js          # Build configuration
```

## Key Development Patterns

### 1. Audio Management System
- **Dual playlist structure**: Root `playlist.json` (simple) + `public/data/playlist.json` (enhanced metadata)
- **Category-based organization**: `ambient`, `disco`, `hiphop`, `barbara`, `kids`
- **Web Audio API integration**: Visualizer canvas, gain control, audio context management
- **HLS streaming support**: Uses HLS.js CDN for live stream capabilities

### 2. PWA Implementation
- **Multi-layer caching**: Static, dynamic, and versioned cache strategies in `sw.js`
- **Install banner**: Custom PWA install prompt with wave light animations
- **Offline-first**: Comprehensive service worker handles 546 audio files + assets
- **Media session API**: System-level media controls integration

### 3. Polish Language Context
- **Content language**: All UI text, comments, and documentation in Polish
- **Cultural context**: Educational content about "narcystyczna przemoc" (narcissistic abuse)
- **Accessibility**: ARIA labels in Polish, semantic HTML structure

### 4. CSS Architecture
- **CSS Custom Properties**: `--color-primary` (#f59e0b amber), `--color-secondary` (#dc2626 red)
- **Special typography**: "Special Elite" Google Font for headers (`special-elite` class)
- **Advanced animations**: Complex keyframe animations for PWA banner, studio backgrounds
- **Studio theming**: Background images from `public/images/studio/studio-1.png`

## Development Workflows

### Build Process
```bash
pnpm dev          # Development server on :3000
pnpm build        # Production build to dist/
pnpm preview      # Preview build on :4173
```

### Asset Management
- **Music files**: Organized in `music/` with subdirectories by genre
- **Podcasts**: Educational content in `audio/` directory (16 files)
- **Images**: Studio photos in `public/images/studio/`
- **External assets**: CDN resources (HLS.js, Google Fonts) cached by SW

### Testing PWA Features
- Use Chrome DevTools > Application > Service Workers
- Test install prompt on mobile devices
- Verify offline functionality with Network throttling
- Check cache strategies in Application > Storage

## Code Conventions

### JavaScript Patterns
- **DOM-first approach**: Heavy use of `document.getElementById()` and event delegation
- **State management**: Global variables for audio context, playlist state, HLS instance
- **Error handling**: Graceful fallbacks for audio API failures
- **Async/await**: Modern promise handling for PWA install prompts

### CSS Methodology
- **Utility-first influenced**: Mix of custom classes and utility-like patterns
- **Component-based naming**: `.studio-gallery-item`, `.pwa-banner-content`
- **Animation-heavy**: Multiple `@keyframes` for interactive elements
- **Mobile-first responsive**: Breakpoints using `md:` prefixes

### HTML Structure
- **Semantic sections**: Clear content hierarchy with `<main>`, `<section>`, `<nav>`
- **Accessibility focus**: Comprehensive `aria-label` attributes
- **Progressive enhancement**: Core functionality works without JavaScript

## Integration Points

### External Dependencies
- **HLS.js**: Stream handling for live radio functionality
- **Google Fonts**: Special Elite typeface for branding
- **External images**: CDN-hosted favicons and assets

### Media Pipeline
- **Playlist sync**: Root and public playlist files must stay synchronized
- **Category mapping**: Music files organized by directory AND JSON category field
- **Audio formats**: Exclusively MP3 for broad browser compatibility

## Common Tasks

### Adding New Music
1. Place MP3 files in appropriate `music/[category]/` directory
2. Update both `playlist.json` and `public/data/playlist.json`
3. Increment SW cache version in `sw.js`

### PWA Updates
1. Modify `manifest.json` for app metadata changes
2. Update cache version and static assets list in `sw.js`
3. Test install flow and offline functionality

### Styling Changes
- Use existing CSS custom properties for color consistency
- Follow component-based class naming convention
- Test animations across different devices and browsers
- Verify PWA banner animations work correctly

## Polish Content Context

When working on content, understand this is an educational platform about recognizing manipulation patterns. Maintain the serious, analytical tone while preserving the creative "radio station" metaphor. All user-facing text should be in Polish and culturally appropriate for Polish audiences discussing psychological abuse topics.