# 🎨 UI & Design Guidelines — CivicAI

Design Philosophy: **Accessible & Ethical** — built for high contrast, WCAG AAA compliance, and low-cognitive load.

## 🎨 Color Palette
- `--color-navy` (`#0F172A`): Primary headings and dark mode surface.
- `--color-navy-light` (`#334155`): Secondary body text.
- `--color-cta` (`#0369A1`): Primary interactive buttons and links.
- `--color-saffron` (`#C2410C`): Darkened civic accent for high contrast on light mode.
- `--color-success` (`#15803D`): Resolved status and positive alerts.
- `--color-danger` (`#B91C1C`): Critical priority and SLA breach warnings.

## 🔤 Typography
- **Headings**: `Lexend` — designed to reduce visual stress.
- **Body**: `Source Sans 3` — highly legible at 16px minimum with 1.6 line-height.

## ♿ Accessibility Rules
- **Focus Rings**: 3px outline on `:focus-visible`.
- **Touch Targets**: 44×44px minimum for touch pointers.
- **Contrast Ratios**: All text exceeds 4.5:1 against background (7:1 for AAA).
- **Reduced Motion**: Respects `prefers-reduced-motion: reduce`.
