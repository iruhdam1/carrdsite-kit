# Popup Modal

Displays a centered modal with a semi-transparent backdrop. Supports multiple trigger types.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher

## Trigger Options

| Trigger | How |
|---|---|
| Button click | Add class `popup-trigger` to any Carrd element |
| Time delay | Modal appears automatically after N seconds |
| Exit intent | Modal appears when cursor moves toward browser top edge |

Multiple triggers can be combined.

## Before Generating Code — Ask the User

1. What trigger(s)? (click, timer, exit intent)
2. If timer: how many seconds?
3. What should the modal contain? (text, image, form, CTA)
4. Show once per session or every visit?
5. Color scheme and size preferences?
6. Close behavior: X button only, or also close on backdrop click / Escape key?

## How It Works

- Backdrop: `position: fixed`, full viewport, `z-index: 99990`, semi-transparent
- Modal box: centered via flexbox, `z-index: 99995`
- `overflow: hidden` added to body when open to prevent background scroll
- Close handlers: X button, optional backdrop click, optional Escape key
- Session persistence via `sessionStorage` if "once per session" is selected

## Code Placement

Embed → Code → Hidden → Body End
