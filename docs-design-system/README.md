# SecurityPal AI — Document Design System

The operating reference for building brand-locked **documents** (Google Docs / Word / PDF reports) such as the *Third Party Risk Assessment Report*. It is the document counterpart to the SecurityPal Deck Design System: same brand, same blue, different canvas.

Every rule below comes from the BrandGuard spec (`reference/brandguard.html`) and the approved report pages in `reference/`. When the two disagree, the spec's numbers win and the reference pages decide anything the spec leaves open.

## Sources

- **BrandGuard spec**: the SecurityPal brand-compliance checker. Defines page setup, the type scale, the 6-color palette, layout, tables, cover, footer, charts, and the 35-item checklist in §12.
- **Reference pages** in `reference/`:

| File | Shows |
|---|---|
| `01-table-of-contents.png` | TOC page, two-level entries, body footer |
| `02-executive-summary.png` | Two-column label / content layout, bullets |
| `03-bar-chart.png` | Bar chart in blue shades, caption below |
| `04-radar-chart-and-table.png` | Radar chart, table title, data table, caption |
| `05-table-styles.png` | The three approved table header patterns |

- **Typeface**: **Geist**, used for all text. No second font.

---

## 0 · Page setup

| Property | Value |
|---|---|
| Format | A4 portrait (8.27 × 11.69 in) |
| Margins | 0.8 in on all four sides, uniform |
| Orientation | Portrait, always. No landscape pages for text-heavy reports |
| Page background | White `#FFFFFF`. Only the cover page has a colored background |
| Content grid | Two columns: label column ~30%, content column ~70% (§3) |

**Google Docs:** File → Page setup → A4, margins 0.8 in, portrait, page color white → **Set as default**.

---

## 1 · Color system (strict)

Six colors. Nothing else appears in text, tables or backgrounds.

| Token | Hex | Use |
|---|---|---|
| Brand Blue | `#015CE6` | H1 headings, chart primary, table header (option A), footer accents, date pill |
| Black | `#121212` | Body text, H4, captions, table header (option B) |
| Grey | `#828282` | H2 headings, TOC sub-entries, footer document title |
| Light Blue | `#E8F1FF` | Table body under a **blue** header |
| Light Grey | `#F0F4F9` | Table body under a **black** header |
| White | `#FFFFFF` | Page background, text on blue/black, table borders |

**Chart-only blue shades.** Use these only for chart data series and Canva-made visual pages, never for text:

`#015CE6` · `#1A6EEA` · `#3380ED` · `#4C92F1` · `#66A4F4` · `#80B6F7` · `#99C8FB` · `#B3DAFE` · `#CCE6FF` · `#E6F3FF`

**Cover gradient.** The cover is Brand Blue and may deepen into dark navy `#000E44`, which BrandGuard accepts. Do not use it anywhere else.

**Rules**
- Black is `#121212`, not `#000000`. Blue is exactly `#015CE6`, not a "close enough" blue.
- Brand Blue is for headings and accents. Never use it for body paragraphs.
- No extra accent colors for emphasis: no red, green, yellow or orange text or highlights.

---

## 2 · Typography (strict)

**Font: Geist** for everything. Hierarchy comes from size and color. Do not make text bigger or bolder to create emphasis; use the right style instead.

| Style | Size | Weight | Color | Used for |
|---|---|---|---|---|
| Title | 34 pt | Regular | White | Cover page title |
| Subtitle | 18 pt | Regular | White | Cover supporting line |
| Heading 1 | 18 pt | Regular | Brand Blue `#015CE6` | Section heading at the top of a page ("Executive Summary") |
| Heading 2 | 14 pt | Regular | Grey `#828282` | Sub-heading to H1: the left-column label ("Objective"), table titles |
| Heading 4 | 11 pt | Semi-Bold | Black `#121212` | Sub-heading to H2, inside the content column |
| Normal text | 11 pt | Regular | Black `#121212` | Body paragraphs, bullets, TOC entries |
| Table text | 10 pt | Regular (header: Medium) | White on header, Black in body | All table cells (§4) |
| Heading 6 | 11 pt | Regular italic, label semi-bold | Black `#121212` | Figure and table captions ("*Image:* CIS Controls…") |
| Heading 5 | 8 pt | Regular | Grey `#828282` / Brand Blue | Footer text |

**Allowed sizes:** 8 · 10 · 11 · 14 · 18 · 34 pt. Nothing else (no 12, 16, 20 or 24).

- There is **no Heading 3**. Go straight from H2 to H4.
- Semi-Bold is used only for H4 and the caption label ("Image:" / "Table:"). Everything else is Regular.
- Set up each style once under Format → Paragraph styles → *Update to match*, then only ever apply styles, never manual formatting.
- Sentence case or title case for headings. Never ALL CAPS.
- Body paragraphs use generous line spacing (the reference Executive Summary sets roughly 2.0) with space-after between paragraphs, never empty lines.

---

## 3 · Layout & spacing

The core body pattern is a **borderless two-column layout**:

```
┌──────────────────────────────────────────────────────────┐
│ Heading 1 (Brand Blue, 18pt)                             │
│                                                          │
│ Heading 2 label     │ Normal text, 11pt, left-aligned,   │
│ (Grey, 14pt)        │ 50–75 characters per line.         │
│      ~30%           │              ~70%                  │
│                                                          │
│ Next label          │ • Bullet, filled round dot,        │
│                     │   hanging indent                   │
└──────────────────────────────────────────────────────────┘
```

- **Build it** as a borderless 2-column table: left 30%, right 70%. The H2 label and its content share a top baseline.
- **Line length** 50–75 characters per line. The 70% column enforces this. Never run full-width single-column paragraphs.
- **Alignment:** left-aligned, always. **Never justified.** Justified text spaces words unevenly, slows reading, and goes against WCAG 1.4.8.
- **Whitespace:** leave clear space between label/content blocks (see the reference gap between *Objective* and *Methodology*). Use space-after, not blank lines.
- **Page breaks:** each H1 section starts on a new page. If a page feels cramped, move content to the next page. Never shrink fonts or spacing to make things fit.
- **Rule of thumb:** when you are unsure whether to add more to a page or start a new one, start a new one. An 18-page report with good spacing looks more professional than a crammed 15-page one.
- **Full-width exceptions:** charts and data tables may span the full content width (margin to margin) below the two-column text.

**Bullets:** filled round dot (●), Normal text, hanging indent, same line spacing as body. One bullet level. If you need a second level, restructure the content.

---

## 4 · Tables

| Property | Value |
|---|---|
| Font | Geist 10 pt, single line spacing, no paragraph spacing |
| Header text | White, Medium weight, cell alignment **middle** |
| Header background | Brand Blue `#015CE6` **or** Black `#121212` |
| Body text | Black `#121212`, cell alignment **top** |
| Body background | Light Blue `#E8F1FF` **or** Light Grey `#F0F4F9` |
| Borders | 3 pt, **White**, acting as the gap between cells |
| Cell padding | 0.1 in |
| Placement | Inline, left-aligned to the margin |
| Column text | First (label) column left-aligned; numeric columns centered |

**Column pairing rule.** A body column's fill follows its header:

| Header | Body column fill |
|---|---|
| Brand Blue `#015CE6` | Light Blue `#E8F1FF` |
| Black `#121212` | Light Grey `#F0F4F9` |

**Approved header patterns** (see `reference/05-table-styles.png`). Pick one per document and use it for every table in that document.

| Pattern | Column 1 | Columns 2…n |
|---|---|---|
| **A · Blue key** | Blue | Black |
| **B · Black key** | Black | Blue |
| **C · Alternating** | Black | Blue, Black, Blue… alternating |

Pattern A is the one used in the approved report's data tables (`04-radar-chart-and-table.png`).

**Table title and caption**
- An optional **title** goes above the table in Heading 2 (Grey 14 pt, centered), e.g. *Organizations used for Industry Average: 1963*.
- A **caption** goes below the table in Heading 6, centered: ***Table:*** *CIS Control Average vs Industry Standard*.

**Never:** default Docs/Word styling (thin black borders, no fills), mixed header patterns in one document, body text centered vertically, missing padding, zebra striping by row.

---

## 5 · Charts & visual pages

| Property | Value |
|---|---|
| Tool | Canva (SecurityPal template when available); export at high resolution |
| Primary color | Brand Blue `#015CE6` |
| Other series / shades | Only the ten approved blue shades (§1) |
| Background | White, no chart border, no chart shadow |
| Gridlines | Hairline light grey (horizontal only on bar charts; dashed rings on radar) |
| Axis & label text | Geist, small, Black |
| Chart name | **Below** the chart as a Heading 6 caption, never a title above |

**Bar chart** (`03-bar-chart.png`)
- One bar per category, square-ended, with narrow white gaps between bars.
- Shade encodes value: the highest values get Brand Blue `#015CE6` and lower values step down through the lighter shades. Never use a rainbow palette.
- The value label sits inside the bar: white on dark shades, Black on the lightest shades.
- The y-axis runs 0–100 with gridlines every 20. Category labels (e.g. "CIS C01") wrap to two lines under each bar.

**Radar / spider chart** (`04-radar-chart-and-table.png`)
- Primary series (*Your Assessment*): light blue fill (`#99C8FB`–`#B3DAFE` at ~50% opacity) with a light blue stroke.
- Comparison series (*Industry Average*): Brand Blue fill and stroke, drawn on top.
- The legend sits top-center with filled dot markers. Rings are dashed light grey, labeled 0–100.

**Insert:** size the image to the content width, lock its aspect ratio (never stretch), center it, and put the caption directly below.

**Never:** default Excel/Sheets colors, non-blue series (red/green included), chart titles above, low-resolution exports, charts too small to read or so large they spill the page.

---

## 6 · Figures & captions

Every chart, image and data table gets a caption **below** it in Heading 6 (11 pt, Black, italic, centered). The label is semi-bold italic and followed by a colon:

- ***Image:*** *CIS Controls Implementation Chart*
- ***Table:*** *CIS Control Average vs Industry Standard*

Leave one body line of space above and below the caption.

---

## 7 · Cover page

- Full-page **Brand Blue** background (a flat `#015CE6` or a blue → `#000E44` gradient from the approved Canva template).
- **Title**: 34 pt White Geist. **Subtitle**: 18 pt White Geist.
- SecurityPal AI logo (white) in the top-left.
- Branding only: no body content, no TOC, and as little text as possible.
- The cover has its own pre-designed footer, different from the body footer (Docs: *Different first page*).

**Never:** a missing cover, a plain white cover with just a title, off-brand gradients, missing logo.

---

## 8 · Table of contents

See `reference/01-table-of-contents.png`.

- Page heading in Heading 1: **Table of Contents**.
- **Level 1 entries**: Normal text, Black `#121212`, flush left.
- **Level 2 entries**: Normal text, Grey `#828282`, indented ~0.6 in.
- Page numbers are right-aligned to the margin, in the same color as their entry, with **no dot leaders**.
- Generous, even spacing between rows (about one blank line's worth). Sections map 1:1 to H1s and sub-entries to H2s.

Report section order used in the approved TPRA report: Executive Summary → Vendor Profile → Purpose → Vendor Assessment Scope of Work → Risk Assessment Approach → Risk Assessment Findings → SOC Audit Report Review → Vendor Diversity Assessment → ESG Assessment → Recommendation.

---

## 9 · Footer

The same footer appears on **every body page** (not on the cover). It is set in Heading 5, Geist 8 pt.

```
Confidential                                Third Party Risk Assessment Report
( 2026-03-16 )                                      Prepared by SecurityPal AI
```

| Position | Line | Style |
|---|---|---|
| Left | `Confidential` | 8 pt Brand Blue |
| Left | Date `YYYY-MM-DD` | 8 pt White in a fully rounded Brand Blue pill |
| Right | Document title | 8 pt Grey `#828282`, right-aligned |
| Right | `Prepared by SecurityPal AI` | 8 pt Brand Blue, right-aligned |

Footer content should cover the company name, document title, date, and the confidentiality notice. Add page numbers when the document has a TOC.

**Never:** no footer, body-size footer text, footers that differ between body pages, the body footer on the cover.

---

## 10 · Page templates

Recombine these page types for any report.

| # | Page | Structure |
|---|---|---|
| 01 | Cover | Blue background, logo, Title 34 pt + Subtitle 18 pt, cover footer |
| 02 | Table of contents | H1 + two-level entries + right-aligned page numbers |
| 03 | Two-column section | H1, then rows of H2 label (30%) + body / bullets (70%) |
| 04 | Section + chart | H1, two-column intro row, full-width chart, caption |
| 05 | Chart + table | Chart + caption, H2 table title, data table, caption |
| 06 | Data table | H1 or H2 label, full-width table (one header pattern), caption |
| 07 | Recommendation | H1, two-column rows; the conclusion is set as body text, not decorated |

---

## 11 · What not to do

- **Cramming**: more content per page is not more professional. Readers skip, skim, or give up.
- **Decoration**: no drop shadows, decorative borders, boxes around text, or gradient fills on text boxes.
- **Extra fonts or colors**: Geist only, the 6-color palette only.
- **Justified text**: never.
- **Filling every inch**: whitespace is working space.
- **Emoji, clip-art, stock icons in body text**: never.

---

## 12 · QA checklist (must pass before a document ships)

The 35 BrandGuard checks, grouped as in the tool:

**1. Page setup & format**
- [ ] A4 portrait (8.27 × 11.69 in)
- [ ] Margins 0.8 in on all four sides
- [ ] White background
- [ ] Portrait orientation

**2. Typography**
- [ ] Geist font family throughout
- [ ] Title is 34 pt, White, on the cover page
- [ ] Heading 1 is 18 pt Brand Blue `#015CE6`
- [ ] Heading 2 is 14 pt Grey `#828282`
- [ ] Body / Normal text is 11 pt Black `#121212`
- [ ] Footer text is 8 pt
- [ ] No sizes outside the scale (8 · 10 · 11 · 14 · 18 · 34)

**3. Brand colors**
- [ ] Brand Blue used for headings and charts
- [ ] Black `#121212` used for table headers and body text
- [ ] Grey used for subtitles and footer
- [ ] Light Blue `#E8F1FF` used for table column backgrounds
- [ ] Light Grey `#F0F4F9` used for alternate table backgrounds
- [ ] No off-brand colors

**4. Layout & spacing**
- [ ] Two-column layout (≈30% / 70%)
- [ ] Line length 50–75 characters
- [ ] Generous whitespace; pages are not cramped
- [ ] Left-aligned text, not justified
- [ ] Content has breathing room

**5. Tables**
- [ ] Table font 10 pt
- [ ] Header background Brand Blue or Black
- [ ] Header text White
- [ ] Body background Light Blue or Light Grey (paired with its header)
- [ ] Borders 3 pt White
- [ ] Cell padding 0.1 in
- [ ] Inline, left-aligned

**6. Cover page**
- [ ] Distinct cover page
- [ ] Brand Blue background
- [ ] Title large, white, prominent
- [ ] SecurityPal AI branding present

**7. Footer**
- [ ] Same footer on all body pages
- [ ] Footer uses Heading 5 (8 pt)
- [ ] Cover footer differs from the body footer

**8. Overall professionalism**
- [ ] No decorative borders or effects
- [ ] No competing fonts
- [ ] No justified text
- [ ] Clear visual hierarchy

Run the finished PDF through **BrandGuard** (`reference/brandguard.html`, open it in a browser and drop in the PDF or a Docs link) for an automated score.

---

## Index

```
docs-design-system/
  README.md            ← you are here
  SKILL.md             ← agent skill manifest
  reference/
    brandguard.html    ← BrandGuard spec + compliance checker (source of truth)
    01-table-of-contents.png
    02-executive-summary.png
    03-bar-chart.png
    04-radar-chart-and-table.png
    05-table-styles.png
```

## Caveats

- **px vs pt.** BrandGuard writes sizes as "px", but its checker measures PDF point sizes. Enter them as **pt** in Google Docs or Word.
- **Heading 3** is not defined in the spec, so it is intentionally unused.
- **Italic captions.** Geist ships no true italic, so Docs will synthesize a slanted one. That is accepted for captions only.
- **Pure black headers.** One reference table (`05-table-styles.png`) renders a header near `#000000`. The spec value `#121212` is binding.
- **Centered captions and table titles** are the one exception to "left-aligned always", matching the approved pages.
- Chart styling for radar fills (opacity) and value-label colors is read from the reference images, not stated in the spec.
