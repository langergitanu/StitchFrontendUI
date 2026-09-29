---
name: Obsidian Precision Note System
colors:
  surface: '#131317'
  surface-dim: '#131317'
  surface-bright: '#39393d'
  surface-container-lowest: '#0e0e12'
  surface-container-low: '#1b1b1f'
  surface-container: '#1f1f23'
  surface-container-high: '#2a292e'
  surface-container-highest: '#353439'
  on-surface: '#e4e1e7'
  on-surface-variant: '#e4bdbd'
  inverse-surface: '#e4e1e7'
  inverse-on-surface: '#303034'
  outline: '#ab8889'
  outline-variant: '#5b4040'
  surface-tint: '#ffb3b5'
  primary: '#ffb3b5'
  on-primary: '#680018'
  primary-container: '#dc2646'
  on-primary-container: '#fff8f7'
  inverse-primary: '#be0234'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffb95f'
  on-tertiary: '#472a00'
  tertiary-container: '#a16600'
  on-tertiary-container: '#fff9f5'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffdada'
  primary-fixed-dim: '#ffb3b5'
  on-primary-fixed: '#40000b'
  on-primary-fixed-variant: '#920025'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffddb8'
  tertiary-fixed-dim: '#ffb95f'
  on-tertiary-fixed: '#2a1700'
  on-tertiary-fixed-variant: '#653e00'
  background: '#131317'
  on-background: '#e4e1e7'
  surface-variant: '#353439'
typography:
  display-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
  headline-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '600'
    lineHeight: 24px
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.02em
  label-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 11px
    fontWeight: '500'
    lineHeight: 14px
    letterSpacing: 0.03em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1rem
  gutter-tablet: 1.25rem
  margin: 1rem
  margin-tablet: 1.5rem
  margin-desktop: 2rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

This design system establishes a high-performance, focused environment tailored for technical, scientific, and academic notetaking across tablets, foldables, and mobile form factors. 

The aesthetic is built on **Dark Tactile Modernism**—combining deep charcoal grounds with high-chroma, laser-focused functional accents. It eliminates visual noise to prioritize deep work, formula writing, diagramming, and hierarchical document organization. 

Key attributes:
- **Focused & Immersive:** Low-luminance dark backgrounds reduce eye fatigue during prolonged late-night study and technical research.
- **Instrument-Grade Precision:** Sharp structural discipline balanced by friendly, tactile pill-shaped interaction targets (stylus and touch-optimized).
- **Vibrant Functional Accents:** Crimson acts as the primary focal point, emerald represents addition and growth, amber marks priority, and electric cobalt guides navigation and tool selection.

## Colors

The color architecture is calibrated specifically for OLED and high-resolution tablet displays. Surfaces scale through three distinct dark neutral steps rather than pure black, preserving depth while maintaining comfortable contrast with muted boundary strokes.

### Palette Roles
- **Primary (`#DC2646` / `#E63956`):** Vivid Crimson/Rose. Reserved for primary calls-to-action (Create File, Upgrade CTA), active navigation states, and primary pen tools.
- **Secondary (`#10B981` / `#059669`):** Vibrant Emerald. Dedicated to additive actions (Create Folder), success notifications, and secondary document tags.
- **Tertiary (`#F59E0B`):** Warm Golden Amber. Dedicated to favorites, starred status markers, and pinned notebook bookmarks.
- **Accent Blue (`#3B82F6`):** Sky/Cobalt blue for tool sub-actions, stylus status links, and cloud synchronization chips.
- **Surface Hierarchy:**
  - `Base / Canvas`: `#111115` (Deepest charcoal backdrop)
  - `Surface Container / Sidebars`: `#18181C` (Layer 1 containers and side drawer navigation)
  - `Card / Elevation Surface`: `#222228` (Interactive note tiles, folders, toolbar backgrounds)
  - `Borders / Dividers`: `rgba(255, 255, 255, 0.08)` (Crisp, low-contrast boundary delineations)
  - `Text High Contrast`: `#F9FAFB`
  - `Text Muted / Metadata`: `#9CA3AF`
  - `Text Subtle / Placeholder`: `#6B7280`

## Typography

The type system uses **Plus Jakarta Sans** across all roles to ensure geometric clarity and legibility when handling technical terminology, scientific units, and dense file structures.

### Hierarchy & Usage
- **Display & Large Headlines:** Used for view headers ("All Notes", document titles in reader mode) with tight letter-spacing to ground the workspace.
- **Section Headers (`headline-md`):** Delineates functional clusters like "Recent Folders" and "Recent Files".
- **Body Styles:** Scaled for rapid scanning of note metadata (page counts, timestamps, folder affiliations).
- **Labels & Microcopy:** Enhanced medium and semi-bold weights for badges, count tags, and tool size indicators to remain sharp against dark surfaces.

## Layout & Spacing

The layout is built around a dynamic adaptive grid designed for touch gestures and stylus interactions across phone, foldable, and tablet form factors.

### Grid & Responsiveness
- **Tablet / Foldable Landscape (Split View):** 
  - Fixed-width collapsible primary sidebar (280px to 320px) pinned to the left on `#18181C`.
  - Main workspace fills the remaining canvas on `#111115` with a fluid 3-column or 4-column card grid (`gutter-tablet: 1.25rem`).
- **Compact Mobile / Folded Screen:**
  - Sidebar folds into a sliding modal drawer triggered via a menu icon.
  - Cards stack into a single column or dual-column grid with `margin: 1rem` and `gutter: 1rem`.
- **Canvas Note View:**
  - Full-bleed workspace framed by a top utility bar (height: 56px) and docked or floating bottom control dock.
  - Touch/Stylus targets maintain a minimum dimension of 44×44dp with at least `space-sm` (8px) between adjacent interactive elements.

## Elevation & Depth

This system avoids heavy drop shadows, instead using **tonal surface stepping** combined with **subtle micro-borders** to express hierarchy and clickable affordance.

### Surface Tiers
- **Layer 0 (Canvas):** `#111115` - Background for editor sheets and primary content canvas.
- **Layer 1 (Panels & Navigation):** `#18181C` - Sidebar menu, persistent top app bar, and bottom navigation pill container.
- **Layer 2 (Interactive Modules & Cards):** `#222228` - Grid cards for folders, note previews, and floating action panels. Bordered by `1px solid rgba(255, 255, 255, 0.07)`.
- **Layer 3 (Floating Overlays & Tooltips):** `#2A2A32` - Stylus palette dropdowns, context popovers, and dialogs. Enhanced with subtle ambient depth: `box-shadow: 0 12px 32px -4px rgba(0, 0, 0, 0.6)`.

### Accent Lighting
- Active tools and selected navigation items utilize a slight internal glow or vibrant solid fill (`#DC2646`) that visually lifts the control out of the dark panel without muddying adjacent tools.

## Shapes

The design system implements a soft, modern geometry that blends rounded rectangles with full-radius pill buttons.

### Curvature Architecture
- **Primary Content Cards & Folders:** 16px to 20px (`rounded-lg` / `rounded-xl`), creating friendly, tangible notebook modules.
- **Action Buttons & Badges:** Fully rounded pills (`border-radius: 9999px`) for quick-action floating buttons, count badges, and tool selectors.
- **Micro UI & Indicators:** 8px to 12px for tool sub-panels, segmented toggles, and status tags.
- **Interactive Thumbnails:** Inner content blocks inside preview cards mirror outer radii with proportionate stepped corner radii (10px–12px).

## Components

### Buttons & Action Triggers
- **Primary Pill Action Button (Create File):** Full crimson fill (`#DC2646`), white text, bold icon prefix, height 48px, horizontal padding `space-lg`, pill radius. On hover/press: `#E63956`.
- **Secondary Pill Action Button (Create Folder):** Vibrant emerald fill (`#10B981`), white text, height 48px, pill radius.
- **Sidebar Active Item:** Solid crimson fill (`#DC2646`) with 12px border radius, containing white active icon, label, and pill badge for note count.
- **Sidebar Inactive Item:** Transparent fill, muted text (`#9CA3AF`), with high-contrast icon on hover/focus.

### Cards & Grid Containers
- **Folder Card:** Dark surface (`#222228`), 18px radius, subtle border (`rgba(255, 255, 255, 0.08)`). Top row features file count tag and category color swatch or tertiary star badge; bottom row features folder icon, bold title, and directional indicator.
- **Note Preview Card:** Two-tier vertical arrangement. Top aspect-ratio preview container (representing a simulated dark canvas sheet with formula/graph sketches); bottom area provides note title, modification date, and context menu trigger (`...`).

### Stylus & Editor Toolbar
- **Tool Strip:** Dark floating dock (`#18181C`) with 12px radius and crisp boundary stroke.
- **Tool Icons:** 36×36dp touch targets with icon glyphs. Selected pen/eraser receives a bright crimson highlight or circular background indicator.
- **Color Pickers:** Circular 20px swatches for ink colors (Crimson, Emerald, Sky Blue, Golden Amber) with an active white ring indicator on selection.
- **Status Badges (e.g., Stylus Connected):** Low-opacity tinted pill (`rgba(220, 38, 70, 0.15)`), red icon, label-sm text.

### Navigation Pill Dock
- **Floating Bottom Bar:** Docked horizontally centered with pill shape (`#18181C`), containing circular touch targets for Home/Notes, Folders, and Quick Draw stylus modes. Active tab highlighted in vibrant crimson.