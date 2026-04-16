# Back to Top Button

A floating button that appears after the user scrolls down, and smoothly returns them to the top on click. Fully code-generated — no Carrd elements needed.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher

## Before Generating Code — Ask the User

1. Scroll threshold to show the button (default: 300px)
2. Visual style: up-arrow icon, text ("↑" or "Top"), or custom SVG?
3. Position: bottom-right (default), bottom-left, or custom?
4. Color scheme (background, icon/text color)?
5. Shape: circle or rounded rectangle?

## How It Works

- Button is injected into the DOM via JavaScript
- `position: fixed; bottom: 20px; right: 20px` (or custom position)
- Z-index: 9980
- Scroll listener with `requestAnimationFrame` debounce for performance
- Opacity transition for smooth show/hide
- `window.scrollTo({ top: 0, behavior: 'smooth' })` on click

## Code Placement

Embed → Code → Hidden → Body End
