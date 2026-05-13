# Culture Wireless Design System

> **Culture Connects.**
> Brand system for Culture Wireless — a telecom committed to closing the digital divide for unserved, underserved, and unconnected communities.

---

## Index

| File / Folder | What's in it |
|---|---|
| `README.md` | This file — brand foundations, content, visual, iconography |
| `colors_and_type.css` | All design tokens — colors, type, spacing, radii, shadows, motion |
| `assets/logos/` | Logo lockups (gradient, white, black, full transparent) |
| `preview/` | Cards rendered into the Design System tab |
| `ui_kits/marketing/` | Marketing-site UI kit (hero, plans, footer, etc.) |
| `SKILL.md` | Skill manifest for use as a Claude/Agent skill |

---

## Brand at a glance

- **Mission** — Connect Everyone.
- **Vision** — Leverage technology to deliver digital opportunities.
- **Purpose** — Create an authentic connection to the communities we serve.
- **Positioning** — Culture Connects.
- **Pillars** — Connect · Empower · Expand
- **Voice** — Authentic · Expert · Connected
- **Values** — Inclusivity · Reliability · Affordability · Honesty · Community
- **Audience** — Unserved · Underserved · Unconnected
- **Archetype mix** — 70% Everyman / 30% Hero
- **Elevator pitch** — *"Culture Wireless® transforms access to technologies that empower a true 'connection' to the communities we serve."*

### Sources

All source material lives in `uploads/`:
- `CULTURE_BRAND_PRESENTATION_FULL.pdf` — 36-slide brand house deck (mission, vision, pillars, voice)
- `Culture Wireless Branding Style Colors.pdf` — Material-3-style semantic color tokens
- `branding-guidelines_1627x3999.png` — Color, icon, type guidelines sheet
- `CULTURE_LOGOS.zip` — Logo PNGs (extracted into `assets/logos/`)
- `CULTURE_PLAN_2425.pdf` — Empty/scanned, no extractable text

---

## Content fundamentals

**Tone:** Authentic, expert, plainspoken. Civic-minded but not preachy. Talks *with* the community, not *at* it.

**Voice mix:** Everyman warmth (70%) with Hero conviction (30%). Lines should feel like a trusted neighbor who also happens to be excellent at their job — not a corporate PR voice and not a startup hype voice.

**Casing:**
- **Display headlines & wordmarks → ALL CAPS** (the logo, slide titles, eyebrows, section headers).
- **Body & UI copy → Sentence case.** Never Title Case in long-form copy.

**Pronouns:** "We" for the brand; "you" for the customer; "our communities" or "the communities we serve" when speaking to constituency. Avoid "users" and "consumers" in customer-facing copy — they're permitted in internal/strategic docs.

**Punchy three-beat structure** (used heavily in the brand house — keep this rhythm):
- *Connect | Empower | Expand*
- *Authentic | Expert | Connected*
- *Unserved | Underserved | Unconnected*

When writing taglines, headers, or value props, lean on this triplet pattern.

**Examples to follow:**
- ✅ "Culture Connects."
- ✅ "Connect everyone."
- ✅ "The internet isn't a luxury. It's a necessity."
- ✅ "Authentic connections to the communities we serve."

**Emoji:** No. Not in marketing, not in product UI. The brand expresses warmth through type, color, and language — not emoji.

**Unicode characters as separators:** Use the bullet `·` (middle dot) between three-beat lists — it matches the rhythm of the brand pillars. Avoid `•`, `—`, `|` for the same purpose in customer copy.

---

## Visual foundations

### Color
- **Deep navy `#33244D`** — the anchor. Backgrounds, headers, body text on light.
- **Purple `#8B69C1`** — primary brand color. Buttons, accents, links.
- **Blue `#77A3FF`** — secondary, often paired with purple in the signature gradient.
- **Yellow `#FFB900`** — tertiary accent. Used sparingly for highlights/CTAs that need to pop off purple.
- **Signature gradient** — `#4F7BFF → #8B69C1 → #B07BC9` (left-to-right blue → purple). This IS the wordmark treatment. Use on hero text, primary CTAs, key data callouts. Never on body copy.
- **Background gradient** — `#33244D → #4F3D7A → #8B69C1` (diagonal). Used as an alternative dark hero background.

### Typography
- **Display: Good Times** — uppercase only. Geometric, telecom-feeling, used for the wordmark, eyebrows, and major headers. Always tracked out (`letter-spacing: 0.04em+`).
- **Body: Kelson Sans** — geometric grotesque, used for everything else.
- **Substitute fallbacks (flagged):** Orbitron (Good Times) and Jost (Kelson) from Google Fonts. **Please supply licensed font files at `fonts/`** to replace these.

### Spacing & rhythm
- 8-point grid (`4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96`).
- Generous vertical rhythm in marketing — sections breathe at 96px+.
- Text content max-width ~640–720px for readability.

### Backgrounds
- **Primary canvas:** white (`#FFFFFF`) or very subtly tinted off-white (`--cw-bg-2`, `#F7F4FB`).
- **Hero / section breaks:** deep navy (`#33244D`) or the diagonal gradient.
- **No hand-drawn illustrations.** No textures or repeating patterns. The brand identity is clean, type-first, with the signal-bar icon as the only repeating motif.
- **Imagery vibe:** warm, people-centered photography of real community members. Slight cool color cast OK to harmonize with purple. Avoid b&w, avoid heavy grain, avoid stock-photo vibes.

### Borders & cards
- **Borders:** 1px, low-saturation (`--cw-border-1`, `#E5DEF0`). Stronger 1px navy for emphasis.
- **Card radius:** 16px (`--cw-radius-lg`) default. Pills (999px) for tags and filter buttons. 8px for tight UI components.
- **Card surface:** white with 1px purple-tinted border + soft shadow. Avoid card-with-colored-left-border-only.

### Shadows
Shadows are soft and cool-toned (rgba navy, not black):
- `--cw-shadow-1` — 1px hairline (subtle separation)
- `--cw-shadow-2` — 4px lift (default cards)
- `--cw-shadow-3` — 12px lift (overlays, modals)
- `--cw-shadow-4` — 24px lift (heroes, drag states)
- `--cw-shadow-glow` — purple glow for primary CTAs and focus rings

### Motion
- Default `240ms cubic-bezier(0.22, 1, 0.36, 1)` (ease-out) for entrances and state changes.
- **Hover:** lighten by ~6% OR add subtle `translateY(-2px)` + shadow lift.
- **Press:** `scale(0.98)` + remove shadow.
- **Focus:** 3px purple outline at 40% opacity.
- No bouncy/springy animations. No fades alone — always pair with subtle motion.

### Layering & blur
- Use blur on overlays only (modals, sheets) — `backdrop-filter: blur(16px)` over a 70% navy tint.
- Avoid frosted glass on top of imagery; brand prefers clean solid surfaces.

---

## Iconography

The brand has **one signature icon**: the **signal-bar wave** — a stack of vertical bars increasing in height, also forming the negative-space "U" / "C" shape inside the wordmark. It represents signal strength, growth, and connection. It is used standalone, in the wordmark, and as the favicon/app icon.

**For all other UI iconography**, use **[Lucide](https://lucide.dev/)** via CDN — it has the right stroke weight (1.5–2px) and rounded line caps that complement the geometric type.

```html
<script src="https://unpkg.com/lucide@latest"></script>
<i data-lucide="wifi"></i>
```

**Substitution flagged:** Lucide is the agent's pick — Culture Wireless does not appear to ship a proprietary icon set. Replace with a brand-approved set if/when one exists.

**No emoji. No unicode glyphs as icons.** The middle-dot `·` is used as a separator only.

---

## Quick start

```html
<link rel="stylesheet" href="colors_and_type.css">
<header style="background: var(--cw-navy); color: var(--cw-white); padding: var(--cw-space-7);">
  <p class="cw-eyebrow" style="color: var(--cw-blue);">Connect · Empower · Expand</p>
  <h1 class="cw-display-lg" style="color: var(--cw-white);">Culture <span class="cw-gradient-text">Connects.</span></h1>
</header>
```
