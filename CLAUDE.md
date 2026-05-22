# Portfolio — Claude Rules

## Project
Sarah's personal developer portfolio. Built with React, TypeScript, Vite, and Tailwind CSS v4.

## Stack
- React 19 + TypeScript
- Vite 8
- Tailwind CSS v4 (via `@tailwindcss/vite` — no `tailwind.config.js`)
- No backend

## Design
- **Heading font:** Cabinet Grotesk (bold, 700/800 weights) — from Fontshare
- **Body font:** Manrope (400/500/600) — from Google Fonts
- **Style:** Bold, dark, expressive — deep purple gradient background, strong typography, confident layout
- **Colors:** Dark base (~#16102a), accent lavender/purple (~#c084fc), white text
- Dark mode is the primary mode

## Sections
1. **Hero** — name, title, short intro, blurry gradient background
2. **About** — background, skills, tech stack
3. **Projects** — cards with title, description, links
4. **Contact** — links (email, GitHub, LinkedIn)

## Component Structure (Atomic Design)

```
src/
├── components/
│   ├── atoms/        # Button, Tag, Badge, IconLink
│   ├── molecules/    # ProjectCard, NavItem, SkillBadge
│   └── organisms/    # Navbar, HeroSection, ProjectGrid, ContactSection
├── App.tsx
├── App.css
├── index.css
└── main.tsx
```

One file per component. Export as default from the component file directly.

## Rules

### Styling
- Tailwind utility classes only — no new CSS files unless absolutely necessary
- No hardcoded color or spacing values — use Tailwind theme tokens or CSS custom properties
- Mobile-first responsive design
- No external UI libraries (no shadcn, MUI, etc.) — build from scratch

### TypeScript
- No `any` — ever
- No type assertions (`as`) unless provably safe
- Define prop types with interfaces above the component

### Imports
- Sort imports alphabetically by module path
- React imports first, then external libraries, then internal (`./`, `../`)

### HTML & Accessibility
- Semantic HTML — `<nav>`, `<section>`, `<article>`, `<header>`, `<main>`
- All images must have meaningful `alt` text (or `alt=""` if decorative)
- Interactive elements must be keyboard-navigable
- No `eslint-disable` comments — fix the underlying issue

### General
- Single-page app with anchor navigation — no router needed
- Keep animations subtle — CSS transitions only, no animation libraries
- No documentation changes unless explicitly requested
- Never commit or push changes unless explicitly asked to do so
