# Design System Specification: Fast Forms Design Bootcamp

## 1. Overview & Creative North Star: "The Modern Academy"
The Creative North Star for this design system is **The Modern Academy**.

We are moving away from the "standard educational portal" look—which often feels rigid, cold, and tabular—toward an editorial, high-energy experience. This system balances the prestige of a traditional institution with the kinetic energy of a fast-paced bootcamp.

To achieve this, we employ **Intentional Asymmetry**. Instead of a perfectly centered grid, we use oversized typography (Display scales) paired with generous negative space to create a "Signature Editorial" feel. Layouts should feel curated, not templated. Overlapping elements (e.g., a card bleeding into a background gradient) are encouraged to break the box-model monotony and suggest movement and progress.

---

## 2. Colors & Tonal Architecture
The palette is a sophisticated evolution of the brand's orange and navy heritage, designed for digital depth rather than flat print.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections or containers. Structure must be achieved through **Background Color Shifts** or **Tonal Transitions**.
- A section sitting on `surface` should transition to `surface-container-low` to define its boundary.
- Use the `outline-variant` (#e3bfb1) at 15% opacity only if a "Ghost Border" is strictly required for accessibility.

### Surface Hierarchy & Layering
Treat the interface as a physical stack of premium materials.
- **Base Layer:** `surface` (#fff8f6) – The canvas.
- **Content Blocks:** `surface-container` (#ffe9e1) – For primary content sections.
- **Elevated Cards:** `surface-container-lowest` (#ffffff) – Used to "lift" key information off a tinted background.

### Signature Textures: Glass & Gradients
To provide "soul" to the professional aesthetic:
- **The Kinetic Gradient:** Use a linear gradient from `primary` (`#A33E00`) to `primary_container` (#ff6600) at 135 degrees for Hero CTAs and high-impact headers.
- **Glassmorphism:** For floating navigation or overlays, use `surface` at 80% opacity with a `24px` backdrop-blur. This ensures the vibrant orange energy bleeds through the interface without sacrificing legibility.

---

## 3. Typography: The Editorial Voice
We use a dual-font pairing to balance academic authority with modern tech-readiness.

*   **Headlines (Plus Jakarta Sans):** A contemporary sans-serif with geometric leanings. Used for `display` and `headline` scales. Its wide apertures feel welcoming yet professional.
*   **Body & Utility (Manrope):** A highly legible, modern grotesque. Used for `title`, `body`, and `label` scales. Its technical precision ensures "Fast Forms" instructions are crystal clear.

### The Hierarchy Strategy
- **Aggressive Scale:** Use `display-lg` (3.5rem) for hero sections to create an immediate "High-End" impact.
- **Tight Leading:** For headlines, keep line heights tight (1.1–1.2) to maintain a dense, authoritative "newspaper" feel.
- **Micro-Copy:** All labels use `label-md` in `on_surface_variant` (#5a4136) to provide a sophisticated, muted contrast against the bold brand colors.

---

## 4. Elevation & Depth
Depth is achieved through **Tonal Layering**, not shadows.

*   **Layering Principle:** Place a `surface-container-lowest` card (Pure White) on a `surface-container-low` section. The contrast in "warmth" creates a natural lift.
*   **Ambient Shadows:** Where floating elements are required (e.g., Modals), use a "Tinted Glow":
    *   `box-shadow: 0 20px 40px rgba(86, 29, 0, 0.08);` (A subtle shadow tinted with the `on_primary_container` hue).
*   **Glass Depth:** Use semi-transparent layers for sub-navigation. This prevents the UI from feeling like a series of "stacked boxes" and instead creates an integrated, fluid environment.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary_container`), `xl` rounded corners (1.5rem). Use `headline-sm` for text to maintain energy.
- **Secondary:** `secondary_container` (#9fc2fe) background with `on_secondary_container` (#294f83) text. No border.
- **Interaction:** On hover, apply a `2px` upward shift and increase shadow diffusion.

### Input Fields & Forms
- **The Container:** Use `surface_container_highest` (#f8ddd2) for the input track.
- **The Focus State:** Instead of a border change, use a `2px` solid `primary` (`#A33E00`) bottom-bar and a subtle background glow.
- **Labels:** Always use `label-md` floating above the field to maintain the "Fast" in Fast Forms.

### Cards & Lists
- **Rule:** Absolute prohibition of divider lines.
- **Separation:** Use `md` (0.75rem) or `lg` (1rem) spacing scale increments to separate list items.
- **Highlighting:** Use a `surface_variant` (#f8ddd2) background on hover for list items to indicate interactivity.

### Progress Indicators (Bootcamp Specific)
- **The Track:** A thick, `lg` (1rem) rounded bar using `surface_container_high`.
- **The Fill:** A vibrant `primary` (`#A33E00`) fill with a subtle "shimmer" animation to denote energy and momentum.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical margins. If the left margin is 80px, try a right margin of 120px for editorial sections.
*   **Do** use `primary` (`#A33E00`) for "Actionable" elements and `secondary` (`#3A5F94`) for "Information" elements.
*   **Do** embrace white space. If a section feels "crowded," double the padding.

### Don’t
*   **Don’t** use 100% black (#000000) for text. Use `on_surface` (#261812) for a warmer, premium feel.
*   **Don’t** use standard `0.5rem` gaps. Move between `0.75rem` (md) and `1.5rem` (xl) to create a rhythm of "tension and release."
*   **Don’t** use sharp 0px corners. Even the most "academic" element should have at least a `sm` (0.25rem) radius to feel modern.

---

## 7. Spacing Scale
Maintain a strict 8pt grid, but prioritize these tokens for the "Editorial" layout:
- **Tight (sm):** 0.25rem (4px)
- **Standard (md):** 0.75rem (12px)
- **High-Impact (xl):** 1.5rem (24px)
- **Section Break:** 4rem (64px) to 8rem (128px)