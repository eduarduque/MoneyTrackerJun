# Money Tracker Visual Design System (Level 2)

This document serves as the absolute visual system source of truth for the Money Tracker app. All styling, layout, typography, and interactive behaviors must strictly adhere to these specifications.

---

## 🎨 Theme & Color System (Obsidian Glass)

We use a deep, premium obsidian dark theme with semi-transparent glassmorphism panels, high-contrast borders, and focused HSL light signals.

### Color Tokens (HSL)
*   **`--bg`**: `hsl(240, 10%, 4%)` - Deep pitch obsidian black (`#0a0a0c`).
*   **`--surface`**: `rgba(20, 20, 24, 0.65)` - Semi-transparent cards.
*   **`--surface-solid`**: `hsl(240, 8%, 9%)` - Opaque elements (`#141418`).
*   **`--surface-hover`**: `hsl(240, 7%, 13%)` - Hovered states (`#202026`).
*   **`--border`**: `rgba(255, 255, 255, 0.06)` - Sleek micro borders.
*   **`--border-focus`**: `rgba(255, 255, 255, 0.15)` - Active or focused inputs.
*   **`--text-primary`**: `hsl(0, 0%, 96%)` - Highly readable text (`#f4f4f5`).
*   **`--text-secondary`**: `hsl(240, 5%, 65%)` - Labels and metadata (`#a1a1aa`).
*   **`--text-muted`**: `hsl(240, 5%, 45%)` - Placeholders and disabled states (`#71717a`).

### Accent Signals
*   **`--green`**: `hsl(142, 70%, 45%)` - Income / Positive balance (`#10b981`).
*   **`--green-glow`**: `rgba(16, 185, 129, 0.12)`
*   **`--red`**: `hsl(346, 84%, 61%)` - Expense / Negative balance (`#f43f5e`).
*   **`--red-glow`**: `rgba(244, 63, 94, 0.12)`
*   **`--blue`**: `hsl(217, 91%, 60%)` - Interactive elements / Links (`#3b82f6`).
*   **`--blue-glow`**: `rgba(59, 130, 246, 0.15)`
*   **`--violet`**: `hsl(262, 83%, 64%)` - Transfers / Group headers (`#8b5cf6`).
*   **`--violet-glow`**: `rgba(139, 92, 246, 0.15)`
*   **`--amber`**: `hsl(38, 92%, 50%)` - Budget Warning / Alerts (`#f59e0b`).
*   **`--amber-glow`**: `rgba(245, 158, 11, 0.12)`

### Glassmorphism Formula
*   `background: var(--surface);`
*   `backdrop-filter: blur(16px) saturate(120%);`
*   `-webkit-backdrop-filter: blur(16px) saturate(120%);`
*   `border: 1px solid var(--border);`

---

## 📐 Layout & Dimensions

The app is built as a mobile-first application designed for single-hand thumb reach on modern screens.
*   **Max Width**: `480px` (centered horizontally using `margin: 0 auto;`).
*   **Height**: `100dvh` (uses dynamic viewport height to prevent keyboard clipping).
*   **Padding**: Standard screen gutter is `16px` (`padding: 16px`).
*   **Border Radius**:
    *   Cards & Modules: `16px` (`border-radius: 16px`).
    *   Form elements, buttons & chips: `12px`.
    *   Pills & Badges: `999px`.
*   **Safe Area Bottom**: Integrates `env(safe-area-inset-bottom, 16px)` to avoid overlapping native mobile bars.

---

## 🔠 Typography Hierarchy

We use Google Font **`Outfit`** for clean, modern geometry.

| Element | Font Weight | Size | Line Height | Case / Spacing |
| :--- | :---: | :---: | :---: | :---: |
| **Large Balance Amount** | 800 (Extra Bold) | `38px` | `1.1` | `-0.03em` |
| **Section Title** | 700 (Bold) | `18px` | `1.3` | `Normal` |
| **Card Header** | 600 (Semi-Bold) | `14px` | `1.4` | `Normal` |
| **Body Text** | 400 (Regular) | `14px` | `1.5` | `Normal` |
| **Labels / Small Caps** | 600 (Semi-Bold) | `11px` | `1.2` | `UPPERCASE / 0.08em` |
| **Subtext / Metadata** | 400 (Regular) | `12px` | `1.4` | `Normal` |

---

## 🚫 Design Anti-Patterns (Banned Styles)

To prevent generic "AI Slop" look, the following styles are strictly banned:
1.  **NO Generic Icon Outlines**: Do not use generic emoji icons in flat circles. Use custom CSS iconography or stylized typography badges.
2.  **NO Plain Solid Borders**: All borders must be either semi-transparent (`rgba`) or use a double-border effect with inset shadows to give depth.
3.  **NO Centered Call-To-Action (CTA) on Dashboard**: The default dashboard layout must be left-aligned and structured hierarchically.
4.  **NO Flat Dark Backgrounds**: Backgrounds must have a subtle radial gradient radiating from the top center to create depth:
    `background: radial-gradient(circle at top, hsl(240, 10%, 8%) 0%, hsl(240, 10%, 4%) 100%);`
5.  **NO Abrupt Page Flashing**: All tab switches and sheet drawer openings must use smooth transitions.
