# ThunderNotes — Stitch Frontend UI

Static front-end mockups for **ThunderNotes**, a tablet-first note-taking app.
Every page is a single self-contained `code.html` (plain HTML + Tailwind CSS CDN
+ Lucide / inline SVG). No build step, no frameworks — Stitch-compatible.

## Pages

| Folder | Screen | Notes |
|---|---|---|
| `ThunderHomePage/` | Library home | Dashboard: recent folders, recent files, floating create dock |
| `NotesLibraryPage/` | All Notes | Filter chips + `Import Note` (blue) / `Create Note` (red) actions |
| `FoldersLibraryPage/` | All Folders | Filter chips + `Create Folder` (emerald) action |
| `CreateNotePage/` | Create-note modal | Quick-create sheet over a dimmed library |
| `CoverSelectionPage/` | Cover picker | Template browser with cover/paper previews |
| `CreateFolderPage/` | Create-folder modal | Folder creation sheet with color swatches |
| `CanvasLayoutPage/` | Canvas (base) | Lecture sheet, pen tray, zoom + AI-snip controls |
| `CanvasCustomizationPage/` | Canvas + popups | Pen / palettes / shape / line-type popups (closable) |
| `CanvasSettingsPage/` | Canvas + settings | Floating settings popup + Equation-Snip OCR modal |
| `CanvasUtilityPage/` | Canvas + utilities | Pages sidebar, radial AI-snip fan menu, context menu |

`Icons/` holds the original SVG icon assets; `DESIGN.md` in each page folder is
the original Stitch design-token spec.

## Shared conventions

- **Design tokens** live in each page's `tailwind.config` (`surface.*`, `accent.*`
  on library pages; `obsidian.*`, `thunder.*` on canvas pages). Prefer these over
  raw hex values.
- **Icons**: library pages use Lucide (`<i data-lucide="…">` rendered by
  `lucide.createIcons()` at the end of `<body>`); canvas pages use hand-drawn
  inline SVG.
- **Anatomy comments**: each file is annotated `[1] status bar … [4] gesture dock`
  so sections can be located quickly. Keep comments in sync with the markup.
- **Interactive bits** (pure JS, no frameworks):
  - Canvas pages: tapping a pen in the tray toggles its active (lifted) state;
    customization popups close via their `✕` buttons.
  - Theme / finger-stylus / bookmark toggles are CSS-only (`peer` + `has-[:checked]`).

## Responsive behavior

The layout is a fluid flex column capped at a 1600 px chassis (library pages) or
full-bleed (canvas pages). Verified free of horizontal overflow from 480 px up
to 1280 px; grids step 1 → 2 → 3 → 4 columns at Tailwind's `sm` / `lg` / `xl`
breakpoints. Desktop reference composition: 1280 × 1024.
