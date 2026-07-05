---
name: Skill Wiring Probe
colors:
  surface: '#f8f9ff'
  surface-dim: '#cbdbf5'
  surface-bright: '#f8f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eff4ff'
  surface-container: '#e5eeff'
  surface-container-high: '#dce9ff'
  surface-container-highest: '#d3e4fe'
  on-surface: '#0b1c30'
  on-surface-variant: '#45464d'
  inverse-surface: '#213145'
  inverse-on-surface: '#eaf1ff'
  outline: '#76777d'
  outline-variant: '#c6c6cd'
  surface-tint: '#565e74'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#131b2e'
  on-primary-container: '#7c839b'
  inverse-primary: '#bec6e0'
  secondary: '#006a61'
  on-secondary: '#ffffff'
  secondary-container: '#86f2e4'
  on-secondary-container: '#006f66'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#07006c'
  on-tertiary-container: '#7073ff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dae2fd'
  primary-fixed-dim: '#bec6e0'
  on-primary-fixed: '#131b2e'
  on-primary-fixed-variant: '#3f465c'
  secondary-fixed: '#89f5e7'
  secondary-fixed-dim: '#6bd8cb'
  on-secondary-fixed: '#00201d'
  on-secondary-fixed-variant: '#005049'
  tertiary-fixed: '#e1e0ff'
  tertiary-fixed-dim: '#c0c1ff'
  on-tertiary-fixed: '#07006c'
  on-tertiary-fixed-variant: '#2f2ebe'
  background: '#f8f9ff'
  on-background: '#0b1c30'
  surface-variant: '#d3e4fe'
typography:
  display:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  mono-label:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  button:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  gutter: 16px
  margin: 24px
---

## Brand & Style
The design system is engineered for **Skill Wiring Probe**, a deterministic verification utility. The brand personality is grounded, precise, and utilitarian, prioritizing "calm productivity" over marketing flair. It targets developers and system operators who require high information density without cognitive overload.

The visual style is **Corporate / Modern** with a lean toward **Minimalism**. It avoids unnecessary ornamentation, focusing on structural alignment, clear hierarchy, and functional affordances. The goal is to evoke a sense of reliability and technical mastery, similar to a high-end IDE or a mission-critical operations dashboard.

## Colors
The palette is rooted in a professional technical spectrum. 
- **Primary:** Deep Slate (#0F172A) is used for headers, primary text, and grounding elements to establish authority.
- **Accent:** Technical Teal (#0D9488) serves as the primary action color, providing a distinct but calm focal point.
- **Semantic:** Emerald, Amber, and Rose are used strictly for status signaling (Ready, Paused, Error), ensuring immediate diagnostic recognition.
- **Surfaces:** A crisp white surface sits atop a soft Slate-50 canvas to define workspace boundaries without heavy borders.

## Typography
This design system utilizes **Inter** for its exceptional legibility in data-heavy environments. For technical metadata, IDs, and code snippets, **JetBrains Mono** is introduced to provide a clear distinction between prose and system data.

The type scale is intentionally constrained to maintain density. High-contrast weights (600 for headers) are used sparingly to guide the eye, while body text stays within the 12px-16px range to maximize the visibility of complex information grids.

## Layout & Spacing
The system employs a **Fixed Grid** philosophy on desktop and a **Fluid Grid** on mobile. A strict 4px/8px incremental rhythm ensures a compact, professional feel.

- **Desktop:** 12-column grid with a max-width of 1440px. 16px gutters provide sufficient breathing room for dense data tables.
- **Density:** Components use "Compact" vertical padding (8px) by default to ensure maximum information is visible above the fold.
- **Reflow:** On tablet and mobile, complex data tables should transition to a "Stacked Card" view or implement horizontal scrolling with sticky primary columns.

## Elevation & Depth
Depth is conveyed through **Tonal Layers** and **Low-contrast outlines** rather than heavy shadows. 

1.  **Level 0 (Canvas):** The base background layer (#F8FAFC).
2.  **Level 1 (Surface):** White cards and containers, defined by a 1px solid border (#E2E8F0).
3.  **Level 2 (Interaction):** Subtle, tight shadows (4px blur, 0.05 opacity) are used only for floating elements like dropdowns or tooltips to separate them from the content grid.

This flat-but-layered approach maintains the "calm" aesthetic while providing clear structural separation.

## Shapes
The design system uses a **Soft (1)** roundedness profile (0.25rem / 4px). This subtle rounding softens the technical edge of the UI without appearing too consumer-focused or "bubbly." 

- **Small elements (Checkboxes, Tags):** 2px radius.
- **Standard elements (Buttons, Inputs):** 4px radius.
- **Large elements (Cards, Modals):** 8px radius.

## Components

### Buttons
- **Primary:** Teal background, White text. High contrast for critical path actions.
- **Secondary:** White background, Slate-200 border, Slate-900 text. Used for standard utility actions.
- **Ghost:** No background or border. Slate-600 text. Used for secondary navigation or subtle toolbar actions.

### Status Tiles
Small, high-density blocks used for "at-a-glance" metrics. They should feature a 4px vertical accent bar on the left indicating status (Emerald, Amber, or Rose) and use `mono-label` for numerical data.

### Data Tables
Tables are the core of the utility. Use a 1px horizontal stroke for row separation. Headers should be `body-sm` in all-caps with `mono-label` styling. Row height should be fixed at 40px for maximum density.

### Form Fields
Inputs use a white background with a 1px border. Validation states (Error/Success) must use both color (Rose/Emerald) and a supporting icon to ensure accessibility.

### Utility Toolbar
A persistent horizontal bar (height: 48px) at the top of data views containing filters, search, and view toggles. Use ghost buttons here to keep the focus on the data itself.