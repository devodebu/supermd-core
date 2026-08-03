# design.md — UI/UX Design Guidelines

## 1. Visual identity

- **Color palette:**
  - Primary: `#______`
  - Secondary: `#______`
  - Background: `#______`
  - Error: `#______`
  - Success: `#______`
- **Typography:**
  - Family: (e.g. Inter, Roboto, Poppins)
  - Scale: Title / Subtitle / Body / Caption
- **Iconography:** (e.g. Material Symbols, Lucide, custom set)
- **Overall style:** (e.g. Material 3, minimalist, flat, neumorphic)

## 2. Design tokens

> These values must map to the project's theming/styling layer (see folder structure in `STACK.md`) — never hardcode loose values in components/widgets.

- **Base spacing:** (e.g. 4px / 8px / 16px / 24px / 32px)
- **Border radii:** (e.g. sm 4px, md 8px, lg 16px)
- **Elevations/shadows:** (define levels)
- **Dark mode:** (Yes/No — if applicable, define dark palette)

## 3. Base components

| Component | Status | Notes |
|---|---|---|
| Primary button | Placeholder | |
| Secondary button | Placeholder | |
| Text input | Placeholder | |
| Card | Placeholder | |
| Main navigation | Placeholder | |

## 4. Mockups and visual prototypes

- Location: `docs/design/` (screenshots, mockups, `.png`/`.jpg` prototypes)
- For each mockup, note which screen/feature it corresponds to.

## 5. Mandatory UI states

Every screen/view that consumes data (backend, APIs) must account for:

- [ ] Loading state (loading / shimmer)
- [ ] Empty state (no data)
- [ ] Error state (with retry option)
- [ ] Data state (happy path)

## 6. Accessibility

- Minimum color contrast: (e.g. WCAG AA)
- Scalable text sizes (support the system's/browser's accessibility settings)
- Minimum touch targets: follow the target platform's guidance (e.g. 48x48dp on Android/Material, 44x44pt on iOS/HIG, 44x44px on web/WCAG) — specify per `STACK.md`.

## 7. Consistency notes

- (Log design decisions made throughout the project here)
