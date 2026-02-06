# Copilot Instructions for Every Child Seen

## Project Overview
**Every Child Seen** is a districtwide equity-centered MTSS and belonging framework delivered as a single-file resource hub. The README.md contains embedded HTML/CSS and JavaScript that renders as a complete, interactive website—designed to be dropped into Weebly or viewed directly in browsers. This is **not a codebase**; it's an implementation-ready resource document for K-12 districts.

## Core Purpose & Audience
- **What it does**: Aligns instruction, supports, and family partnership so students on the margins (MLL/immigrant, IEP, poverty, trauma, LGBTQ+, Native students) are proactively supported rather than retroactively "fixed."
- **Who uses it**: District leaders, principals, teachers, and families across K-12.
- **How it's used**: Dropped into school websites (Weebly), printed as handouts, used in staff meetings and professional development cycles.

## Document Architecture

### Top-Level Structure (in order)
1. **Hero Section** (`#intro`): Opening promise, program definition, quick-start tags, navigation
2. **District Materials** (`#district`): Commitments, roles, data dashboard, messaging toolkit
3. **Principal Materials** (`#principals`): 10-day launch checklist, weekly huddle protocol, staff meeting script, walkthrough look-fors, communication templates
4. **Grade-Appropriate Materials** (`#grades`): K-2, 3-5, 6-8, 9-12 specific routines and approaches
5. **Grade-Band Handouts** (`#grade-handouts`): Copy/paste one-page PDFs for each grade band (4 detailed toolkits)
6. **Family Engagement** (`#family`): Partnership principles, survey, event formats
7. **FAQ** (`#faq`): Common questions addressed

### Key Sections & Hierarchy
- Each major section is a `.card` (styled container)
- Sub-sections use `<details>` elements (collapsible accordions) marked as `[open]` (expanded by default) or collapsed
- Templates are in `.template` divs (monospace, code-like formatting)
- Critical information is highlighted with `.callout` (dashed border highlight)

## Critical Content Patterns

### "Seen Data" Concept
The framework's measurable core. AI should understand:
- **Definition**: Evidence that students are known, supported, connected—beyond grades (adult connection logs, attendance, course access, behavior context, language support access, student voice)
- **Tracking**: Weekly huddles identify 3-5 students; assign adult owner + action + due date
- **Not compliance**: Data is human-centered and actionable, not box-checking

### Tiered Approach (MTSS Foundation)
- **Tier 1 (Universal)**: Strong instruction for all; checks for understanding every 8-12 min, sentence stems, language supports, participation equity
- **Tier 2/3 (Targeted/Intensive)**: Early re-engagement protocols, barrier removal, family partnership
- **Barrier removal**: Schedule, materials, transportation, interpreter access, tutoring—not just interventions

### Grade-Band Progressions
- **K-2**: Belonging + safety routines, early literacy, family outreach
- **3-5**: Participation equity, checks for understanding, barrier removal
- **6-8**: Advisory systems, executive skills, restorative responses
- **9-12**: On-track monitoring, course access equity, rapid re-engagement

## Style & Content Conventions

### HTML/CSS Structure

#### CSS Variables (Design System)
**Colors** (all defined in `:root`):
- `--bg: #0b1220` — dark background
- `--card: #0f1b33` — card/container background
- `--card2: #0c172d` — alternate card shade
- `--text: #eaf0ff` — primary text
- `--muted: #b9c7ee` — secondary text/labels
- `--brand: #5ea1ff` — primary action/links (blue)
- `--accent: #ff4d6d` — highlights/alerts (red/pink)
- `--ok: #2dd4bf` — success/positive indicators (teal)
- `--warn: #fbbf24` — warnings/cautions (amber)
- `--border: rgba(255,255,255,.12)` — subtle borders
- `--shadow: 0 12px 30px rgba(0,0,0,.35)` — card shadows

**Typography**:
- `--mono: ui-monospace, ...` — monospace font family (for `.template` blocks)
- `--sans: system-ui, ...` — sans-serif system fonts

**Spacing & Layout**:
- `--radius: 18px` — large border-radius (cards, hero)
- `--radius2: 12px` — medium border-radius (details, callouts, buttons)
- `--max: 1100px` — max-width for `.wrap` container

#### Key Classes & Usage
- **`.card`**: Primary content container
  - Uses gradient background + border + shadow
  - Applied to all major sections
  - Variants: `.card.small` (reduced padding for sidebars)
  
- **`.tag`**: Badge/label element
  - Includes `.dot` color indicator (inline, with box-shadow halo)
  - Variants: `.dot.accent`, `.dot.ok`, `.dot.warn`
  - Example: `<span class="dot ok"></span> Belonging`

- **`.template`**: Pre-formatted code/script block
  - Monospace font, dark background, light text
  - Used for copy/paste protocols, scripts, surveys, handouts
  - White-space preserved (allows indentation)

- **`.callout`**: Highlighted callout/emphasis box
  - Dashed border + blue tint background
  - Used for "Non-negotiables," "Purpose," critical definitions
  - Contains `<b>` (muted label) + `<p>` (content text)

- **`.grid2`, `.grid3`**: Responsive grid layouts
  - `.grid2`: 2 columns (1fr 1fr) →→ 1 column below 900px
  - `.grid3`: 3 columns (repeat 3, 1fr) →→ 1 column below 1000px
  - 14px gap between items

- **`.list`**: Bulleted list (replaces `<ul>/<ol>`)
  - Left padding 18px, styled list-items
  - Line-height 1.45 for readability

#### Interactive Elements
- **`<details>`**: Collapsible accordion
  - Styled border + semi-transparent background
  - `[open]` attribute = expanded by default
  - `.chev` (chevron icon) rotates on open state (color changes from muted → text)
  - 10px margin between adjacent `<details>` elements

- **`.btn`**: Button styling
  - Base: semi-transparent blue background + border
  - Variants: `.secondary` (red tint), `.ghost` (almost transparent)
  - Hover: slightly more opaque; Active: translateY(1px)
  - No border-radius defined; uses inherited properties

- **`.pill`**: Navigation/tag buttons (top navigation)
  - Rounded (border-radius: 999px)
  - Hover: opacity increase
  - Active: slight down-press animation (translateY)

#### Responsive Design
- **Primary breakpoint: 900px** (where `.grid2`, `.heroGrid` collapse)
- **Secondary breakpoint: 1000px** (where `.grid3` collapses)
- **Small screens: 560px** (`.kpis` grid → 1 column)
- **Topbar**: sticky, always visible; collapses `.nav` below 900px
- **Print styles**: body margins removed, gradients simplified (for PDF export)

#### Animations & Transitions
- **Transitions**: `transform .06s ease` (buttons, pills), `background .2s ease` (hover states)
- **Transform**: `translateY(1px)` on active buttons (press feedback)
- **Hover**: color/background changes, underlines added to links
- **Details open state**: `.chev` color changes to indicate state

### Writing Patterns
- **Action-oriented**: Use imperative language ("Run a huddle," "Track connection," "Remove barriers")
- **Specificity**: Concrete examples over generic advice (e.g., "checks for understanding every 8-12 minutes" vs. "check often")
- **Brevity**: Bullet lists, short scripts, templates meant to be copy/pasted
- **Inclusive language**: "Students on the margins," specific subgroups, culture + language + identity
- **Non-negotiables**: Explicit statements of what cannot be skipped (e.g., "Every student speaks daily"; "Every adult tracks 5 students")

### Naming Conventions
- **Routines**: "Seen Data Huddle," "Connection Tracking," "Participation Equity," "Barrier Removal"
- **Tools/Handouts**: Grade-band specific (e.g., "Handout A: Daily 'Seen' Routines (K–2)")
- **Key metrics**: Belonging, access, engagement, rigor, disproportionality, on-track
- **Terminology**: "Tier 1," "MTSS," "Coherence," "MLL" (multilingual learners), "IEP"

## Common Update Scenarios

### Adding a Section
- Follow existing `.card` > `details` structure
- Include `.tag` badges for quick categorization
- Add an `.template` for any copy/paste assets
- Link from navigation pills at top
- Update FAQ if needed
- Test at 900px and 1000px breakpoints to ensure grids collapse properly

### Refining Timelines/Protocols
- Keep specific time allocations (e.g., "30 min huddle," "10 days launch")
- Use `.callout` for critical non-negotiables
- Avoid vague language ("soon," "regularly"); use concrete frequencies ("weekly," "within 5 days")

### Adding Subgroup Context
- Reference specific populations (MLL, IEP, foster/housing insecurity, LGBTQ+, Native students)
- Suggest disaggregation in dashboards/data sections
- Include language about asset-based + culturally responsive approaches

### Grade-Band Handouts
- Each is a stand-alone `.card` with 3 detailed sections (A/B/C)
- Formatted in `.template` for printing as one-page PDF
- Include 1-2 key tags for quick reference
- Reference Tier 1 principles (checks, language supports, participation equity, barrier removal)

### CSS Best Practices for Content Updates
- **Color usage**: Reserve `--brand` (blue) for primary actions/links; `--accent` (red) for alerts; `--ok` (teal) for positive/success states; `--warn` (amber) for cautions
- **Avoid inline styles**: Always use CSS classes from the design system
- **Typography**: Use `--muted` for secondary text/labels, `--text` for body content
- **Spacing**: Margins/padding use pixel values (8px, 10px, 12px, 14px, 18px); prefer CSS variables for borders/shadows
- **New card sections**: Use existing gradient (`linear-gradient(180deg, rgba(15,27,51,.92), rgba(12,23,45,.88))`)
- **Interactive elements**: Apply `transition: transform .06s, background .2s ease` for consistency
- **Grid layouts**: Use `.grid2` for 2-column sections; `.grid3` for 3-column (with 14px gap)
- **Template blocks**: Always use monospace font + dark background (`rgba(0,0,0,.18)`) for code/script areas
- **Callouts**: Reserve for non-negotiables, critical definitions, and emphasis (dashed border + blue tint)

## Anti-Patterns to Avoid
- **Generic advice** without examples from this framework
- **Jargon without definition** (if borrowing terms, explain in context)
- **One-size-fits-all** language (grade bands, subgroups, cultural context matter)
- **Compliance language** (this is about student experience, not forms)
- **Disconnected initiatives** (always show coherence—how does this align to broader framework?)

## Key Files & References
- **Single file**: `/workspaces/everychild/README.md` (everything lives here)
- **No config files**, no build process, no dependencies
- **Intended delivery**: Weebly embed (use "Embed Code" element and paste entire HTML)
- **Alternative views**: GitHub markdown rendering, direct browser load

## Developer Workflow
1. **Edit README.md** in any text editor
2. **Preview**: Open in browser or GitHub to see rendered HTML
3. **Update navigation pills** (`<a class="pill">`) if adding major sections
4. **Test responsive design** at 900px breakpoint
5. **Print test** (Ctrl+P) to verify PDF layout for handouts
6. **Validate HTML**: Check for unclosed tags, especially in `<details>` blocks
7. **Test links**: Internal anchors (`href="#section-id"`) should scroll smoothly

## Quick Reference: Framework Anchors
- **Non-negotiable outcome**: Belonging + access for every learner
- **How to operationalize**: Tiered supports + culturally responsive practice
- **What changes Monday**: Routines, data cycles, family partnership
- **Evidence of success**: Student can name an adult; families report partnership; access gaps narrow; engagement improves
