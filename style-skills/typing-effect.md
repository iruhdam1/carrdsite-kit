# Typing Effect

Animates text with a typewriter effect — types characters one by one, pauses, then deletes and cycles to the next phrase.

## Requirements

- Carrd Pro Standard or higher

## Two Approaches

### Approach A — Target an Existing Element

Add the class `typing` to any Carrd text element. The script replaces its content with the animation.

### Approach B — Generate a New Element

The script creates the element entirely. Embed it inline at the desired position.

## Before Generating Code — Ask the User

1. What phrases should cycle? (list all of them)
2. Is there static text before the animated part? (e.g. "I help you [typing effect here]")
3. Approach A or B?
4. Typing speed (default: 80ms/character), delete speed (default: 40ms/character), pause duration (default: 2s)?
5. Cursor style: blinking `|`, `_`, or none?
6. Font and color?

## How It Works

- `setTimeout` chains control character-by-character timing
- Text is written via `textContent` (never `innerHTML`) for security
- A CSS `@keyframes` animation creates the cursor blink
- Phrases loop infinitely

## Code Placement

- Approach A: Embed → Code → Hidden → Body End
- Approach B: Embed → Code → Inline
