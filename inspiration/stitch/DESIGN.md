# Design System Documentation: The Gentle Guardian

## 1. Overview & Creative North Star
This design system is built to bridge the gap between clinical precision and maternal warmth. For a leading medical center in Bahrain specializing in fertility and women’s health, the digital experience must transcend the "cold clinic" aesthetic.

**Creative North Star: The Gentle Guardian**
The philosophy of this system is "Organic Tech." We combine the high-end, technologically advanced nature of modern fertility science with the empathetic, soft touch of a caregiver. We break the standard medical "template" by utilizing **intentional asymmetry**—placing text and imagery in an editorial fashion that mimics a premium lifestyle magazine rather than a sterile portal. Overlapping elements, such as images breaking the bounds of container edges, create a sense of movement and life.

## 2. Colors & Surface Philosophy
The palette is a sophisticated blend of deep teals, breathable neutrals, and calming blues. We avoid the clinical "hospital blue" in favor of tones that feel grounded and luxurious.

*   **Primary (`#216775`):** Our anchor of trust. Use this for authoritative actions and headlines.
*   **Surface & Background (`#fbf9f6`):** This is not a flat white; it is a warm, linen-inspired neutral that provides an immediate sense of comfort.

### The "No-Line" Rule
To maintain a high-end feel, **1px solid borders are strictly prohibited** for sectioning. Boundaries must be defined through:
1.  **Background Shifts:** Transitioning from `surface` to `surface-container-low`.
2.  **Tonal Transitions:** Using subtle shifts in the neutral scale to indicate a new content area.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers, like stacked sheets of fine Bahraini parchment.
*   **Level 0 (Base):** `surface` (`#fbf9f6`)
*   **Level 1 (Sections):** `surface-container-low` (`#f5f3f0`)
*   **Level 2 (Interactive Cards):** `surface-container-lowest` (`#ffffff`)
By nesting a `lowest` (pure white) card inside a `low` (light beige) section, you create a soft, natural lift without the need for dated shadows.

### The "Glass & Gradient" Rule
For floating navigation or high-impact hero sections, use **Glassmorphism**. Apply a semi-transparent `surface_variant` with a `backdrop-blur` of 20px. For primary CTAs, use a subtle linear gradient from `primary` (`#216775`) to `primary_dim` (`#0e5b69`) at a 135-degree angle to add "soul" and depth.

## 3. Typography
We use **Manrope** across the entire system. Its geometric yet rounded terminals strike the perfect balance between "technologically advanced" and "approachable."

*   **Display (lg/md):** Reserved for empathetic hero statements. Use `display-lg` (3.5rem) with tight tracking (-0.02em) to create a bold, editorial look.
*   **Headlines:** Use `headline-lg` for section headers. These should be paired with generous top-padding (Spacing 16 or 20) to let the typography breathe.
*   **Labels:** Use `label-md` (0.75rem) with increased letter-spacing (0.05em) in all-caps for a premium "boutique" feel.
*   **The Narrative Flow:** Use `title-lg` for sub-headers. Always ensure the line height for `body-lg` is set to 1.6x to ensure maximum legibility for patients who may be feeling stressed or overwhelmed.

## 4. Elevation & Depth
In this design system, depth is felt, not seen. We move away from traditional shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by "stacking." A `surface-container-highest` element should only exist on a `surface-container` background. This creates a natural hierarchy of importance.
*   **Ambient Shadows:** If a floating element (like a modal) is required, use a shadow with a 40px blur at 6% opacity, tinted with the `on-surface` color (`#313330`). Never use pure black shadows.
*   **The "Ghost Border" Fallback:** If accessibility requires a container definition, use the `outline-variant` token at **15% opacity**. It should be a suggestion of a border, not a hard line.

## 5. Components

### Buttons
*   **Primary:** High-pill shape (`rounded-full`). Background: `primary`. Text: `on-primary`. Apply a subtle `primary-container` inner-glow on hover.
*   **Secondary:** Ghost style. No background, `outline-variant` ghost border (20% opacity). Text: `primary`.
*   **Tertiary:** Text only with an underline that is 2px thick and offset by 4px, using the `primary_fixed_dim` color.

### Cards & Lists
*   **The "No-Divider" Mandate:** Dividers are forbidden. Separate list items using the spacing scale (e.g., `spacing-4` between items) or by placing each item on a `surface-container-low` pill.
*   **Patient Cards:** Use `surface-container-lowest` with `rounded-lg` (1rem). Content should be asymmetrical—left-aligned text with a thin-line icon floating in the top right.

### Input Fields
*   **Style:** Minimalist. No bottom line or full outline. Use a soft fill of `surface-container-high` with `rounded-md`. 
*   **Focus State:** The fill shifts to `surface-container-lowest` and a 2px "Ghost Border" of `primary` appears at 30% opacity.

### Specialized Components
*   **The "Care Timeline":** A vertical track for pregnancy or fertility journeys. Instead of a hard line, use a series of soft, blurred `primary_container` circles to indicate progress.
*   **Appointment Glass-Dock:** A floating bottom navigation bar using Glassmorphism (`surface` @ 70% opacity + blur) to keep essential booking actions always reachable.

## 6. Do's and Don'ts

### Do:
*   **Embrace White Space:** Use the `20` and `24` spacing tokens to separate major narrative blocks. Space is a luxury.
*   **Use Thin-Line Icons:** Use 1px or 1.5px stroke weights. Icons should feel like fine-line illustrations, not heavy blocks.
*   **Center on Empathy:** Align clinical data (like fertility charts) with supportive, human-centric copy.

### Don't:
*   **Don't use "Pure" Colors:** Avoid `#000000` or `#FFFFFF`. Always use the `on-surface` and `surface` tokens to maintain the soft, premium warmth.
*   **Don't Over-Animate:** Transitions should be "Liquid"—slow, easing-in-out (e.g., 400ms cubic-bezier). Avoid snappy or "bouncy" animations which feel immature.
*   **Don't Grid-Lock:** Allow images or decorative elements to "bleed" off-center. A rigid, centered grid feels like a generic template; asymmetry feels bespoke.