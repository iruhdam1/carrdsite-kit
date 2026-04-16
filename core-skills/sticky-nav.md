# Sticky Nav

Creates a navigation bar that fixes to the top of the screen as the user scrolls down.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher (for Embed elements)
- A navigation container already built in the Carrd editor

## Setup

1. Add the class `sticky-nav` to your navigation container
2. Embed the generated code at **Body End** (Embed → Code → Hidden → Body End)

## Before Generating Code — Ask the User

1. What are the nav items and their destination anchors? (e.g. "About → #about, Pricing → #pricing")
2. What background color should the nav have when stuck? (e.g. `#ffffff`, `rgba(0,0,0,0.9)`)
3. Should there be a shadow when the nav is fixed?
4. What is the nav's position on the page — top section, or somewhere else?

## How It Works

- On scroll, `getBoundingClientRect()` detects when the nav reaches the top of the viewport
- The nav switches to `position: fixed` and `top: 0`
- Body padding is added equal to the nav height to prevent content jump
- Background is set via `setProperty()` on `.wrapper` and `.inner` (per carrd-base rules)
- Z-index is set to 9990 so it sits above content but below modals
- Smooth scroll is applied to all anchor links inside the nav

## Compatibility

Works alongside: mobile-menu, scroll-animations, popup-modal, dark-mode-toggle

## Code Placement

Embed → Code → Hidden → Body End
