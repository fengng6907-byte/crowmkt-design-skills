# Motion performance and implementation

## Rendering and loading

- Render the final logo footprint and meaningful hero content immediately. Reserve width, height, or aspect ratio to prevent layout shifts.
- Prefer transforms and opacity for frequent changes. Use SVG path, mask, blur, filter, or particle effects only where the concept needs them and test on target devices.
- Keep entrance finite; release `will-change` after motion and avoid idle animation loops or unnecessary GPU layers.
- Do not hold navigation, CTA, or headline behind a timeline. A failed animation should leave the static logo and controls available.
- Load only the assets needed for the visible hero. Check raster sharpness and SVG complexity at mobile and desktop sizes.

## Input and lifecycle

- Provide touch-safe behavior; hover must not be the only way to reveal the logo or meaning.
- Pointer motion should be restrained, optional, and reversible. Do not attach high-frequency state updates to every pointer event without a need.
- In React, cancel animation frames, timelines, observers, timers, and listeners on cleanup. Prevent duplicate entrances from development remounts or route transitions when they would be visible.
- If replay exists, give it a discoverable, keyboard-operable control with a meaningful label. Do not restart animation unexpectedly on focus.

## Reduced motion

Honor `prefers-reduced-motion: reduce` from first render. Show the complete, static approved logo and omit spatial travel, flashing, and looping decoration. If the preference changes during a session, stop ongoing motion and settle into the static state. A small opacity change is optional only when it remains comfortable and does not delay content.

## Evidence

Inspect desktop and mobile layouts; verify loading, resize, touch, keyboard, reduced motion, and fallback behavior. Use measured data when available, but never infer a score from code alone. Report device, browser, method, and any untested conditions alongside results.

