# Granbury Design System

A dark, gradient-accented design system built for Granbury Carpet Cleaning.
The visual language (surfaces, gradients, card radii, type scale, spacing)
was reverse-engineered from a dark-navy dashboard reference; the brand marks
were adapted from the Granbury Carpet Cleaning logo and mascot.

Open `index.html` in a browser for the full style guide, or serve the repo
locally: `python3 -m http.server 8080`.

## Structure

```
design-system/
  tokens.css       CSS custom properties: color, gradients, type, spacing, radius, shadow
  base.css         Reset + global typography utility classes
  components.css   Sidebar/nav, top bar, cards, stat cards, badges, buttons, list rows, chart bars
  brand/
    logo.svg       Full lockup (mascot + wordmark)
    mascot.svg     Standalone mascot illustration
    icon.svg       Compact square mark for sidebars/favicons
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

`design-system/brand/logo.svg`, `mascot.svg`, and `icon.svg` are vector
recreations of the Granbury Carpet Cleaning mark, built to match the
original's color palette (red/blue wordmark, black outline, blue-uniformed
mascot). They were redrawn from the reference image rather than copied
byte-for-byte — if you have the original production artwork (AI/EPS/PNG),
drop it into `design-system/brand/` under the same filenames to replace
these placeholders with pixel-exact versions; nothing else needs to change
since the CSS/HTML only reference the filenames.
