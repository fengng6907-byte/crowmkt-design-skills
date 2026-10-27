---
name: bobby-brand-motion
description: Develop brand-specific website logo motion concepts, specifications, and authorized implementations using an authentic client logo. Use for hero logo animation, logo reveals, and logo interactions; skip for general page transitions or logo redesign.
---

# Bobby Brand Motion

Create a distinctive logo experience that serves the brand and hero composition. This skill works on its own or when called by `bobby-design-director`. A logo animation is optional; recommend a static treatment when motion adds little value.

## Establish the brief

Inspect the authentic logo and available brand guidelines before proposing motion. Record what is known about its shapes, colors, symbolism, typography, proportions, approved variants, file format, audience, industry, positioning, intended feeling, and the site's hero layout. Distinguish evidence from assumptions. Ask for missing official assets before implementing logo-specific motion if their absence would force invention.

Use [brand-motion-personalities.md](references/brand-motion-personalities.md) to choose a motion personality from the brand evidence, not from a preset. Check the hero headline, copy, CTA, background, navigation, loading sequence, and visual hierarchy. If the logo should remain still, explain why and specify a static or subtle presentation.

## Propose before building

For a custom logo animation, present **three distinct creative directions** before implementation. Each must include a name, brand rationale, intended feeling, ordered storyboard, estimated duration, easing and movement style, technology, mobile adaptation, reduced-motion fallback, and performance risks. Recommend the strongest direction and explain its fit. Use [animation-storyboarding.md](references/animation-storyboarding.md) for the proposal and handoff format.

For an AUDIT or PROPOSAL request, stop after the proposal unless implementation is separately authorized. For an explicit implementation request, continue with the selected or clearly specified concept; if none is selected, use the recommended concept and state the choice.

## Preserve the mark

Use the client's authentic logo. Keep its recognizable silhouette, approved colors, typography, and proportions. Do not substitute a generated logo, invent hidden layers, or alter the official artwork without approval. Inspect SVG structure before animating paths or groups. For raster logos, favor whole-image transforms, clipping or masking; reconstruct only from approved source artwork. Decorative motion may support the mark but must not overpower it. See [logo-animation-techniques.md](references/logo-animation-techniques.md).

## Specify and implement

Deliver a storyboard with timing, easing, interactions, asset requirements, and a meaningful static and reduced-motion state. Select the lightest technology that meets the concept and existing stack. Coordinate logo entrance with hero content and keep navigation and CTA usable throughout. Default to one intentional finite entrance; hover, pointer response, or explicit replay are optional. Do not autoplay an endless loop by default.

When implementation is authorized, build reusable components or assets appropriate to the project stack. Reserve the final logo's space before animation, render meaningful content without waiting for animation, support touch and mobile, and clean up observers, timers, listeners, and animation instances in React. Read [motion-performance.md](references/motion-performance.md) when choosing the technique and implementation details.

## Review and report

Use [logo-animation-qa.md](references/logo-animation-qa.md) to review visual consistency, smoothness, responsive layouts, accessibility, and runtime behavior. Respect `prefers-reduced-motion`, preserve logo readability, avoid intense flashing and excessive movement, and never block core interactions. Report what was actually tested; do not invent scores, devices, or results.

The final handoff contains the three-concept creative proposal and recommendation, animation specification, implementation when authorized, and quality review. For illustrative brand-specific behavior, see the examples in [animation-storyboarding.md](references/animation-storyboarding.md); they are specifications, not substitute assets.

