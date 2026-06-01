# Gemi Takeaway — Project Workflow & Build Documentation

**Project:** Premium fast-casual outlet, Rayfield, Jos, Plateau State  
**Client:** Dakol Masiyer / Dakon Enterprises  
**Scope:** Concept development, architectural drawings, 3D renders, presentation site  
**Status:** Complete (concept to presentation) | Lease proposal pending  

---

## Overview

This document captures the full workflow and decision history for the Gemi Rayfield outlet project, from initial site survey through final presentation assets. Use this as a reference for Claude Code, future iterations, or teaching/documentation purposes.

### Quick Links
- **Main site:** `gemi_site/index.html` — Scrollable presentation (open in browser)
- **Architectural drawing:** `gemi_arch_plan.html` — GEMI-A-101, 1:100, millimetres, measured plan with forecourt & drainage
- **Concept floor plan:** `gemi_floor_plan.html` — Warm, branded layout view
- **3D Exterior:** `gemi_exterior.html` — Street view, daytime
- **3D Interior:** `gemi_interior.html` — Counter, seating, chevron floor
- **Brand board:** `gemi_concept_board.html` — Design system, colour, typography

---

## Project Context

### Location & Site
**Rayfield, Jos, Plateau State, Nigeria** — dual-carriageway arterial road frontage, high daytime traffic, open green fields across road.

### Lease Scope
**Kitchen end-unit + 3 open bays** (full contiguous run)

**Measured dimensions (from site survey, hand-verified):**
- Total front run: ~14.6 m (48 ft)
- Bay A: 3.632 m (11'11") | Bay B: 3.226 m (10'7") | Bay C: 3.200 m (10'6")
- Kitchen: ~3.353 m (11 ft)
- Pier widths: ~406 mm (1'4") × 3 piers
- Bay depth: 6.299 m (20'8")
- Front beam height: 2.337 m (7'8") — **critical constraint**
- Interior peak height: 3.99 m (13'1") under exposed steel truss
- Patio depth: ~4.877 m (16 ft)
- Indoor area: ~68 m²

### Design Reference
**gögi, Lagos** — premium burger + rice bowl concept, monochrome base (matte black #1A1A1A + white #FFFFFF), terracotta (#9B4A3A) seating, walnut (#8B5A2B) furniture, chevron marble floor, glass-block backlit counter, editorial visual language, high-quality packaging.

---

## Workflow & Decision Log

### Phase 1: Concept & Brand Identity

#### 1.1 Brand Definition
- **Name:** Gemi (not copying gögi; own brand, same design language)
- **Tagline:** "good food, no waiting."
- **Wordmark:** Familjen Grotesk, lowercase, bold geometric, seed-mark umlaut over the i
- **Colour Palette:**
  - Primary: White #FFFFFF, Matte Black #1A1A1A
  - Accent: Terracotta #9B4A3A, Cream #EADCC9
  - Nature: Olive #556B2F, Sage #8A9A5B, Walnut #8B5A2B
- **Typography:** Fraunces (display/serif) + Familjen Grotesk (body/UI)
- **Key Visual:** Black-and-white chevron marble floor (45° diagonals)

**Output:** `gemi_concept_board.html` — Full brand & design system board

#### 1.2 Design System Locked
- Counter: Illuminated glass-block facade, marble quartz top
- Seating: Walnut tulip tables, terracotta + grey channel-tufted chairs
- Lighting: Linear warm LED pendants
- Patio: Olive green slatted benches, dark tables, planters with palms, festoon string lights
- Shopfront: Slim black aluminium framing + full glazing, sliding entry
- Signage: White fascia with 24/7 left, Gemi wordmark right

---

### Phase 2: Architectural Drawings & Floor Plans

#### 2.1 Concept Floor Plan (Drawing 01)
**Decision:** Show the space in warm, branded colours to sell the vision and teach design thinking.

- Kitchen end-unit (back of house, zone 01): cooking line, prep, cold storage
- Pass-through door: new internal doorway from kitchen to service area (flagged for fit-out)
- Service counter: glass-block backlit, POS, order & pickup
- Dining/seating (bays 2–3, zone 02): chevron marble floor, walnut tables, terracotta chairs, banquette
- Forecourt patio (zone 03): green benches, planters, festoon lights, ~5 m deep
- Works notes flagged: (1) pass-through door, (2) seal settlement crack, (3) glazed shopfront, (4) new floor slab

**Output:** `gemi_floor_plan.html` — 1 page, scale annotated, concept impressions

#### 2.2 Architectural Plan GEMI-A-101 (Drawing 02)
**Decision:** Single comprehensive sheet showing building interior + external works (forecourt patio, drainage, furniture). ISO/BS drafting conventions.

**Content:**
- **Building zone:**
  - Wall poché (hatched)
  - Column grid A–F (red dashed lines + bubbles)
  - Dimension strings (witness lines, tick marks, millimetres)
  - Door schedule: D1 (existing kitchen door), D2 (new pass-through, 900mm), D3 (sliding entrance)
  - Door swings shown with arcs
  - Lintel beam shown dashed (structure over)
  - Section marker (AA)
  - Room labels & zones (01 Kitchen, 02 Dining/Service, 03 External Dining)
  - Fixtures: cooking line, counter, POS, prep, cold, tables, banquette

- **Forecourt zone:**
  - Patio paved area: 600×600 porcelain pavers setting-out grid
  - Drainage falls: 1:60 slope, arrows pointing to channel
  - Existing roadside drainage channel (hatch pattern)
  - Patio furniture: 3 bench-table sets + booth (thin lines)
  - Planters (circles)

- **Dimensions:**
  - Top: 14630 mm overall front run, bay-by-bay chain (3353 + 3632 + 3226 + 3200 + 2438)
  - Right: 6299 mm bay depth, 4877 mm patio depth
  - Bottom: overall front run repeated, FFL datum note, roof height range
  - North arrow (ROAD South)

- **Title Block:**
  - Drawing No.: GEMI-A-101
  - Scale: 1:100 @ A2
  - Units: Millimetres
  - Projection: Plan, view down
  - Drawn: D. Masiyer, 2026
  - Revision: A
  - Sheet: 1 of 1

- **Legend:** Wall (poché), glazed shopfront, structure over, grid ref, door + swing, new work/action, drainage channel, drainage fall

**Output:** `gemi_arch_plan.html` — 1 page, comprehensive, construction-ready, double border, title block per ISO

---

### Phase 3: 3D Visualisations

#### 3.1 Exterior 3D (Drawing 02 — Street View)
**Decision:** Render the façade and patio as they appear to the road, showing the daytime experience and key brand touchpoints.

**Scene:**
- Blue-gradient sky with soft clouds
- Distant green fields across road
- Dual carriageway with median, solar street poles, dashed white line
- Building: matte ochre/yellow walls (existing), concrete parapet
- White signage fascia: "24/7" on left, "gemi" wordmark with seed marks on right
- Green-and-white stripe awning above shopfront
- Glazed three-bay shopfront: blue-tinted glass, mullion ticks, sliding entry with mascot decal
- Kitchen end-unit: solid wall, high vent window, brown existing door
- Forecourt patio: light paved surface, joint lines visible
- Bench-table sets: olive green benches, dark tables
- Planters with palms: terracotta pots
- Festoon string lights: golden bulbs on dark wire
- Shadow cast by building on patio

**Style:** Flat/geometric rendering, true to measurements (7'8" beam height respected), editorial rather than photorealistic

**Output:** `gemi_exterior.html` — 1 page, daytime concept impression

#### 3.2 Interior 3D (Drawing 03 — Inside Gemi)
**Decision:** Show the service counter, seating, and floor in warm, inviting light to communicate the premium fast-casual brand feel.

**Scene:**
- Warm cream walls with subtle gradient
- Ceiling: exposed to peak roof, black cylinder downlights, linear warm LED pendants with golden glow halos
- Back wall: oversized "gemi" wordmark (matte black, 78px), seed marks offset
- Service counter: glass-block facade (light blue-grey) with marble-veined top, internal glow hint, product jars (terracotta), POS station (black)
- Chevron marble floor: bold black-and-white 45° diagonal stripes in perspective, converging toward camera
- Dining: 3 walnut tulip tables with terracotta + grey channel-tufted chairs (4 chairs per table, mixed colours)
- Banquette: terracotta channel-tufted along back wall
- Bowl on table: white with "gemi" branding
- Foreground plant: potted with green leaves in terracotta pot
- Floor lamp: black with shade, right side
- Branded bowl visible on table with "gemi" mark

**Style:** Perspective 3D with linear depth, warm colour temperature, photogenic

**Output:** `gemi_interior.html` — 1 page, premium fast-casual interior impression

---

### Phase 4: Presentation Site

#### 4.1 Main Site: `gemi_site/index.html`
**Decision:** Single scrollable HTML page with smooth navigation, alternating light/dark sections, embedded images, and clear visual hierarchy. Suitable for browser presentation or classroom projection.

**Structure (6 sections):**

1. **Hero:** Large wordmark (gemi with seed mark), tagline, description, location callout, scroll cue
2. **The Brand (01):** Concept board image, description of design language
3. **Street View (02):** Exterior 3D, dark background section
4. **Inside (03):** Interior 3D, light background
5. **Floor Plan (04):** Concept plan image, dark background
6. **Architectural Plan (05):** GEMI-A-101 drawing, light background
7. **Why Lease (06):** Stats (68 m², 48 ft frontage, 24/7 model, 100% tenant fit-out), three benefit boxes, closing quote, dark background

**Navigation:** Fixed nav bar with links to each section, logo with seed mark

**Style:** UK English typography, minimalist layout, professional yet accessible, print-friendly

**Images embedded:** concept_board.png, exterior.png, interior.png, floor_plan.png, arch_plan.png

**Output:** `gemi_site/index.html` + image folder (keep together when deployed)

---

### Phase 5: Standalone Drawing Files

All major deliverables saved as individual HTML files for printing, export, or editing:

1. **gemi_concept_board.html** — Brand system, colours, typography, floor patterns, textures
2. **gemi_floor_plan.html** — Concept floor plan (warm, branded)
3. **gemi_arch_plan.html** — GEMI-A-101 architectural drawing (measured, ISO conventions, forecourt + drainage)
4. **gemi_exterior.html** — Street view 3D
5. **gemi_interior.html** — Interior 3D

Each file is self-contained, styled for screen and print (A4/A2 scale noted in title block), and can be opened in any browser or exported to PDF.

---

## Key Decisions & Trade-offs

### 1. One Architectural Drawing vs. Separate Sheets
**Decision:** Add the forecourt (patio, drainage, furniture) to GEMI-A-101 rather than split into A-100 (site plan) + A-101 (building plan).

**Rationale:** For a teaching project and single-outlet pitch, one comprehensive sheet communicates the full scope to the owner and simplifies document management. Drainage falls and patio design are shown with proper conventions (hatch, arrows, grid).

**If scaled up:** Would split into separate sheets per standard practice.

### 2. 7'8" Front Beam Height as Design Constraint
**Decision:** Respected in both exterior 3D and architectural drawing. Governs door and signage band height.

**Implication:** Glazed shopfront mullions and signage band must fit within 2.337 m clearance. Sliding entry is feasible at this height (shown in rendering).

### 3. Chevron Floor as Brand Mark
**Decision:** Black-and-white 45° chevron marble as the primary visual differentiator (inspired by gögi but executed as Gemi's own mark).

**Impact:** Drives the interior experience and becomes instantly recognisable in photos and renderings.

### 4. Warm LED + Terracotta Seating
**Decision:** Gögi reference uses matte black + white minimalism. Gemi softens it with warm light and rust/terracotta accents.

**Rationale:** Jos market context — warmth and colour signal hospitality and approachability, while the chevron floor and white fascia maintain editorial quality.

### 5. Forecourt Patio as Evening Destination
**Decision:** Forecourt is lit and furnished as a primary feature, not an afterthought.

**Implication:** 24/7 operating model: daytime grab-and-go, evening sit-out destination. Festoon lights and bench seating create a gathering space that extends the brand beyond the counter.

---

## Technical Specifications

### Drawing Scales & Dimensions
- **Concept floor plan:** Annotated, not to scale (graphic clarity prioritised)
- **GEMI-A-101:** 1:100 @ A2, millimetres, ISO/BS conventions, metric throughout
- **3D renderings:** No scale, concept impressions

### File Formats
- **HTML:** All drawings and site; self-contained, browser-compatible, printable to PDF
- **SVG:** Embedded in HTML for crisp vector rendering at any size
- **PNG:** Embedded images for the presentation site (compressed)

### Colour Space
- All brand colours locked as hex values in CSS custom properties
- Print: CMYK separation recommended when outputting to PDF

### Typography
- **Display:** Fraunces (serif, italicised for taglines)
- **Body/Labels:** Familjen Grotesk (sans-serif, tight tracking on labels)
- **Callouts:** 9–11px for architectural annotations, 15px+ for room labels

---

## Fit-Out Scope (Works Flagged)

As per architectural drawing and floor plan:

1. **(1) Pass-through door** — Cut new internal doorway from kitchen to service bay (900 mm, not currently open)
2. **(2) Seal crack** — Patch and reinforce settlement crack on kitchen rear wall
3. **(3) Glazed shopfront** — Install glazed aluminium storefront across full three-bay run (front elevation ~14.6 m)
4. **(4) Floor slab** — Pour finished RC concrete over raw dirt (bays) and paved patio deck (600×600 porcelain pavers)
5. **Drainage** — Forecourt falls 1:60 to existing roadside channel
6. **MEP** — Electrical (linear LED, POS, kitchen), water (counter, kitchen), mechanical (insulation under zinc roof)

**Investment:** 100% tenant-funded. **Argument:** Permanent improvements stay with the property, raising its value and appeal.

---

## Next Steps / Pending Deliverables

### Lease Proposal Document
**Status:** Not yet built.

**Scope:** Formal written pitch to the landlord, 2–3 pages, covering:
- Who is Gemi (brand, operator profile)
- What investment they're making (fit-out scope + cost estimate framework)
- Why lease to them (reliable operator, premium brand, footfall benefit)
- Proposed terms: **[PLACEHOLDER: rent per m² per month]**, **[PLACEHOLDER: lease term, e.g. 3/5 years]**, rent-free fit-out period option
- Closing: signature block, next steps

**Format:** Professional Word document or PDF, suitable for printing and signing.

**For teaching:** Leave rent/term placeholders so students debate and fill in figures.

---

## How to Use This Workflow

### For Presentation (Owner Pitch)
1. Open `gemi_site/index.html` in a browser
2. Present the full scroll, or jump to sections via nav
3. Use individual drawings (architectural plan, exterior, interior) to discuss specifics
4. Print any page to PDF for distribution

### For Classroom Teaching
1. **Entrepreneurship:** Use the brand board and floor plans to discuss design vision vs. construction reality
2. **Architecture:** Compare the concept plan (warm, branded) with GEMI-A-101 (technical, ISO) to show two languages for the same space
3. **Project Management:** Walk through the site survey → measured drawing → 3D render pipeline
4. **Finance/Negotiation:** Use the lease proposal placeholder to debate rent figures, fit-out investment, and landlord incentives

### For Claude Code (Future Iterations)
- This markdown captures all decisions, dimensions, and design intent
- If changes are needed (e.g., different rent term, new room label, colour adjustment), reference the relevant section
- All HTML files are SVG-based and text-editable; CSS custom properties make bulk colour changes trivial
- Dimensions are in the drawing comments; metric conversions are in the project context section

### For Version Control
- Commit this markdown alongside the build folder
- Tag releases (v1.0 = concept complete, v2.0 = with lease proposal, etc.)
- Track decisions in git history

---

## File Structure

```
gemi_complete/
├── README.md  (this file)
├── gemi_site/
│   ├── index.html  (main presentation site)
│   ├── concept_board.png
│   ├── exterior.png
│   ├── interior.png
│   ├── floor_plan.png
│   └── arch_plan.png
├── gemi_concept_board.html
├── gemi_floor_plan.html
├── gemi_arch_plan.html
├── gemi_exterior.html
└── gemi_interior.html
```

---

## Contact & Project Owner

**Project Lead:** Dakol Masiyer  
**Location:** Rayfield, Jos, Plateau State, Nigeria  
**Created:** June 2026  
**Status:** Presentation assets complete; lease proposal pending

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 2026-06-01 | Initial concept, brand board, floor plans (concept + architectural), 3D renders, presentation site |
| TBD | TBD | Lease proposal document |

---

**End of Workflow Documentation**
