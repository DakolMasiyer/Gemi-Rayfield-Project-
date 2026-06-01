# Gemi Refinement Plan

## Scope
1. **Main site (`gemi_site/index.html`)** — responsiveness audit + spacing/layout polish
2. **3D drawings (exterior + interior)** — aesthetic uplift + interactive rotation
3. **Architectural drawing (`gemi_arch_plan.html`)** — aesthetic uplift
4. **Concept board + floor plan** — aesthetic uplift

---

## 1 · Main Site (`gemi_site/index.html`) — Responsiveness & Spacing

### Issues found
- Nav links hidden on mobile (≤780px) with no hamburger replacement — blank nav
- Section padding `90px 24px` is fine desktop but needs tighter rhythm on mobile
- `.sec-head` collapses to column on mobile, but `.sec-head p` description loses its margin and just stacks with no breathing room
- `.stats` 2-col on mobile has border logic (`nth-child`) that is brittle — the 3rd/4th stat borders go wrong below 480px
- Benefit boxes (`grid-template-columns: 1fr 1fr 1fr`) have no responsive rule — they stack as overflowing columns on mobile
- Hero `h1` uses `clamp(80px,16vw,200px)` — on very small screens (320px) this is 51px which is fine, but seed mark `::after` position is hardcoded at `top:18px right:2px width:16px height:21px` and will mis-register at small sizes
- Footer `.big` `clamp(24px,4vw,40px)` is fine
- No horizontal scroll guard on the sheet-based drawing pages (exterior, interior, arch)

### Fixes
- Add a minimal hamburger/drawer for mobile nav (pure CSS `:focus-within` toggle, no JS dependency — or a simple `<input type=checkbox>` CSS trick)
- Add 480px breakpoint: stack benefit boxes to 1 col, fix stat borders
- Tighten hero and section padding on mobile
- Make seed mark on hero `h1` scale with `em` units relative to parent font-size
- Add `overflow-x: hidden` to `body` and `max-width: 100vw` guard

---

## 2 · Exterior 3D (`gemi_exterior.html`) — Aesthetic + Rotation

### Aesthetic uplift
- Sky gradient is flat — add more cloud depth, subtle horizon haze
- Building walls (ochre `#cfc6b4`) are too muted — punch up to `#d4c9a8` and add faint horizontal render lines for texture
- Patio shadow is a single flat polygon — replace with a proper radial/feathered gradient shadow using SVG `<filter>` blur
- Festoon lights are too small (r=6) and uniform — vary radii slightly (5–8), add a soft glow filter behind them
- Counter/interior glow through glass is barely visible — strengthen `opacity` from 0.18 → 0.32, add a second warmer rect
- Piers are too prominent and detract — subtlety: reduce stroke to 0.8, lighten fill to blend with wall
- Add a thin drop-shadow `<filter>` to the whole building group for depth vs. sky

### Interactive rotation
- Wrap the SVG scene in a `<div class="scene-wrap">` with CSS `perspective`
- Add a `<input type="range">` scrubber (–25° to +25° azimuth) below the scene
- JS listener updates `scene-wrap` CSS `transform: rotateY(Xdeg)` — the SVG will rotate in 3D giving a parallax feel
- Add two preset buttons: "Street" (0°) and "Angle" (–15°) for quick switching
- Label: "Drag to orbit" with a small rotate icon

---

## 3 · Interior 3D (`gemi_interior.html`) — Aesthetic + Rotation

### Aesthetic uplift
- Floor chevron polygons are too blocky — the convergence math is slightly off, stripes should narrow more aggressively toward the horizon vanishing point (currently uniform width)
- Back wall `gemi` logo is well-placed but seed marks `cx=672/690` are off-centre relative to the text — recalibrate
- LED pendants glow ellipse (`rx=240,ry=60`) is circular and flat — extend `ry` to 80, use two overlapping glows at different opacities for softness
- Chair tufting lines are 4 vertical stripes only — add 2 horizontal lines for a proper channel-tufted cross-hatch
- Counter glass-block grid only goes to 3×3 — increase to 4 columns, add subtle inner-glow gradient per block
- Potted plant left foreground is stroke-only; add a terracotta pot `rect` at base (already there at y=600, good — but pot colour `#b5532f` is more orange than brand terracotta `#9B4A3A` — align)
- Wall gradient is too uniform — add a very faint vignette (dark corners) using a radial gradient overlay rect

### Interactive rotation
- Same approach as exterior: `rotateY` CSS transform on a perspective wrapper
- Range –20° to +20°, two presets: "Counter" (0°) and "Seating nook" (–12°)

---

## 4 · Architectural Drawing (`gemi_arch_plan.html`) — Aesthetic Uplift

### Issues found
- Background `#9aa3ab` is dated — use `#e8e2d8` (warm paper tone) to match brand
- Sheet background `#fbfbf9` is fine but double-border `innerborder` div is purely CSS positioned — works but could mis-align on mobile (sheet auto-scales)
- Poche pattern (`#1c2733` / `#2c3a47`) alternating rects is very dark and blocks legibility at small scale — lighten fill to a more readable cross-hatch style
- Grid lines and bubble refs are red (`#b8232f`) which is harsh — soften to `#c43b3b` with 70% opacity
- Legend bar needs a small top border separator
- Drawing is wide (1280px) with no horizontal scroll wrapper — add `overflow-x: auto` wrapper and `min-width: 900px` on sheet

---

## 5 · Concept Board (`gemi_concept_board.html`) — Minor Polish

- Moodboard `.m` panels use CSS pattern backgrounds — they're good but `.floorpat` stripe size (14px) is too coarse at board scale; tighten to 10px
- Footer section `.foot` grid has no responsive breakpoint — at <600px right panel overflows
- `board` max-width 1240px with no mobile padding guard — add `padding: 0 12px` on body at <600px

---

## 6 · Floor Plan (`gemi_floor_plan.html`) — Minor Polish

- Sheet is 1240px wide, same scroll issue on mobile
- Works section `.works ul` 3-col grid collapses badly on mobile — needs 1-col fallback
- Patio label text-anchor positioning is fine

---

## Implementation Order

1. `gemi_site/index.html` — responsive fixes (most critical, public-facing)
2. `gemi_exterior.html` — aesthetic + rotation
3. `gemi_interior.html` — aesthetic + rotation
4. `gemi_arch_plan.html` — aesthetic
5. `gemi_concept_board.html` — minor polish
6. `gemi_floor_plan.html` — minor polish

All changes go to branch `claude/laughing-volta-Lymhn`, pushed to update PR #1.
