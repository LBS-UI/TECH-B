# TechPro B Digital Yearbook

A premium, futuristic digital yearbook — glassmorphism, glowing accents, particle
backgrounds, and cinematic motion, built with plain HTML, CSS, and JavaScript.

## Folder structure

```
/
├── index.html            # Animated welcome / boot sequence → Continue
├── main.html              # Main menu with navigation cards
├── about.html              # Class + school info, mission, vision, credits
├── gallery/
│   └── index.html          # Masonry gallery + lightbox
├── halloffame.html          # Outstanding student profiles
├── messages.html           # Appreciation wall (localStorage persisted)
├── computerroom.html      # Futuristic lab visuals / interactive stations
├── ai-assistant.html      # Redirects to Luminara.html (kept for structure)
├── Luminara.html            # AI assistant chat interface
├── secret-archive.html    # Locked vault + matrix animation
├── assets/
│   ├── css/style.css       # Design tokens, glassmorphism, animation system
│   ├── js/
│   │   ├── main.js          # Particles, nav, reveal-on-scroll, counters, ripple, transitions
│   │   ├── gallery.js       # Masonry render + lightbox
│   │   ├── messages.js      # Message wall render + submit
│   │   └── luminara.js      # Chat logic + typing animation
│   ├── images/               # (empty — currently using hosted placeholder photos)
│   ├── icons/                # (empty — emoji used as icons; swap in SVGs here)
│   └── audio/                 # (empty — reserved for future sound design)
└── README.md
```

## Running it

No build step. Open `index.html` directly in a browser, or serve the folder
with any static server, e.g.:

```
npx serve .
```

## Notes on features

- **Theme persistence**: an accent color (cyan / purple / green / yellow) is
  saved to `localStorage` under `tpb-accent` and re-applied on every page load.
- **Messages wall**: new notes are saved to `localStorage` under
  `tpb-messages` and merged with the seeded quotes on render.
- **Secret Archive**: the demo access code is `2026`. This is a client-side
  gate for atmosphere only — it is not real security. Do not use this pattern
  to protect anything sensitive.
- **Images**: gallery and profile photos currently load from Unsplash /
  Pravatar placeholders. Replace the URLs in `assets/js/gallery.js`,
  `halloffame.html`, and `main.html` with real photos in `assets/images/`
  before publishing.
- **Accessibility**: all interactive cards are keyboard-reachable, focus
  states are visible, and `prefers-reduced-motion` is respected across pages.

## Customizing the palette

All colors live as CSS custom properties at the top of
`assets/css/style.css` (`--cyan`, `--blue`, `--purple`, `--lavender`,
`--green`, `--yellow`, `--navy`, `--black`). Changing them there updates the
whole site.
