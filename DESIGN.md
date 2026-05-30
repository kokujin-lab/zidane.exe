---
name: Operator Profile
description: A Night City netrunner's HUD as a personal designer portfolio.
colors:
  yellow: "#f5e642"
  yellow-dim: "#c4b82e"
  teal: "#00e5c8"
  teal-dim: "#00a895"
  red: "#ff3c5f"
  dark: "#050810"
  ink-on-yellow: "#0a0c14"
  text-primary: "#e8eaf0"
  text-muted: "#e8eaf080"
  glass-bg: "#080e1c8c"
  glass-border: "#f5e6422e"
  glass-border-strong: "#f5e64266"
typography:
  display:
    fontFamily: "Orbitron, monospace"
    fontSize: "clamp(52px, 9vw, 120px)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Orbitron, monospace"
    fontSize: "clamp(28px, 4vw, 48px)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: "normal"
  title:
    fontFamily: "Orbitron, monospace"
    fontSize: "18px"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "normal"
  body:
    fontFamily: "Rajdhani, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.7
    letterSpacing: "0.05em"
  label:
    fontFamily: "Share Tech Mono, monospace"
    fontSize: "11px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0.15em"
rounded:
  sharp: "0"
  full: "9999px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "16px"
  card: "28px"
  section: "100px"
  gutter: "48px"
components:
  button-primary:
    backgroundColor: "{colors.yellow}"
    textColor: "{colors.ink-on-yellow}"
    rounded: "{rounded.sharp}"
    padding: "14px 32px"
  button-primary-hover:
    backgroundColor: "#fff7a0"
    textColor: "{colors.ink-on-yellow}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.sharp}"
    padding: "13px 31px"
  button-ghost-hover:
    textColor: "{colors.teal}"
  card-glass:
    backgroundColor: "{colors.glass-bg}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.sharp}"
    padding: "{spacing.card}"
  badge:
    backgroundColor: "#00000080"
    textColor: "{colors.text-muted}"
    rounded: "{rounded.sharp}"
    padding: "5px 14px"
---

# Design System: Operator Profile

## 1. Overview

**Creative North Star: "The Operator Terminal"**

This is not a portfolio that happens to look cyberpunk. It is a Night City netrunner's heads-up display that happens to be a portfolio. Every surface behaves like a panel in an operator's interface: glass readouts floating over a live video feed, status tickers cycling, section labels prefixed with `//` like console output, and the hero name glitching as if the signal can't quite hold it steady. The interface is diegetic. The visitor isn't reading a résumé, they're jacked into someone's profile.

The mood is **electric, defiant, cinematic**. Depth comes from a dark, near-black field (`#050810`) lit by two neon signals: an aggressive electric yellow and a colder teal. Atmosphere is structural, never decorative, the looping video, animated scanlines, film grain, vignette, and a custom dual-layer cursor are load-bearing parts of the identity and must never be stripped "for cleanliness." Red exists only as a wound: glitch interference and danger, nothing else.

This system explicitly rejects the **corporate / LinkedIn-bland** safe zone (beige, forgettable, personality-free), the **generic SaaS template** (Inter, soft purple gradients, rounded cards, default "modern minimal"), and the **all-white minimalist designer portfolio** (whitespace and thin gray type with no point of view). Loud is the brand. The only hard constraint on the loudness is legibility: the name, the role, the work, and the contact path must always land instantly.

**Key Characteristics:**
- Diegetic terminal/HUD framing: `//` labels, system readouts, status tickers
- Near-black canvas with twin neon accents (yellow primary, teal secondary)
- Glass panels over a live video background; sharp angled geometry, never rounded
- Motion as identity: glitch, scanlines, grain, lagging cursor, scroll reveals
- Orbitron display set huge and tight; mono for every label and code-like element

## 2. Colors

A dark HUD palette: a single near-black field lit by two saturated neon signals, with red reserved as pure danger.

### Primary
- **Signal Yellow** (`#f5e642`): The dominant operator accent. CTAs, the hero name, stat values, panel top-edge highlights, corner accents, the custom cursor. This is the color the eye is pulled to first. **Hover Yellow** (`#c4b82e`) and a brightened press tint (`#fff7a0`) handle interactive states.

### Secondary
- **Signal Teal** (`#00e5c8`): The second channel. Status indicators ("ONLINE", the pulsing dot), links, in-text emphasis (`<em>`), accent words in headings, secondary-action hover. **Teal Dim** (`#00a895`) is its recessed variant. Teal answers yellow; the two never blur into each other's role.

### Tertiary
- **Glitch Red** (`#ff3c5f`): Danger and interference only. It appears exclusively in the glitch effect's red channel. **The Red-Is-A-Wound Rule:** red is never used for normal UI, never for text, never for accents. If red reads as "decoration," it's wrong.

### Neutral
- **Operator Ink** (`#050810`): The page background. A near-black with a faint blue cast, not pure `#000`.
- **HUD White** (`#e8eaf0`): Primary text and headings. A cool off-white, never pure white.
- **Muted Signal** (`#e8eaf080`, HUD White at 50%): Secondary/body-supporting text, labels, captions. A transparency of the text color, never a flat gray.
- **Ink On Yellow** (`#0a0c14`): The only "dark text" use, sits on yellow button fills for maximum contrast.
- **Glass Fill** (`#080e1c8c`): Panel backgrounds, `rgba(8,14,28,0.55)` over `backdrop-filter: blur(20px)`.
- **Glass Border** (`#f5e6422e`) and **Glass Border Strong** (`#f5e64266`): yellow at low alpha for resting and hover/active panel edges.

### Named Rules
**The Two-Signal Rule.** Yellow leads, teal answers, and they never swap jobs: yellow is the thing you act on, teal is the thing that's alive (status, links, motion). A screen using teal for a primary CTA or yellow for a status dot is off-brand.

**The Gray-Is-Banned Rule.** There is no flat gray in this system. "Muted" text is always HUD White at reduced opacity, so it stays tinted to the canvas. Never introduce a neutral `#888`-class gray.

## 3. Typography

**Display Font:** Orbitron (with `monospace` fallback)
**Body Font:** Rajdhani (with `sans-serif` fallback)
**Label/Mono Font:** Share Tech Mono (with `monospace` fallback)

**Character:** A geometric, wide, almost mechanical display face (Orbitron) for shouting; a tall, condensed humanist sans (Rajdhani) for readable body; and a true monospace (Share Tech Mono) for everything that should read like console output. The contrast axis is shape and width, not just weight, so the three never blur together.

### Hierarchy
- **Display** (Orbitron 900, `clamp(52px, 9vw, 120px)`, line-height 0.9, letter-spacing -0.02em): The hero name only. Set deliberately huge; the size is part of the loudness. The glitch layers ride on this.
- **Headline** (Orbitron 700, `clamp(28px, 4vw, 48px)`, line-height 1.1): Section titles ("Selected Projects", about heading), with teal `.accent` spans for emphasis words.
- **Title** (Orbitron 700, 18–24px): Project card titles, character-card stat values.
- **Body** (Rajdhani 400, 17px, line-height 1.7, letter-spacing 0.05em): Paragraphs and descriptions. Cap measure around 65–75ch; `<strong>` lifts to HUD White, `<em>` shifts to teal.
- **Label** (Share Tech Mono, 10–12px, letter-spacing 0.1–0.2em, UPPERCASE): Every code-like element, nav links, section eyebrows, badges, stat labels, status ticker. The `//` prefix and `> ` hover markers live here.

### Named Rules
**The Console-Label Rule.** Every label, nav item, tag, badge, and section eyebrow is Share Tech Mono, uppercase, tracked, and most carry a `//` or `> ` prefix. This is the deliberate, named terminal voice of the system, not generic eyebrow scaffolding; it is the diegetic frame and is applied consistently, never half-way.

**The Display-Is-For-Shouting Rule.** Orbitron is reserved for the hero name, section titles, and numeric stat values. Never set body copy or long strings in Orbitron; at width it becomes unreadable.

## 4. Elevation

This system conveys depth through **atmospheric layering, not drop shadows**. There are effectively no `box-shadow` cards. Instead, depth is built from a fixed z-stack of full-bleed atmosphere layers behind translucent glass: the video sits at `z-index: -2`, scanlines at `-1`, vignette at `0`, grain at `1`, and content sections at `2`, with nav/cursor above. Glass panels (`backdrop-filter: blur(20px)` over a 55%-opaque fill) read as floating because the live video and grain are visibly blurred through them, not because they cast shadows.

### Shadow Vocabulary
- **Neon glow** (`box-shadow: 0 0 8px var(--teal)`): Used only on the status dot, a signal bloom, not an elevation shadow. This is the single legitimate `box-shadow` in the system.

### Named Rules
**The No-Drop-Shadow Rule.** Surfaces never cast soft gray drop shadows; that reads as 2014 Material and breaks the HUD illusion. Depth comes from `backdrop-filter` blur, the top-edge yellow gradient highlight (`linear-gradient(90deg, transparent, var(--yellow), transparent)` at 0.5 opacity), and the layered atmosphere behind glass.

**The Ghost-Card Ban.** Never pair a 1px border with a wide soft `box-shadow` on the same element. Panels get a glass border OR a glow, never a generic lifted-card shadow.

## 5. Components

### Buttons
- **Shape:** Sharp with an intentional angled cut, never rounded. Every button uses `clip-path: polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%)`, the diagonal corners are a signature, not an accident.
- **Primary:** Solid Signal Yellow fill with Ink-On-Yellow text (`#0a0c14`), mono uppercase, `14px 32px` padding. Hover brightens to `#fff7a0` and lifts `translateY(-2px)`; press gives `scale(0.97)` feedback.
- **Ghost:** Transparent with a strong glass border and HUD White text, `backdrop-filter: blur(8px)`, `13px 31px`. Hover shifts border and text to teal and lifts; press gives `scale(0.97)`.
- **Easing:** Interactive transitions use `--ease-out: cubic-bezier(0.23, 1, 0.32, 1)`; press feedback is fast (~100ms).

### Chips / Badges / Tags
- **Style:** Mono uppercase, tracked, on a near-black fill (`rgba(0,0,0,0.3)`) with a glass border; sharp corners, `5px 14px`.
- **State:** An `.active` badge swaps border and text to teal (e.g. "▶ AVAILABLE FOR WORK"). Project tags are the same family with thinner padding.

### Cards / Containers (Glass Panels)
- **Corner Style:** Sharp (`0` radius). Never rounded.
- **Background:** Glass Fill (`rgba(8,14,28,0.55)`) over `backdrop-filter: blur(20px)`.
- **Top Edge:** A yellow `linear-gradient(90deg, transparent, var(--yellow), transparent)` highlight at 0.5 opacity along the top 1px.
- **Border:** Glass Border at rest; Glass Border Strong on hover.
- **Hover:** `translateY(-4px)` lift, an L-shaped yellow corner accent fades in (top-right), and a faint yellow corner gradient wash appears. On fine-pointer devices a subtle 3D `perspective` tilt tracks the cursor (max 6deg), snapping while tracked and easing back on leave.
- **Internal Padding:** `28px` (project cards), `14–32px` across stat/character cards.

### Navigation
- **Style:** Fixed top bar, `rgba(5,8,16,0.3)` + `blur(12px)`, hairline yellow bottom border. Logo in Orbitron (`// your_name.exe`), links in mono lowercase.
- **States:** Links rest at Muted Signal; hover lifts to HUD White and reveals a teal `> ` prefix. A pulsing teal status dot + cycling mono status ticker sit at the right.
- **Mobile:** Reduced padding; the status ticker is hidden under 600px to keep the bar uncluttered.

### Signature Component: The Glitch Name
The hero name uses a triple-layer glitch: the base yellow text plus two pseudo-element clones (teal and red channels) that clip and offset on a ~6s loop, simulating signal tearing. The red channel here is the one sanctioned use of Glitch Red. This is the centerpiece of "The Operator Terminal" and must survive any redesign.

### Signature Component: The Custom Cursor
A two-part cursor, a solid yellow dot (`mix-blend-mode: difference`) plus a larger ring that lags behind via lerp interpolation. Both are GPU-transform driven. It grows on hover over interactive elements and is disabled on touch devices. It is part of the identity, never removed.

## 6. Do's and Don'ts

### Do:
- **Do** keep every label, nav item, tag, and section eyebrow in Share Tech Mono, uppercase, with `//` or `> ` prefixes. The terminal voice is the brand.
- **Do** use the angled `clip-path` cut on buttons (`polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%)`). The diagonal corner is intentional.
- **Do** build depth with `backdrop-filter` glass, the top-edge yellow highlight, and the layered video/scanline/grain/vignette stack, never drop shadows.
- **Do** keep yellow as the action color and teal as the alive/status color (The Two-Signal Rule).
- **Do** render "muted" text as HUD White at reduced opacity, never a flat gray (The Gray-Is-Banned Rule).
- **Do** preserve the scanlines, film grain, vignette, custom cursor, glitch name, and video background. They are structural identity.
- **Do** use `--ease-out: cubic-bezier(0.23, 1, 0.32, 1)` for transitions and add `scale(0.97)` press feedback to every pressable element.

### Don't:
- **Don't** drift toward corporate / LinkedIn-bland: no beige, no safe, no personality-free layouts. This is the single worst failure mode.
- **Don't** introduce the generic SaaS/startup look: no Inter, no soft purple gradients, no rounded cards, no "modern minimal" defaults.
- **Don't** build the all-white minimalist designer portfolio: thin gray type on white with no point of view is forbidden.
- **Don't** round corners on cards, panels, or buttons. Geometry is sharp; only the cursor, dots, and rings are circular.
- **Don't** use Glitch Red for anything except the glitch effect's red channel. Red is a wound, not an accent.
- **Don't** pair a 1px border with a wide soft `box-shadow` (the ghost-card pattern), and don't add generic lifted-card drop shadows.
- **Don't** set body copy or long strings in Orbitron; reserve the display face for the hero name, section titles, and stat numbers.
- **Don't** let spectacle bury the message: the name, role, work, and contact path must stay instantly legible under all the motion.
