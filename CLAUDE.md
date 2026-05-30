# Personal Site — CLAUDE.md

## What This Is
A personal one-page portfolio website with a cyberpunk / Edgerunners aesthetic.
Single file project: `index.html` + `bg_video.mp4` in the same folder.
No framework, no build tools, no npm. Pure HTML/CSS/JS only.

---

## Stack
- **Structure:** Single `index.html` — keep everything in one file unless explicitly told otherwise
- **Fonts:** Orbitron (display/hero), Share Tech Mono (mono/labels), Rajdhani (body) — loaded via Google Fonts
- **Animations:** CSS-first. GSAP allowed via cdnjs CDN if CSS can't do it
- **No:** React, Vue, Tailwind, npm, build steps, or any external dependencies beyond Google Fonts + cdnjs

---

## Design System

### Colors (CSS variables — never hardcode these)
```
--yellow:       #f5e642   ← primary accent, CTAs, hero name
--yellow-dim:   #c4b82e   ← hover states for yellow elements
--teal:         #00e5c8   ← secondary accent, status, links
--teal-dim:     #00a895
--red:          #ff3c5f   ← danger, glitch effect only
--dark:         #050810   ← page background
--glass-bg:     rgba(8, 14, 28, 0.55)
--glass-border: rgba(245, 230, 66, 0.18)
--glass-border-strong: rgba(245, 230, 66, 0.4)
--text-primary: #e8eaf0
--text-muted:   rgba(232, 234, 240, 0.5)
```

### Typography
- `--font-display: 'Orbitron', monospace` → hero name, section titles, stat values
- `--font-mono: 'Share Tech Mono', monospace` → labels, tags, nav, badges, code-like UI
- `--font-body: 'Rajdhani', sans-serif` → paragraphs, descriptions

### Glass Panels
All cards and panels use:
```css
background: var(--glass-bg);
border: 1px solid var(--glass-border);
backdrop-filter: blur(20px);
```
Top edge highlight: `linear-gradient(90deg, transparent, var(--yellow), transparent)` at 0.5 opacity.

---

## Aesthetic Rules — NEVER BREAK THESE
- Never use Inter, Roboto, Arial, or system fonts
- Never use purple gradients or generic "AI aesthetics"
- Never remove the scanlines, grain, or vignette overlays
- Never remove the custom cursor
- Never remove the video background
- Keep all section labels prefixed with `// ` and font-family mono
- Buttons use `clip-path: polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%)` — the angled cut is intentional
- Corner accents on cards (yellow L-shaped top-right corner on hover) must stay

---

## Animations & Motion
- Scroll reveal: `.reveal` class + IntersectionObserver — already wired, just add the class
- Card tilt: 3D perspective on mousemove — keep it subtle (max 6deg)
- Glitch on hero name: fires every ~6s, CSS keyframes only
- Scanlines: animated CSS repeating-gradient
- Film grain: SVG feTurbulence, animated position
- Custom cursor: yellow dot + lagging ring, uses requestAnimationFrame loop
- Status ticker in nav: cycles through phrases every 3s

---

## Sections (in order)
1. **Nav** — fixed, glassmorphism, logo + links + status dot
2. **Hero** — full viewport, glitch name, tagline, CTA buttons, badges, stat cards (right side), scroll hint
3. **About** — 2-column grid: text + skill grid left, character card right
4. **Work** — project cards in bento grid (first card spans 2 cols)
5. **Contact** — centered, dramatic heading, link buttons
6. **Footer** — single line, copy + sys status

---

## Content Placeholders (things the user still needs to fill in)
- `YOUR NAME` in hero h1
- Photo in the about character card (`.char-box`)
- Project titles, descriptions, and tags in `#work`
- Social/contact links (email, Behance, Twitter, LinkedIn)
- Location in nav status if not Ankara

---

## Model
Use **claude sonnet** for all tasks in this project.

---

## Prompting Tips for This Project
- Say "use visual-fix skill" when something looks broken or off
- Say "use impeccable skill" for a final polish pass before calling a section done
- Always describe what you want visually, not technically — e.g. "make the hero feel more dramatic" not "increase font-size to 140px"
- After any edit, say "check for mobile too" — the site should work on phones
