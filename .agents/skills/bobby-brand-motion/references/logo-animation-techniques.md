# Logo animation techniques

## Protect official artwork

Identify the canonical logo file, approved variants, clear space, minimum size, colors, wordmark relationships, and any brand rules. Keep a static rendering available at every stage. Prefer animating a wrapper or approved SVG groups over editing source paths. Decorative shapes should be separately identifiable from the mark.

## Match technique to asset

| Asset | Suitable approaches | Check first |
| --- | --- | --- |
| Structured SVG | Animate existing groups, transforms, opacity, clip paths, or stroke reveal where drawing order is truthful | Meaningful layer boundaries, IDs, masks, viewBox, filters, accessible name, cross-browser behavior |
| Flattened SVG | Animate the whole mark or apply a reveal mask | Do not pretend the file contains separate parts or redraw paths without approval |
| PNG/WebP/raster | Whole-image motion, opacity, clipping or an approved mask | Resolution at hero size, transparent edges, color fidelity, no invented layers |
| Wordmark | Controlled entrance of the entire approved wordmark or genuine provided letter paths | Typography fidelity and readability throughout |

## Technology choice

- CSS transitions and keyframes: small finite entrances, hover response, simple transforms and opacity.
- SVG animation: vector-specific groups, paths, masks, and reveals when the file supports them.
- Motion for React: React/Next.js sequencing and interaction when already present or justified by the concept.
- GSAP: complex timelines or paths that are difficult to express and maintain with lighter tools.
- Rive or Lottie: use when the project has suitable approved assets, playback needs, and a sound export workflow.
- Three.js: reserve for meaningful 3D interaction tied to the brand; avoid for a simple logo entrance.

Check package cost and project conventions before adding a dependency. Design the static state first; animate toward it. Keep the logo recognizable during the transition, especially at mobile sizes. Use masks to reveal existing artwork rather than creating a replacement mark.

