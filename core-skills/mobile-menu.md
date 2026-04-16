# Mobile Menu

Collapses your navigation into a hamburger menu on small screens.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher
- A navigation container already built in the Carrd editor

## Setup

Embed the generated code at **Body End** (Embed → Code → Hidden → Body End). No additional classes needed — the code targets your nav by position or class.

## Before Generating Code — Ask the User

1. What nav items and destinations should be in the mobile menu?
2. At what screen width should the hamburger appear? (default: 768px)
3. Animation style: slide down from top, slide in from side, or fade?
4. Color scheme: hamburger icon color, menu background, link color?
5. Should clicking a link auto-close the menu?

## How It Works

- CSS media queries hide the desktop nav below the breakpoint
- A hamburger button is injected via JavaScript (3 lines or animated X)
- Clicking the button toggles a full-width overlay menu
- `overflow: hidden` is added to the body while the menu is open
- Menu links smooth-scroll to sections and close the menu
- Z-index: 9995 (above content, below modals)

## Compatibility

Works alongside sticky-nav — if both are active, the hamburger button inherits the sticky nav's fixed position.

## Code Placement

Embed → Code → Hidden → Body End
