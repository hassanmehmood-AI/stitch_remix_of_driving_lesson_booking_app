# Design System Specification: Editorial Trust & Motion

## 1. Overview & Creative North Star
**Creative North Star: "The Guided Precision"**

This design system moves away from the "utility-first" look of standard booking apps toward a high-end, editorial experience. It balances the authoritative weight of a premium driving institution with the fluid, effortless motion of a modern tech startup. 

To break the "template" feel, this system employs **Intentional Asymmetry**. Rather than perfectly centered grids, we use weighted typography and overlapping surface layers to create a sense of forward momentum. We treat the interface not as a set of screens, but as a series of choreographed movements—mimicking the focus and flow required behind the wheel.

---

## 2. Colors: Tonal Depth & Soul
We use a sophisticated palette where "Deep Blue" provides the structural foundation and "Trust Green" acts as the pulse of progress.

### Core Palette
- **Primary (Authority):** `#001e40` (Primary) to `#003366` (Primary Container). Use these for high-density branding and deep-immersion headers.
- **Secondary (Progress):** `#1b6d24` (Secondary). Reserved for "Success" states and verified instructor badges.
- **Tertiary (Action):** `#311700` (Tertiary) with `#e78100` (On-Tertiary Container). This vibrant amber is our "Engine Start" color—reserved exclusively for critical CTA paths.

### The "No-Line" Rule
**Borders are prohibited for sectioning.** To define boundaries, use tonal shifts between `surface`, `surface-container-low`, and `surface-container-highest`. A card should never have a 1px stroke; it should exist because its background color is a `surface-container-lowest` (#FFFFFF) sitting on a `surface` (#F9F9F9) floor.

### The "Glass & Gradient" Rule
To add "soul" to the digital experience:
- **Signature Gradients:** Primary buttons should use a subtle linear gradient from `primary` to `primary_container` (150° angle) to prevent a flat, "cheap" digital look.
- **Glassmorphism:** Navigation bars and floating action cards must use a 20% opacity `surface` fill with a `backdrop-blur` (20px-30px). This ensures the "road" (the content below) is always partially visible, maintaining a sense of speed and transparency.

---

## 3. Typography: The Editorial Scale
We pair **Manrope** (Display/Headline) for its geometric, modern personality with **Inter** (Title/Body) for its unmatched legibility at high speeds.

- **Display (The Statement):** `display-lg` (3.5rem) should be used for milestone numbers (e.g., "12 Lessons Completed"). Set with tight letter spacing (-0.02em).
- **Headlines (The Narrative):** `headline-md` (1.75rem) in Manrope Semi-Bold. Use these to frame the user's journey.
- **Body (The Data):** `body-md` (0.875rem) in Inter. High-contrast (`on-surface`) for instructions; low-contrast (`on-surface-variant`) for metadata.
- **The Hierarchy Rule:** Never use two different font sizes of the same weight in immediate proximity. Create "Visual Breathing Room" by pairing a `headline-sm` with a `label-md` in all-caps for a premium, tagged look.

---

## 4. Elevation & Depth: Tonal Layering
Instead of traditional drop shadows which can feel "muddy," we use the **Layering Principle**.

- **Surface Nesting:** 
    - Floor: `surface` (#F9F9F9)
    - Section: `surface-container-low` (#F3F3F3)
    - Interactive Card: `surface-container-lowest` (#FFFFFF)
- **Ambient Shadows:** For floating elements (like a "Book Now" bar), use a shadow color tinted with the primary hue: `rgba(0, 30, 64, 0.06)` with a 40px blur and 12px Y-offset.
- **Ghost Borders:** If an element requires more definition (e.g., a disabled input), use `outline-variant` at 15% opacity. Never use pure black or grey strokes.

---

## 5. Components: Primitive Definitions

### Buttons: The "Ignition" Set
- **Primary:** `xl` (1.5rem) corner radius. Background: Tertiary (Amber/Orange). Label: `title-sm` Bold. High-gloss finish using a subtle top-down gradient.
- **Secondary:** Transparent background with a `Ghost Border` and `primary` text.
- **States:** On press, scale the component down to 97% to provide haptic visual feedback.

### Cards: The "Informational Pods"
- **Strict Rule:** No dividers. Separate content using `body-sm` labels as headers and 24px of vertical whitespace.
- **Layout:** Use asymmetric padding—more padding at the bottom than the top (e.g., T:24px, B:32px) to give an editorial, "weighted" feel.

### Input Fields: "Quiet Inputs"
- Minimalist design: No background fill. Only a bottom "Ghost Border" that transforms into a 2px `primary` line on focus.
- Labels: Always visible, using `label-md` positioned 8px above the input line.

### Specialty Component: The Progress Orbit
- For driving progress, use a large-scale circular track using `secondary_container` as the base and `secondary` as the active stroke. Place `display-md` typography in the center.

---

## 6. Do’s and Don’ts

### Do:
- **Do** use whitespace as a functional tool. If in doubt, increase the margin.
- **Do** use "Trust Green" for all success states and instructor verification icons to build psychological safety.
- **Do** lean into `xl` (1.5rem) border radiuses for large containers to maintain a "friendly high-end" vibe.

### Don’t:
- **Don’t** use 1px solid dividers. Use 8px of `surface-container-low` as a "gutter" instead.
- **Don’t** use standard blue for links. Use `primary` (Deep Blue) with a semi-bold weight and no underline.
- **Don’t** crowd the screen. This system is designed to be consumed "at a glance"—one primary thought per screen.

---

## 7. Roundedness Scale
- **Small (sm):** `0.25rem` (Selection indicators)
- **Default:** `0.5rem` (Input fields)
- **Large (lg):** `1rem` (Standard Cards)
- **Extra Large (xl):** `1.5rem` (Main Hero Containers / CTAs)
- **Full:** `9999px` (Status Pills / Chips)