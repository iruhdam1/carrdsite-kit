# Scroll Animations

Adds entrance animations to elements as they scroll into view. Uses IntersectionObserver for performance.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher

## Available Animation Classes

Add one of these classes to any Carrd element:

| Class | Animation |
|---|---|
| `fade-in` | Fades from invisible to visible |
| `slide-up` | Slides up 40px while fading in |
| `slide-left` | Slides in from the left |
| `slide-right` | Slides in from the right |
| `scale-in` | Scales from 90% to 100% while fading in |

## Before Generating Code — Ask the User

1. Which animation types do you need?
2. Animation duration preference (default: 0.6s)?
3. Should elements animate once, or reset when scrolled out of view?
4. Stagger delay for grouped elements? (e.g. cards animating one after another)

## How It Works

- Elements start with `opacity: 0` and their transform offset
- `IntersectionObserver` fires when 15% of the element is visible
- A `.visible` class is added, triggering CSS transitions
- `will-change: opacity, transform` enables GPU acceleration
- Elements animate once by default (observer disconnects after trigger)

## Code Placement

Embed → Code → Hidden → Body End
