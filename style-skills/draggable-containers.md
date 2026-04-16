# Draggable Containers

Lets visitors pick up and move containers around the page, like dragging windows on a desktop.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher

## Setup

Add the class `draggable` to any container you want users to be able to move.

## Before Generating Code — Ask the User

1. Which containers should be draggable?
2. Visual feedback during drag: shadow, border highlight, or none?
3. Should position persist after page refresh? (uses `localStorage`)
4. Any containers to exclude from dragging?

## How It Works

- Pointer Events API handles both mouse and touch (no separate handlers needed)
- `setPointerCapture()` keeps `pointermove` firing even when cursor leaves the element during fast drags
- `touch-action: none` prevents the browser from scrolling instead of dragging on mobile
- Native image dragging is disabled to prevent conflicts
- Z-index is elevated during drag so the element floats above others
- `e.stopPropagation()` prevents Carrd's handlers from interfering

## Compatibility Note

If using alongside popup-modal with `copyable-command` elements, exclude those elements from drag listeners to prevent conflicts.

## Code Placement

Embed → Code → Hidden → Body End
