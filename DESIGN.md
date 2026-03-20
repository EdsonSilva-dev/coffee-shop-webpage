# Design System Document: The Dublin Editorial Cafe

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Public House"**

This design system moves away from the sterile, "tech-first" coffee apps of the past decade. Instead, it draws inspiration from the tactile nature of a Dublin cafe: the heavy weight of a ceramic mug, the gold-leaf lettering on a storefront window, and the cozy overlap of a rainy afternoon. 

The experience is defined by **Editorial Asymmetry**. We break the rigid, centered grid by using intentional whitespace and overlapping elements (e.g., a high-resolution image of a pour-over coffee slightly bleeding into a cream-colored text block). By utilizing a sophisticated scale of rich browns and "Dublin Green," the UI feels like a curated lifestyle magazine rather than a transactional tool.

---

## 2. Colors & Surface Philosophy
The palette is a dialogue between deep roasts and steamed milk, punctuated by the heritage of a Dublin moss green.

### Surface Hierarchy & The "No-Line" Rule
To achieve a premium feel, **1px solid borders are strictly prohibited for sectioning.** Boundaries must be created through background shifts.
- **Layer 0 (Base):** Use `surface` (`#fdf9f4`) for the main canvas.
- **Layer 1 (Nesting):** For featured content or cards, use `surface-container-low` (`#f7f3ee`) to create a subtle, soft-edged "pocket" of content.
- **The "Glass & Gradient" Rule:** For floating headers or navigation bars, use a backdrop-blur (12px–20px) on `surface` at 85% opacity. For CTAs, apply a subtle linear gradient from `primary` (`#33210d`) to `primary-container` (`#4b3621`) to add "soul" and depth.

### Color Tokens
- **Primary (The Roast):** `primary` (`#33210d`) – Use for high-impact text and primary actions.
- **Secondary (Dublin Green):** `secondary` (`#316948`) – Reserved for "Open" status indicators, success states, or premium loyalty features.
- **Tertiary (Brass Accents):** `tertiary` (`#322200`) – Use for iconography and subtle highlights to evoke the feel of brass railings and light fixtures.
- **On-Surface:** `on-surface` (`#1c1c19`) – A soft charcoal, never pure black, to keep the reading experience "cozy."

---

## 3. Typography
We use a high-contrast pairing to balance Dublin's historical "Old World" charm with modern efficiency.

- **Display & Headlines (Noto Serif):** This is our "Classic Cafe" voice. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero sections. Headlines should feel authoritative yet warm.
- **Body & Labels (Manrope):** A clean, geometric sans-serif that provides a "Modern" counterpoint. Use `body-lg` (1rem) for descriptions to ensure high legibility against creamy backgrounds.
- **Hierarchy Tip:** Use `label-md` (`manrope`) in all-caps with increased letter-spacing (0.05em) for category headers (e.g., "SEASONAL ROASTS") to create an editorial, "menu-style" feel.

---

## 4. Elevation & Depth
In this system, depth is organic, not artificial. We mimic the way light hits a textured paper menu.

- **The Layering Principle:** Stack `surface-container-lowest` cards on top of `surface-container` sections. This creates a "lift" through tonal contrast rather than shadows.
- **Ambient Shadows:** Shadows should only be used for elements that physically move over the interface (e.g., Modals, Floating Action Buttons). Use a 32px blur, 8% opacity, with the shadow color tinted by `on-surface` (#1c1c19).
- **The Ghost Border:** If a form input requires a boundary, use `outline-variant` (`#d2c4ba`) at 20% opacity. It should be felt, not seen.
- **Roundedness:** Use the `xl` (0.75rem) radius for cards and `full` for buttons. Avoid sharp `none` or `sm` corners to maintain the "warm and inviting" brand promise.

---

## 5. Components

### Buttons
- **Primary:** `primary` background with `on-primary` text. Use a `full` (9999px) pill shape.
- **Secondary:** No background. Use a `ghost-border` (20% opacity `outline-variant`) with `primary` text. 
- **Interaction:** On hover, shift background from `primary` to `primary-container`.

### Cards & Lists
- **The "No-Divider" Rule:** Never use horizontal lines to separate list items. Use `spacing-6` (2rem) of vertical whitespace or alternating background tones (`surface` to `surface-container-low`).
- **Cards:** Use `surface-container-highest` for a subtle hover state to indicate interactivity.

### Inputs & Selection
- **Text Fields:** Use a "Minimalist Tray" style—only a bottom border (using `outline-variant` at 40%) that thickens to 2px `primary` on focus.
- **Chips:** For coffee types (e.g., "Espresso," "Filter"), use `surface-container-high` with `on-surface-variant` text. Roundedness: `md`.

### Unique Component: The "Brass" Indicator
- Use a small `tertiary` (`#322200`) circle or underline to indicate the "Current Selection" in navigation, mimicking a brass marker.

---

## 6. Do's and Don'ts

### Do
- **Do** use asymmetrical layouts (e.g., an image aligned to the left grid, with text offset to the right).
- **Do** use `surface-dim` for empty states to create a "closed for the evening" moody vibe.
- **Do** leverage the `secondary` (Dublin Green) sparingly as a "reward" color for loyalty milestones.

### Don't
- **Don't** use pure white (`#ffffff`) for backgrounds; it breaks the "cozy" atmosphere. Always stick to the `surface` cream.
- **Don't** use standard Material shadows. They are too "software-like" for a boutique cafe brand.
- **Don't** use 1px dividers. If you feel the need to separate, increase your spacing token (use `8` or `10`).

---

## 7. Spacing Scale
The spacing scale is generous to allow the "Editorial" feel to breathe.
- **Macro-spacing:** Use `16` (5.5rem) or `20` (7rem) between major sections to emphasize a premium, unhurried experience.
- **Micro-spacing:** Use `3` (1rem) for internal card padding to keep content tight and legible.