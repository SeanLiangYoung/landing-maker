---
name: ui-ux-pro-max
description: UI/UX design intelligence for professional interfaces. 67 styles, 96 palettes, 57 font pairings, 99 UX guidelines. Use when designing, building, or reviewing UI/UX for landing pages, dashboards, SaaS, e-commerce. Covers accessibility, typography, color, layout, animation, pre-delivery checklist.
---

# UI/UX Pro Max - Design Intelligence

Comprehensive design guide for web and mobile applications. Contains 67 UI styles, 96 color palettes, 57 font pairings, 99 UX guidelines. Provides industry-specific recommendations and anti-patterns.

## When to Apply

- Designing new UI components or pages
- Choosing color palettes and typography
- Reviewing code for UX issues
- Building landing pages or dashboards
- Implementing accessibility requirements

## Rule Categories by Priority

| Priority | Category | Impact |
|----------|----------|--------|
| 1 | Accessibility | CRITICAL |
| 2 | Touch & Interaction | CRITICAL |
| 3 | Performance | HIGH |
| 4 | Layout & Responsive | HIGH |
| 5 | Typography & Color | MEDIUM |
| 6 | Animation | MEDIUM |
| 7 | Style Selection | MEDIUM |

## Accessibility (CRITICAL)

- `color-contrast` - Minimum 4.5:1 ratio for normal text
- `focus-states` - Visible focus rings on interactive elements
- `alt-text` - Descriptive alt text for meaningful images
- `aria-labels` - aria-label for icon-only buttons
- `keyboard-nav` - Tab order matches visual order
- `form-labels` - Use label with for attribute

## Touch & Interaction (CRITICAL)

- `touch-target-size` - Minimum 44x44px touch targets
- `cursor-pointer` - Add cursor-pointer to all clickable elements
- `hover-vs-tap` - Use click/tap for primary interactions
- `loading-buttons` - Disable button during async operations
- `error-feedback` - Clear error messages near problem

## Pre-Delivery Checklist

### Visual Quality
- [ ] No emojis used as icons (use SVG: Heroicons/Lucide)
- [ ] All icons from consistent icon set
- [ ] Hover states don't cause layout shift
- [ ] Use theme colors directly

### Interaction
- [ ] All clickable elements have `cursor-pointer`
- [ ] Hover states provide clear visual feedback
- [ ] Transitions are smooth (150-300ms)
- [ ] Focus states visible for keyboard navigation

### Light/Dark Mode
- [ ] Light mode text has sufficient contrast (4.5:1 minimum)
- [ ] Glass/transparent elements visible in light mode
- [ ] Borders visible in both modes

### Layout
- [ ] Floating elements have proper spacing from edges
- [ ] No content hidden behind fixed navbars
- [ ] Responsive at 375px, 768px, 1024px, 1440px
- [ ] No horizontal scroll on mobile

### Accessibility
- [ ] All images have alt text
- [ ] Form inputs have labels
- [ ] Color is not the only indicator
- [ ] `prefers-reduced-motion` respected

## Common Anti-Patterns to Avoid

| Rule | Do | Don't |
|------|----|----- |
| **No emoji icons** | Use SVG icons (Heroicons, Lucide) | Use emojis as UI icons |
| **Cursor pointer** | Add `cursor-pointer` to clickable cards | Leave default cursor on interactive elements |
| **Hover feedback** | Visual feedback (color, shadow, border) | No indication element is interactive |
| **Smooth transitions** | `transition-colors duration-200` | Instant or too slow (>500ms) |
| **Text contrast** | Use `#0F172A` (slate-900) for text | Use `#94A3B8` for body text |
| **Floating navbar** | Add `top-4 left-4 right-4` spacing | Stick navbar to `top-0` |

## Industry-Specific Notes

- **SaaS/B2B**: Clean, professional, trust-focused. Soft UI, Hero-Centric or Feature-Rich patterns.
- **Beauty/Wellness**: Calming palettes, organic shapes, premium feel. Soft shadows, gentle transitions.
- **Fintech**: Trust, security. Avoid AI purple/pink gradients. Accessible contrast.
- **E-commerce**: Conversion-optimized, social proof. Clear CTAs above fold.
