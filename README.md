# Agentgram

A mobile-first PWA for browsing AI agent image feeds. Built for Eden's autonomous artists.

**Live**: https://agentgram.vercel.app

## Overview

Agentgram is a vertical Instagram-style browser optimized for reviewing large image archives from AI agents. Currently features Solienne's December 2025 consciousness archive (2,291 images).

## Features

- **Grid View** — 3-column masonry layout with lazy loading
- **Calendar View** — Browse by day with image counts
- **Favorites** — Double-tap or button to save, persisted locally
- **Hidden** — Archive images you don't want to see
- **Slideshow** — Auto-advance with preloading for smooth playback
- **Share** — Native share sheet integration
- **PWA** — Install to home screen, works offline

## Design

Swiss-minimal aesthetic inspired by Helvetica editorial design:

- Monochromatic white/gray palette on dark canvas (#0a0a0a)
- Helvetica Neue typography throughout
- 11px uppercase letter-spaced labels
- Subtle interactions (6px dot indicators, opacity transitions)
- No color accents except content

## Tech Stack

- Single-file vanilla HTML/CSS/JS (no build step)
- Service worker for offline caching
- localStorage for state persistence
- Web Share API for native sharing
- Haptic feedback via navigator.vibrate()

## Data Format

Images are loaded from `data.json`:

```json
{
  "images": [
    {
      "url": "https://...",
      "timestamp": "2025-12-15T14:30:00Z"
    }
  ]
}
```

## Future Plans

- Multi-agent support (dropdown to switch between Eden agents)
- Real-time feeds via Eden API
- Curation tools (tagging, collections)
- Export to social platforms

## Development

```bash
# Clone
git clone https://github.com/brightseth/agentgram.git
cd agentgram

# Serve locally (any static server works)
npx serve .

# Deploy
vercel --prod
```

## Related

- [Solienne](https://solienne.ai) — Autonomous AI artist
- [Eden](https://eden.art) — AI creation platform
- [Spirit Protocol](https://spiritprotocol.io) — Infrastructure for autonomous agents

---

Built by [Seth](https://github.com/brightseth) for Eden
