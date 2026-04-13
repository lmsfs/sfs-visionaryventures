# Design System Document: High-End Editorial Marketplace

## 1. Overview & Creative North Star

### The Creative North Star: "The Academic Curator"
This design system moves away from the traditional, cluttered e-commerce aesthetic toward a high-end editorial experience. It treats the student marketplace not as a "store," but as a curated exhibition of innovation. By utilizing a high-contrast palette of **Primary Red (#a80033)**, deep blacks, and nuanced whites, we evoke the prestige of an elite institution combined with the bold energy of a modern design gallery.

### Breaking the Template
To achieve a "signature" look, we reject the rigid, boxed-in grid. Instead, we utilize:
*   **Intentional Asymmetry:** Hero sections and category headers should use staggered typography to create a sense of movement.
*   **Layered Depth:** We move beyond flat design by treating the interface as a series of stacked, physical materials—fine paper, frosted glass, and bold lacquer.
*   **Editorial Spacing:** Large, luxurious gutters and whitespace aren't just empty; they are a design element that signals premium quality and allows the student products to "breathe."

---

## 2. Colors

The palette is rooted in a high-contrast triad of Red, Black, and White, but executed with sophisticated tonal shifts to prevent visual fatigue.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. Boundaries must be defined through background color shifts.
*   Use `surface` (#f9f9f9) for the main page body.
*   Transition to `surface-container-low` (#f3f3f4) or `surface-container` (#eeeeee) for secondary product sections or sidebars.
*   This creates "soft" boundaries that feel modern and high-end rather than structural and "templated."

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers.
*   **Base:** `surface` (#f9f9f9)
*   **Elevated Sections:** Use `surface-container-lowest` (#ffffff) for product cards to make them "pop" against the slightly greyish background.
*   **Interactive Containers:** Use `surface-container-highest` (#e2e2e2) for search bars or filtering areas to anchor the user’s eye.

### The "Glass & Gradient" Rule
To add "soul" to the high-contrast theme:
*   **CTAs:** Use a subtle gradient from `primary` (#a80033) to `primary_container` (#d31145) for primary action buttons.
*   **Floating Elements:** Navbars or sticky category filters should use `surface_container_lowest` at 85% opacity with a `backdrop-blur` (20px). This "frosted glass" effect integrates the UI into the content.

---

## 3. Typography: The Manrope Scale

Manrope is our sole typeface—a modern, geometric sans-serif that balances technical precision with accessibility.

*   **Display (lg/md):** Reserved for hero titles (e.g., "Athletics"). Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) to mimic a high-fashion magazine masthead.
*   **Headline (lg/md):** Used for category titles (e.g., "MS Toys"). These should be bold and authoritative using the `on_surface` color.
*   **Title (lg/md):** Product names. Pair `title-lg` (1.375rem) with a slightly heavier weight to ensure the product is the star of the grid.
*   **Body (lg/md):** All product descriptions. Use `on_surface_variant` (#5c3f41) to create a subtle tonal difference from the title, enhancing readability.
*   **Labels:** Use `label-md` (0.75rem) in all-caps with increased letter-spacing for category tags (e.g., "NEW ARRIVAL" or "STUDENT BUILT").

---

## 4. Elevation & Depth

We avoid the "shadow-heavy" look of 2010-era design, favoring **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. The subtle shift in hex code creates a "soft lift" that is felt rather than seen.
*   **Ambient Shadows:** If a floating effect is required (e.g., a "Buy" modal), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(26, 28, 28, 0.06)`. The shadow color is a tint of our `on_surface`, not a generic black.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline_variant` (#e4bdbf) at 20% opacity. Never use 100% opaque borders.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` (#a80033) with `on_primary` (#ffffff) text. Use `roundness.md` (0.375rem). On hover, transition to `primary_container`.
*   **Secondary:** No fill. Use a "Ghost Border" of `primary` at 30% opacity. Text remains `primary`.
*   **Tertiary:** No border, no fill. High-contrast `on_surface` text with an underline that appears only on hover.

### Product Cards
*   **Structure:** Forbid divider lines. Use `surface_container_lowest` (#ffffff) for the card background.
*   **Spacing:** Use a 24px internal padding. The image should be flush to the top but have a subtle `roundness.sm` (0.125rem) to soften the "Brutalist" edges.
*   **Interaction:** On hover, the card should not lift. Instead, the image should subtly scale (1.05x) within its frame to signify interactivity.

### Chips (Category Filters)
*   **Filter Chips:** Use `secondary_container` (#e2e2e2) with `on_secondary_container` (#646464) text.
*   **Selected State:** Transition to `primary` (#a80033) background with `on_primary` text to maintain the high-contrast theme.

### Input Fields
*   **Style:** Minimalist. Only a bottom border using `outline_variant` (#e4bdbf).
*   **Focus State:** The bottom border transforms into a 2px `primary` line. Use `body-md` for placeholder text in `on_surface_variant`.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts for category headers (e.g., text left-aligned, image right-aligned with a 10% vertical offset).
*   **Do** use `primary` red sparingly as an accent—it should feel like a "stamp of quality," not a background wash.
*   **Do** prioritize vertical whitespace over lines. If sections feel too close, double the padding rather than adding a divider.

### Don't
*   **Don't** use pure black (#000000). Use `on_surface` (#1a1c1c) to keep the design feeling "inked" rather than "digital."
*   **Don't** use 100% rounded corners (pills) for product cards. Stick to `md` (0.375rem) to maintain a sophisticated, architectural feel.
*   **Don't** use standard drop shadows. If it looks like a "box shadow," it’s too heavy. It should look like "ambient light."

---

## 7. Category Specific Direction
*   **Athletics:** Use larger `display-md` typography to convey energy.
*   **MS/ES Toys & Bags:** Utilize more `surface-container-low` blocks to create a playful, modular "kit" look while maintaining the high-end editorial feel.