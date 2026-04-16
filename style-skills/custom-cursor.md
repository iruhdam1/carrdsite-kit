# Custom Cursor

Replaces the default browser cursor with a custom design sitewide using inline SVG.

## Requirements

- Carrd Pro Standard or higher

## Before Generating Code — Ask the User

1. Cursor style: pixel/retro arrow, crosshair, circle, custom shape, or emoji?
2. Colors?
3. Should links/buttons show a different cursor (e.g. pointer hand)?
4. Size (max recommended: 32x32px)?
5. Dark mode variant needed?

## How It Works

- CSS `cursor` property set on `*` with `!important` to override all defaults
- Cursor is an inline SVG converted to a data URI
- `shape-rendering: crispEdges` for pixel-perfect rendering on retro styles
- Separate cursor rule for `a, button` if a pointer variant is needed
- Dark mode: swap SVG data URI when `carrd-dark` class is on body

## Critical Rules

- Keep cursor CSS as the **first** stylesheet entry in the embed
- Never use `::marker` (crashes Carrd's CSS parser)
- Keep SVGs simple — complex paths affect performance
- Custom cursor overrides `grab` cursor on draggable elements, but drag functionality still works

## Code Placement

Embed → Code → Hidden → **Head** (load before render to avoid cursor flash)
