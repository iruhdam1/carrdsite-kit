# Dark Mode Toggle

Adds a button that switches between light and dark color schemes. Remembers the user's choice for the session.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher

## Before Generating Code — Ask the User

1. Light mode colors: background, text, container backgrounds, borders
2. Dark mode colors: same set of values
3. Toggle button position (bottom-right is default)
4. Button style: sun/moon icons, text labels ("Light / Dark"), or toggle switch?
5. Any images that should invert in dark mode?
6. Any containers to exclude from dark mode (e.g. a footer with its own color)?

## How It Works

- A fixed toggle button is injected via JS
- Clicking adds/removes the `carrd-dark` class on `<body>`
- CSS handles most color overrides via `.carrd-dark` selectors
- Container backgrounds use `setProperty()` on `.wrapper .inner` (CSS `!important` can't override Carrd inline styles — see carrd-base.md)
- `card` class on a container opts it into dark mode background changes
- `footer` class on a container excludes it from background changes
- Preference is stored in `sessionStorage`

## Code Placement

Embed → Code → Hidden → Body End
