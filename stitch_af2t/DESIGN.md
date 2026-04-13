```markdown
# Design System Document: AF2T Global Logistics

## 1. Overview & Creative North Star
### Creative North Star: "The Architectural Flow"
Logistics is often viewed as a rigid, industrial process. This design system reimagines AF2T’s digital presence as "The Architectural Flow"—a sophisticated, editorial-grade interface that mirrors the precision of global transit through intentional white space, layered depth, and authoritative typography. 

Instead of common "boxed" layouts, we use **Asymmetric Tonal Layering**. Elements are not just placed on a grid; they are curated. We break the template-feel by allowing key imagery (vessels, aircraft, cargo) to overlap container boundaries, creating a sense of movement and momentum. The design shifts from a LTR (French) to RTL (Arabic) environment by mirroring the structural flow, ensuring that the "momentum" of the brand is preserved across both linguistic contexts.

---

## 2. Colors
The palette is rooted in a command-and-control **Deep Navy** (`primary_container: #002366`) and balanced by a high-energy **Vibrant Orange** (`on_tertiary_container: #f36100`).

### The "No-Line" Rule
To maintain a high-end editorial feel, **1px solid borders are prohibited for sectioning.** Boundaries must be established through color-blocking and background shifts. 
- Use `surface` (#faf8ff) for the main canvas.
- Use `surface_container_low` (#f4f3f9) for secondary content sections.
- Use `surface_container_highest` (#e3e2e8) to define active or highlighted regions.

### Surface Hierarchy & Nesting
Treat the UI as stacked layers. An information card (`surface_container_lowest: #ffffff`) should sit on a `surface_container_low` background. This "nesting" creates an intuitive hierarchy of importance without the visual clutter of lines.

### Signature Textures & Glassmorphism
- **Glassmorphism:** Use for floating navigation bars or mobile menus. Apply `surface` at 80% opacity with a 20px backdrop-blur.
- **Tonal Gradients:** For Hero sections, use a subtle linear gradient from `primary` (#00113a) to `primary_container` (#002366) at a 135-degree angle to add "soul" and depth to the navy brand color.

---

## 3. Typography
We utilize a dual-typeface system to balance authority with utility.

*   **Display & Headlines (Manrope):** Chosen for its geometric precision and modern "tech-forward" terminals. These are used to convey the brand’s power and scale.
*   **Body & Labels (Inter):** Highly legible at small scales, especially critical for logistics tracking data and bilingual (Latin/Arabic) alignment.

**The Hierarchy of Intent:**
- **Display-LG (3.5rem):** High-impact hero statements. Tight letter-spacing (-0.02em).
- **Headline-MD (1.75rem):** Section headers. Direct and confident.
- **Body-MD (0.875rem):** The workhorse for cargo details and descriptions.
- **Label-MD (0.75rem):** All-caps for status indicators (e.g., "IN TRANSIT"), tracked with +0.05em for a premium feel.

---

## 4. Elevation & Depth
In "The Architectural Flow," depth is a functional tool, not an ornament.

*   **Tonal Layering:** Avoid shadows for static content. Rely on the transition from `surface_dim` to `surface_bright` to indicate elevation.
*   **Ambient Shadows:** For interactive cards or modals, use a custom shadow: `0px 24px 48px -12px rgba(0, 17, 58, 0.08)`. Note the use of a Navy tint (`primary`) instead of black to keep the shadow feeling natural and integrated.
*   **The Ghost Border:** If a border is required for accessibility in input fields, use `outline_variant` at 20% opacity. Never use 100% opacity borders.
*   **Bilingual Flow:** Ensure shadows and blurs are symmetrical so they don't feel "off-balance" when the layout flips from French to Arabic.

---

## 5. Components

### Buttons (High-Precision CTAs)
- **Primary:** `primary_container` background with `on_primary` text. Radius: `md` (0.375rem). Transition: Subtle scale up (1.02x) on hover.
- **Tertiary (Accent):** `tertiary_container` (#4b1800) with `on_tertiary_fixed` (#360f00) text for high-priority calls to action like "Emergency Transit."

### Tracking Input Fields
- **Style:** Clean, `surface_container_highest` background. No border. 
- **States:** On focus, transition the background to `surface_container_lowest` and apply a `ghost border` using the `primary` token at 30% opacity.

### Logistics Cards
- **Construction:** Use `surface_container_lowest` (#ffffff). 
- **Rule:** **No Divider Lines.** Separate the "Origin" and "Destination" data points using `body-sm` typography and a vertical spacing of 1.5rem. Use a `secondary_container` (#d4dcfd) chip for the status.

### Bilingual Switcher
- A glassmorphic pill (`full` roundedness) located in the top-right (LTR) or top-left (RTL). High contrast `on_surface` text.

---

## 6. Do's and Don'ts

### Do:
- **Do** use intentional white space. If a section feels crowded, double the padding rather than adding a divider.
- **Do** align the Arabic text with the same optical weight as the French text. Adjust line-height (leading) for Arabic to prevent descender clipping.
- **Do** use the `Vibrant Orange` sparingly. It is a "signal" color for actions and highlights, not a background color.

### Don't:
- **Don't** use pure black (#000000) for text. Use `on_surface` (#1a1b20) to maintain a premium, softer contrast.
- **Don't** use standard "Drop Shadows." Only use the Ambient Shadow spec defined in Section 4.
- **Don't** use the `DEFAULT` roundedness for large containers; use `xl` (0.75rem) to soften the industrial nature of the brand.
- **Don't** use dividers in lists. Use background tonal shifts between `surface_container_low` and `surface_container_lowest` to distinguish items.

---
*Document produced for AF2T Junior Design Teams. Refer to Figma Variables for token mapping.*```