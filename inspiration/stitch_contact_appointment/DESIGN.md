# Design System Strategy: The Editorial Clinical Standard

## 1. Overview & Creative North Star: "The Serene Curator"
This design system moves away from the sterile, rigid grids of traditional medical portals. Our Creative North Star is **"The Serene Curator."** It treats patient information not as data to be managed, but as a journey to be guided. 

By leveraging a high-end editorial aesthetic, we break the "template" look. We use intentional asymmetry—such as off-center hero text and overlapping image-to-surface containers—to create a sense of organic growth and human compassion. The experience should feel like a premium lifestyle publication: spacious, authoritative, and deeply calming.

## 2. Visual Language & Color Theory
The palette is rooted in deep teals and soft, sandy neutrals, reflecting the coastal sophisticated of Bahrain and the clinical precision of reproductive medicine.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders for sectioning or containment. 
Structure must be defined through **Background Color Shifts**. For example, a section using `surface-container-low` (#f6f3f2) should sit directly against a `surface` (#fcf9f8) background. This creates a "soft-edge" layout that feels modern and expensive.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Use the surface-container tiers to create depth:
*   **Base:** `surface` (#fcf9f8)
*   **Grouped Content:** `surface-container-low` (#f6f3f2)
*   **Interactive Cards:** `surface-container-lowest` (#ffffff) to create a subtle "pop" against the off-white background.

### The Glass & Gradient Rule
To avoid a "flat" digital feel, apply **Glassmorphism** to floating navigation bars or modal overlays. 
*   **Effect:** Use `surface` colors at 80% opacity with a `backdrop-blur` of 12px-20px. 
*   **Signature Gradients:** For primary CTAs or Hero backgrounds, use a subtle linear gradient from `primary` (#003942) to `primary_container` (#19505b) at a 135-degree angle. This adds "visual soul" and depth.

## 3. Typography: The Editorial Voice
We utilize a pairing of **Manrope** for high-impact display and **Inter** for clinical clarity.

*   **Display & Headline (Manrope):** These are our "Editorial" weights. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero headlines. This conveys the brand's high-end, authoritative nature.
*   **Body & Labels (Inter):** Used for trust and readability. `body-lg` (1rem) is the workhorse for patient education.
*   **Hierarchy Tip:** Always use `on_surface_variant` (#40484a) for secondary descriptions to maintain a soft contrast that reduces cognitive eye strain for patients in stressful situations.

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "tech." We achieve depth through atmospheric physics.

*   **The Layering Principle:** Instead of shadows, stack surface tiers. A `surface-container-high` card placed on a `surface-container-low` background creates a natural elevation.
*   **Ambient Shadows:** If a floating element (like a "Book Appointment" FAB) is required, use a shadow with a 40px blur, 0% spread, and 6% opacity. The shadow color must be a tint of `primary` (#003942), not pure black.
*   **The "Ghost Border" Fallback:** If a divider is absolutely necessary for accessibility (e.g., in complex form tables), use the `outline_variant` token at **15% opacity**. Never use 100% opaque lines.

## 5. Component Guidelines

### Buttons (The "Organic Touch")
*   **Primary:** High-contrast `primary` (#003942) background with `on_primary` (#ffffff) text. Use `md` (0.75rem) corner radius.
*   **Secondary:** `secondary_container` (#dae4e4) background. No border.
*   **Interaction:** On hover, primary buttons should transition to the gradient defined in the Color section, rather than just a darker flat color.

### Cards & Patient Info Blocks
*   **Rule:** Forbid divider lines.
*   **Structure:** Use vertical white space (`spacing-12` or `spacing-16`) to separate sections. Use a `surface-container-highest` (#e5e2e1) header bar within a card to distinguish titles from body content.

### Input Fields
*   **Style:** Minimalist. Use `surface_container_low` as the fill color.
*   **States:** On focus, transition the background to `surface_container_lowest` (#ffffff) and apply a 1px "Ghost Border" using the `primary` color at 30% opacity.

### Specialized Components
*   **The "Compassion Card":** A large-format card for doctor profiles or testimonials using `tertiary_fixed` (#e6e2dd) backgrounds and `display-sm` Manrope typography for quotes.
*   **Soft Progress Indicators:** For fertility journey tracking, use thick, rounded bars (12px height) with `primary_fixed` (#b7ebf8) backgrounds and `primary` indicators.

## 6. Do's and Don'ts

### Do:
*   **Embrace Negative Space:** If a section feels "empty," leave it. Large margins (`spacing-24`) signal luxury and calmness.
*   **Use Tonal Shifts:** Use `surface_dim` (#dcd9d9) for footer areas to anchor the page.
*   **Layer Images:** Allow images of clinicians or facilities to slightly overlap the edge of their container for a bespoke, non-grid feel.

### Don't:
*   **Don't use pure black:** Use `on_background` (#1b1c1c) for text to keep the interface feeling "soft clinical" rather than "harsh digital."
*   **Don't use sharp corners:** Never use `none` or `sm` roundedness scales for cards or buttons. Stick to `md` (0.75rem) and `lg` (1rem) to maintain a compassionate, approachable feel.
*   **Don't use standard Dividers:** If content needs separation, use a 32px or 48px gap from the Spacing Scale instead of a line.