# Carrd Base Knowledge

Read this before writing any custom code for a Carrd site. These rules prevent the most common mistakes.

## DOM Structure

Carrd renders pages with this hierarchy:

```
.site-wrapper
  .site-main
    .inner
      [sections: containers, images, text, lists, etc.]
```

Each section type has predictable class names. Containers are the primary grouping element.

## The Wrapper/Inner Rule

Carrd containers have this structure:

```
.container-component
  .wrapper
    .inner
      [content]
```

Setting `background` on `.container-component` alone does nothing visually. You must target `.wrapper` and `.inner` inside it. Always use JavaScript's `setProperty()` for container backgrounds — CSS `!important` cannot override Carrd's inline styles.

```js
el.querySelector('.wrapper').style.setProperty('background', '#fff', 'important');
el.querySelector('.inner').style.setProperty('background', '#fff', 'important');
```

## Style Priority (Highest to Lowest)

1. JavaScript `setProperty()` with `'important'`
2. Inline HTML style attributes
3. CSS `!important`
4. Regular CSS

## Forbidden CSS

- **Never use `::marker`** — it crashes Carrd's CSS parser and breaks the entire page
- Avoid complex `:not()` chains

Safe alternatives: `::before`, `::after`, standard pseudo-classes, media queries, CSS variables.

## Embed Placement

- Use **Body End** for all JavaScript — this ensures the DOM exists before your code runs
- Wrap JS in `setTimeout(() => { ... }, 100)` for extra safety on slow loads
- Use **Head** only for CSS-only embeds (custom cursor, fonts)
- Use **Inline** when you need to place content at a specific page position

## Custom Classes

Users add custom classes via the element's gear icon → Advanced → Classes. These are the primary targeting mechanism. Design skills around well-named classes (e.g. `sticky-nav`, `faq`, `draggable`).

## Z-Index Hierarchy

Reserve these ranges to avoid conflicts:

| Layer | Z-index |
|---|---|
| Modals / overlays | 99990+ |
| Sticky navigation | 9990+ |
| Tooltips | 9000+ |
| Floating buttons | 9980 |

## Event Handling

Always include `e.stopPropagation()` to prevent Carrd's native handlers from interfering with custom interactions.

## List Number Styling

Carrd lists use `::before` pseudo-elements for numbering — not standard `ol > li` markup. Never use `::marker`.

## Pointer Events for Drag/Touch

Use the Pointer Events API with `setPointerCapture()` and `touch-action: none`. Add listeners in the capture phase. This handles both mouse and touch reliably across devices.
