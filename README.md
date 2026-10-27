# Bobby Design Director v2.1

Two reusable agent skills for brand-led website direction and authentic logo hero motion:

- [`bobby-design-director`](.agents/skills/bobby-design-director/SKILL.md) directs the website and decides whether logo motion helps the hero.
- [`bobby-brand-motion`](.agents/skills/bobby-brand-motion/SKILL.md) analyzes the official logo and brand, proposes three distinct animation concepts, specifies the chosen direction, and implements it when authorized.

The skills work independently or together. Logo motion is optional. Both require the client's authentic brand assets and preserve the official mark.

## Installation

Clone this repository into a workspace that discovers project skills under `.agents/skills/`, or copy either skill folder into that location in your project. Keep each skill's `SKILL.md` and its `references/` files together. In a Codex setup that uses personal skills, copy a skill folder into `$CODEX_HOME/skills/` instead. Restart or refresh skill discovery if your agent does not immediately list newly added skills.

```text
.agents/skills/
├── bobby-design-director/SKILL.md
└── bobby-brand-motion/
    ├── SKILL.md
    └── references/
```

No third-party motion skill is required. If project-specific animation guidance is available, review its instructions and license before using it.

## How they work together

The Design Director establishes brand identity and the hero composition, then decides whether logo motion adds value. When it does, it routes the logo task to Brand Motion. Brand Motion inspects the real asset, proposes three different directions, recommends one, and produces an animation specification. For an explicit build request, it implements the selected or clearly specified concept and reviews the result. For AUDIT or PROPOSAL requests, it stops at the proposal until implementation is authorized.

Brand Motion can also be invoked directly for a logo animation task. Design Director can work without Brand Motion for sites whose hero benefits from a static logo.

## Example prompts

```text
Use $bobby-design-director to audit our homepage hero against the brand guidelines and recommend a visual direction. Evaluate whether the official logo should animate, but do not implement changes.

Use $bobby-brand-motion with our official SVG logo and current hero design. Propose three distinct logo animation concepts for our audience, recommend one, and provide a storyboard and reduced-motion plan.

Use $bobby-design-director and $bobby-brand-motion to implement a brand-appropriate hero in our React site. Inspect the official logo, propose three motion directions, choose the strongest one, and build it with mobile and reduced-motion behavior.
```

For Crow Marketing, Tuition Centre, and Technology Platform examples, see [animation storyboarding](.agents/skills/bobby-brand-motion/references/animation-storyboarding.md). These examples do not contain or replace any client's actual logo.

