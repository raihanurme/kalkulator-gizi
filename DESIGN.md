---
name: Pastel Health & Nutrition
colors:
  surface: '#fff8f8'
  surface-dim: '#e6d6dc'
  surface-bright: '#fff8f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#fff0f5'
  surface-container: '#faeaef'
  surface-container-high: '#f4e4ea'
  surface-container-highest: '#efdee4'
  on-surface: '#22191d'
  on-surface-variant: '#544249'
  inverse-surface: '#372e32'
  inverse-on-surface: '#fdecf2'
  outline: '#87717a'
  outline-variant: '#dac0c9'
  surface-tint: '#a43073'
  primary: '#a43073'
  on-primary: '#ffffff'
  primary-container: '#f472b6'
  on-primary-container: '#6d0047'
  inverse-primary: '#ffafd3'
  secondary: '#a93349'
  on-secondary: '#ffffff'
  secondary-container: '#fe7488'
  on-secondary-container: '#730425'
  tertiary: '#006d3e'
  on-tertiary: '#ffffff'
  tertiary-container: '#49b275'
  on-tertiary-container: '#003f21'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#ffd8e7'
  primary-fixed-dim: '#ffafd3'
  on-primary-fixed: '#3d0026'
  on-primary-fixed-variant: '#85145a'
  secondary-fixed: '#ffdadc'
  secondary-fixed-dim: '#ffb2b9'
  on-secondary-fixed: '#400010'
  on-secondary-fixed-variant: '#891933'
  tertiary-fixed: '#8ff8b4'
  tertiary-fixed-dim: '#73db9a'
  on-tertiary-fixed: '#00210f'
  on-tertiary-fixed-variant: '#00522d'
  background: '#fff8f8'
  on-background: '#22191d'
  surface-variant: '#efdee4'
typography:
  display-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 40px
    fontWeight: '700'
    lineHeight: 48px
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 28px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.015em
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 22px
    fontWeight: '600'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  title-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '600'
    lineHeight: 22px
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
    fontWeight: '700'
    lineHeight: 14px
    letterSpacing: 0.04em
  data-metric:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 28px
    letterSpacing: -0.02em
rounded:
  sm: 0.5rem
  DEFAULT: 1rem
  md: 1.5rem
  lg: 2rem
  xl: 3rem
  full: 9999px
spacing:
  gutter: 1rem
  margin: 1.25rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

This design system embodies an encouraging, warm, and restorative digital sanctuary tailored for everyday health, mindful nutrition, and macro tracking. Rather than presenting numbers with sterile clinical detachment or intimidating athletic intensity, the visual language radiates gentle empathy, celebration, and accessible clarity.

The style unites soft minimalism with tactile, pillowy surfaces. It leverages luminous cream backdrops, velvety rose accents, and intuitive pastel color-coding for macronutrients. Interactive elements feature inviting, generous tap targets with subtle springiness that make daily logging feel rewarding rather than tedious. Micro-interactions evoke feelings of calm accomplishment, while high-contrast utilitarian typesetting keeps vital nutrition data legible at a glance.

## Colors

The palette establishes an airy, restorative light mode constructed on soft creamy whites (`#FFFDFD`, `#FFF5F7`) and delicate rose quartz tints (`#FCE7F3`). 

- **Primary (`#F472B6`)**: Directs focal attention, active states, key CTA fills, and primary navigation indicators. High-emphasis text overlays on top of light containers utilize deep rose tones (`#DB2777` or `#37272F`) to preserve strict accessibility standards.
- **Macronutrient Tokens**:
  - **Protein (`#FB7185`)**: A vibrant berry-rose accentuating lean power.
  - **Carbohydrates (`#FDBA74`)**: A warm, uplifting peach representing sustained energy.
  - **Fats (`#86EFAC`)**: A refreshing, pastel matcha denoting nourishing balance.
  - **Energy & Daily Burn (`#F43F5E`)**: A kinetic soft magenta reserved for caloric target arcs and milestone celebrations.
- **Neutrals & Legibility**: Body typography never sits in pure black; instead, it relies on deep berry-tinted charcoal (`#37272F`) paired with soft mineral rose (`#71656A`), eliminating visual harshness while exceeding WCAG AA/AAA contrast ratios against creamy container backings.

## Typography

The typographic hierarchy balances warmth and utilitarian precision. 

- **Headlines & Labels (Plus Jakarta Sans)**: Featuring generous aperture, organic terminal curvature, and modern geometric rhythm, Plus Jakarta Sans handles titles, quick tags, macro labels, and quantitative metrics. It conveys a cheerful, encouraging, and contemporary personality.
- **Body & Continuous Copy (Inter)**: Inter governs long descriptions, ingredient breakdowns, nutrition facts, and educational tips. Its tall x-height and neutral geometry ensure fatigue-free reading even on small handheld displays.
- **Metrics (`data-metric`)**: Nutritional totals and gram figures are rendered in tight, bold Plus Jakarta Sans for instant visual parsing during meal logging.

## Layout & Spacing

This design system uses a mobile-first 4-column fluid layout that seamlessly expands into 8-column and 12-column frameworks for tablet and desktop viewports. 

- **Mobile Rhythm**: Built around an 8pt base grid with a 4pt sub-grid for badges, macro bars, and micro-spacers. Outer canvas margins default to `margin` (20px / 1.25rem) to provide a soft breathing perimeter away from mobile hardware edges.
- **Pill Spacing**: Interactive elements such as macro badges and logged ingredient pills utilize `space-xs` (4px) to `space-sm` (8px) interior gap structures, maintaining tight cohesiveness.
- **Content Stacking**: Metric cards, meal blocks, and progress modules are separated by consistent `space-md` (16px) or `space-lg` (24px) intervals, preventing data clutter and visual fatigue.

## Elevation & Depth

Visual hierarchy relies on warm ambient luminescence and tinted surface layers rather than harsh drop shadows.

- **Ambient Tinted Shadows**: Shadows carry a warm, faint rose-mauve tint (`rgba(175, 77, 115, 0.08)`) instead of standard achromatic black. This preserves the creamy pastel quality of the UI.
- **Depth Layers**:
  - **Level 0 (Canvas Base)**: `#FFFDFD` or `#FFF5F7`. Flat, resting background.
  - **Level 1 (Card & Module Resting)**: Crisp `#FFFFFF` surface accompanied by a soft, highly-diffused bloom: `0px 8px 24px -4px rgba(219, 39, 119, 0.06), 0px 2px 6px -1px rgba(55, 39, 47, 0.03)`.
  - **Level 2 (Active Sheets & Sticky Bars)**: Surface `#FFFFFF` with expanded ambient projection: `0px 16px 36px -6px rgba(219, 39, 119, 0.12)`.
  - **Level 3 (Floating Action & Overlays)**: Accent buttons and bottom snackbars resting above translucent backdrop blurs (`backdrop-filter: blur(16px)` with 85% opacity `#FFF5F7`).
- **Tactile Soft Borders**: Elements utilize whisper-soft perimeter strokes (`1px solid rgba(244, 114, 182, 0.2)`) to delineate edges cleanly against white surfaces without adding visual bulk.

## Shapes

The visual geometry employs an organic, pill-centric form factor (level `3`) that reinforces warmth and gentleness across every boundary.

- **Micro Components (Chips, Tags, Buttons)**: Formed as perfect capsule pills (`border-radius: 9999px`), creating playful, smooth targets for fingertips.
- **Content Cards**: Styled with generous radii (`rounded-2xl` / 1.5rem to `rounded-3xl` / 2rem), cradling metrics, meal photos, and nutrition summaries within friendly curved boundaries.
- **Progress Arcs & Trackers**: All ends of progress bars, calorie track rings, and macro dividers use rounded cap ends (`stroke-linecap: round`), upholding systemic softness throughout the data visualizations.

## Components

### Buttons
- **Primary Action**: Pill-shaped capsule filled with `#F472B6`, housing white bold text (`label-lg`). Includes a subtle glowing underside shadow (`0px 8px 18px -2px rgba(244, 114, 182, 0.4)`). Active state applies a tactile scale compression (`transform: scale(0.97)`).
- **Secondary Action**: Pill container filled with `#FCE7F3` and deep rose label text (`#DB2777`). Zero border, effortlessly clean.
- **Tactile Quick Add ("+")**: Circular 48x48px pill floating button colored in primary rose with a crisp white icon, delivering instantaneous meal logging.

### Nutrition Cards
- **Macro Summary Card**: Encased in high-radius pure white containers (`rounded-3xl`), displaying the circular calorie ring alongside three distinct macro pill capsules:
  - Carbs: `#FDBA74` tint with dark peach text.
  - Protein: `#FB7185` tint with dark berry text.
  - Fat: `#86EFAC` tint with forest matcha text.
- **Meal Log Card**: Displays meal category (e.g., Breakfast, Midday Snack) with soft badge icons, aggregate calories in `data-metric`, and an expandable itemized list of ingredients.

### Chips & Badges
- Ultra-rounded pill tags utilizing a subtle pastel fill (`5% - 12%` opacity of the relevant macro or brand color) with saturated foreground text. Designed for dietary indicators (e.g., "High Protein", "Gluten-Free", "Hydration").

### Form Fields & Log Inputs
- Text and numerical inputs sit on `#FFF5F7` pill-rounded boxes with interior padding of `space-md`. Border begins as transparent and smoothly transitions to a soft `#F472B6` halo upon focus. Label headers use `label-md` in `#71656A`.

### Lists & Segmented Controls
- Item rows separated by gentle whitespace (`space-sm`) rather than solid dividing lines.
- Segmented switches (e.g., Day / Week / Month) sit inside an encompassing `#FCE7F3` pill track, with the active tab morphing via an elevated `#FFFFFF` rounded indicator.

### Progress Rings & Water Trackers
- Circular trackers feature a thick pastel track (`#FCE7F3`) overlaid with smooth animated fills in `#F43F5E` (Calories) and `#38BDF8` (Water). Center cavity holds the remaining deficit or surplus highlighted via `display-lg-mobile`.