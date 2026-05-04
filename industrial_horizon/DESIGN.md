# Design System Strategy: Precision Tectonics

## 1. Overview & Creative North Star
The "Creative North Star" for this design system is **The Industrial Monolith**. This concept treats the digital interface as a piece of high-end architectural engineering—imposing, precise, and undeniably stable. We are moving away from the "web-template" aesthetic to create an editorial experience that reflects the massive scale of energy technology.

To break the standard grid, we utilize **Intentional Asymmetry**. This means hero elements might be offset from the center, and industrial imagery should "bleed" off the edges of the screen or overlap container boundaries. By layering high-contrast typography over deep, tonal surfaces, we convey the brand’s international authority and technological sophistication.

## 2. Colors & Tonal Architecture
The palette is rooted in a spectrum of deep "Power Blues" and "Architectural Whites." This is not a flat design; it is a system of depth.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections or cards. Boundaries must be established through:
*   **Background Shifts:** Transitioning from `surface` (#f7f9ff) to `surface-container-low` (#f1f4fa).
*   **Tonal Transitions:** Defining an area by placing a `surface-container-lowest` (#ffffff) element against a `surface-dim` (#d7dae0) background.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the surface-container tiers to create "nested" depth:
*   **Level 0 (Base):** `surface` (#f7f9ff) for the primary page background.
*   **Level 1 (Sectioning):** `surface-container-low` (#f1f4fa) for large content blocks.
*   **Level 2 (Interaction):** `surface-container-lowest` (#ffffff) for the highest-priority cards or interactive zones.

### The "Glass & Gradient" Rule
To evoke a premium, high-tech feel, floating elements (like navigation bars or modal overlays) must use **Glassmorphism**. Combine `surface` colors at 80% opacity with a `20px` backdrop-blur. 
*   **Signature Textures:** For primary CTAs or high-impact hero backgrounds, use a subtle linear gradient from `primary` (#002e69) to `primary_container` (#004494) at a 135-degree angle. This adds a "soul" to the color that flat hex codes cannot achieve.

## 3. Typography: Editorial Authority
We utilize **Inter** across all scales to provide a clean, international system font feel that mirrors the precision of industrial engineering.

*   **Display Scale (The Statement):** Use `display-lg` (3.5rem) for high-impact metrics or hero headlines. Keep letter-spacing at -0.02em to give it a "pressed" editorial look.
*   **Headline Scale (The Narrative):** `headline-lg` (2rem) and `headline-md` (1.75rem) are the workhorses. They should always be in `on_surface` (#181c20) to ensure maximum contrast and authority.
*   **Body & Labels:** `body-md` (0.875rem) is used for technical descriptions. Ensure a line-height of 1.6 to maintain readability amidst complex industrial data. Use `label-md` in `on_surface_variant` (#434751) for metadata or captions.

## 4. Elevation & Depth
In this system, depth is a functional tool, not a decoration. We convey hierarchy through **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by stacking. Place a `surface-container-lowest` card on a `surface-container-low` section. This creates a soft, natural "lift" that mimics high-end stationery or architectural panels.
*   **Ambient Shadows:** When a floating effect is required, shadows must be extra-diffused. Use a blur of 32px to 64px with an opacity of 4%–6%. The shadow color must be a tinted version of `on_surface` (e.g., `rgba(24, 28, 32, 0.06)`), never pure black.
*   **The "Ghost Border" Fallback:** If a boundary is strictly required for accessibility, use the **Ghost Border**: the `outline_variant` (#c3c6d3) token at 15% opacity. This creates a "suggestion" of a line rather than a hard break.

## 5. Components

### Buttons
*   **Primary:** Background of `primary` (#002e69) with a 45-degree subtle gradient to `primary_container`. 0.25rem (sm) corner radius.
*   **Secondary:** Ghost-style. No background. `outline` (#737783) at 20% opacity with `primary` text.
*   **Interaction:** On hover, primary buttons should shift slightly toward `on_primary_container` (#91b5ff) to simulate an "electric glow."

### Cards & Industrial Lists
*   **Constraint:** Zero divider lines. 
*   **Structure:** Use vertical whitespace (32px or 48px) to separate items. For lists, use alternating background tints between `surface` and `surface-container-low` to distinguish rows.
*   **Cards:** Use `surface-container-lowest` with a "Ghost Border." If the card represents a high-level industrial asset, use a full-bleed industrial image at the top with a subtle 2px `primary` accent bar at the very bottom.

### Input Fields
*   **Structure:** "Underline" style refined. Instead of a box, use a `surface-container-highest` (#dfe3e8) background with a 2px `primary` bottom border that animates from the center outward on focus.
*   **Typography:** Labels use `label-md` in `on_surface_variant`.

### Technical Chips
*   **Industrial Status:** Use `secondary_container` (#5db8fe) with `on_secondary_container` (#00476f) text for active statuses. Roundedness should be `full` (9999px) to contrast against the sharp, architectural layout of the rest of the UI.

## 6. Do's and Don'ts

### Do:
*   **Do** use massive industrial imagery that utilizes the `primary` blue tones. 
*   **Do** allow for "White Space as a Luxury." Give components room to breathe to convey an "International Corporate" scale.
*   **Do** use the `tertiary` (#1d3246) color for specialized technical data or dark-mode-style footer sections to ground the design.

### Don't:
*   **Don't** use 100% opaque, high-contrast borders. They "trap" the eye and break the fluid, architectural feel.
*   **Don't** use standard drop-shadows. If an element doesn't feel elevated through color alone, re-evaluate the surface nesting.
*   **Don't** use generic iconography. Use thick-stroke (2pt), professional-grade icons that match the `outline` token weight.
*   **Don't** crowd the information. If a page feels "busy," increase the vertical spacing by one increment in the scale.