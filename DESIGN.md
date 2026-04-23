# Design System Strategy: The Architect of Transition

## 1. Overview & Creative North Star
**The Creative North Star: "The Luminous Monolith"**

In the world of energy transition and high-level consultancy, clarity is the ultimate currency. This design system moves away from the "busy" aesthetics of traditional corporate dashboards and embraces an editorial, high-end consulting feel. We are building a digital environment that feels like a private gallery or a premium architectural firm—authoritative, yet surprisingly personal.

We reject the standard "boxed-in" grid. Instead, we use **The Luminous Monolith** approach: massive, legible typography paired with deep, atmospheric tonal layering. The design breaks the "template" look through intentional asymmetry—placing content off-center to create active white space—and using the Teal accent not as a decoration, but as a "signal" of progress and energy.

## 2. Colors: Tonal Depth & The "No-Line" Rule
The palette is rooted in the deep void of `#071325` (Background), representing stability and the vast scale of the energy sector.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to define sections. Traditional lines create visual "noise" that diminishes the premium feel. 
- **Boundaries:** Define sections solely through background shifts. A `surface-container-low` section should sit directly against a `surface` background.
- **Nesting Hierarchy:** Use the `surface-container` tiers (Lowest to Highest) to create "nested" depth. Treat the UI as a series of physical layers—like sheets of darkened glass stacked in a lightless room. Each inner container uses a slightly higher tier (brighter) to define its importance.

### The "Glass & Gradient" Rule
To avoid a flat, "web 1.0" appearance, floating elements (like navigation bars or modal overlays) must utilize **Glassmorphism**.
- **Execution:** Use semi-transparent surface colors (e.g., `surface-container-high` at 70% opacity) with a `32px` backdrop-blur.
- **Signature Textures:** For main CTAs and Hero backgrounds, use a subtle radial gradient transitioning from `primary` (#5dd9d8) to `primary-container` (#00a3a3). This mimics the glow of clean energy and adds "soul" to the minimalist layout.

## 3. Typography: The Editorial Scale
We use a dual sans-serif system to balance modern authority with extreme legibility.

- **Display & Headlines (Manrope):** This is our "Architectural" voice. Manrope’s geometric structure feels engineered and precise. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to create a high-impact, editorial presence.
- **Body & Labels (Inter):** This is our "Clarity" voice. Inter is highly functional. Use `body-lg` (1rem) for most reading experiences to ensure the consultant's insights are easily digestible.
- **Hierarchy Strategy:** Create massive contrast. A `display-md` headline followed immediately by a `label-md` "kicker" creates a sophisticated, asymmetrical tension that looks custom-designed rather than templated.

## 4. Elevation & Depth: Tonal Layering
In this system, elevation is a light-source exercise, not a shadow exercise.

- **The Layering Principle:** Stacking determines importance.
    - **Base:** `surface` (#071325)
    - **Sectioning:** `surface-container-low` (#101c2e)
    - **Actionable Cards:** `surface-container-highest` (#2a3548)
- **Ambient Shadows:** Shadows should be almost invisible. Use a 4% opacity of the `on-surface` color with a massive 64px blur. This creates a "lift" that feels like an aura rather than a drop-shadow.
- **The "Ghost Border" Fallback:** If a container absolutely requires a boundary for accessibility, use the `outline-variant` token at **15% opacity**. This creates a "breath of a line" that guides the eye without trapping the content.

## 5. Components

### Buttons: The Kinetic Core
- **Primary:** No borders. Filled with the `primary` (#5dd9d8) to `primary-container` gradient. Text is `on-primary` (#003737). Use `DEFAULT` (0.25rem) roundedness for a sharp, professional edge.
- **Secondary:** Transparent background with the "Ghost Border" (outline-variant at 20%). On hover, transition to a 10% opacity `primary` fill.
- **Tertiary:** Text-only, using `primary` color. Use for low-priority actions like "Learn More."

### Cards & Lists: The Infinite Flow
- **Cards:** Forbid divider lines. Separate card content using `body-md` spacing (1.5rem to 2rem) and subtle background shifts between the card and the section it sits on. 
- **Lists:** Instead of dividers, use a `1px` vertical Teal accent line (24px height) next to the active or hovered list item to indicate selection.

### Inputs: The Sophisticated Form
- **Text Inputs:** Use `surface-container-low` as the background. Use a `bottom-only` ghost border. When focused, the border transitions to 100% `primary` teal. This keeps the forms feeling light and non-intrusive.

### Signature Component: The "Transition Gauge"
- **Purpose:** To visualize energy transition progress.
- **Design:** Use a thin, horizontal track (`surface-container-highest`) with a glowing `primary` teal fill. No labels on the bar—place percentages in `label-sm` above the bar for a clean, data-viz aesthetic.

## 6. Do's and Don'ts

### Do:
- **Do** embrace extreme white space. If a section feels "empty," it’s likely working.
- **Do** use the `tertiary` (#ffb690) color sparingly for "Alerts" or "Key Insight" highlights—it’s a warm contrast to the cool navy/teal.
- **Do** align text-heavy blocks to a 12-column grid but allow images or pull-quotes to break the grid and bleed off-canvas.

### Don't:
- **Don't** use 100% black. The deep navy `#071325` provides the premium "ink" feel we need.
- **Don't** use standard "Drop Shadows." They make the UI look like a 2014 material design clone. Stick to tonal shifts.
- **Don't** use icons unless absolutely necessary. Rely on strong typography and the teal accent to lead the user's eye.