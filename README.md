# Granbury Design System

A dark, gradient-accented design system built for Granbury Carpet Cleaning.
The visual language (surfaces, gradients, card radii, type scale, spacing)
was reverse-engineered from a dark-navy dashboard reference. Brand assets
(logo, mascot, icon) are intentionally not included — drop your own logo
file into `design-system/brand/` and reference it from the sidebar mark
in `index.html`.

Open `index.html` in a browser for the full style guide, or serve the repo
locally: `python3 -m http.server 8080`.

## Structure

```
design-system/
  tokens.css       CSS custom properties: color, gradients, type, spacing, radius, shadow
  base.css         Reset + global typography utility classes
  components.css   Sidebar/nav, top bar, cards, stat cards, badges, buttons, list rows, chart bars
  brand/           Empty — add your logo file(s) here
index.html         Style guide + an applied mini-dashboard example
```

## Using the tokens

Every value lives in `design-system/tokens.css` as a CSS custom property, so
the system drops into any stack (plain HTML, React, Vue, etc.) — just link
the three CSS files in order (`tokens.css`, `base.css`, `components.css`)
and use the classes documented in the style guide, or reference the
`--color-*` / `--space-*` / `--radius-*` variables directly in new components.

Key choices pulled from the reference dashboard:

- **Surfaces**: near-black navy background with slightly lighter card
  panels, large corner radii (18–24px) on cards, tighter radii (8–12px) on
  buttons and nested boxes.
- **Gradients**: a warm orange→pink→magenta gradient for the primary hero
  stat card, and a cool purple→blue gradient for secondary accents and
  chart bars.
- **Type**: Poppins for headings and large stat numbers, Inter for body and
  UI text; big bold numerals are the dashboard's signature.
- **Spacing**: a 4px base scale (4/8/12/16/20/24/32/40/48).
- **Color-coded numbers**: purple/blue/green/orange used semantically to
  differentiate stat categories, mirrored here for job status counts.

## Brand assets

`design-system/brand/` is empty by design. Add your logo file(s) there and
point the sidebar mark in `index.html` (`.demo-brand`) at the real file
instead of the placeholder monogram.
