# FAQ Accordion

Creates an expandable Q&A section where clicking a question reveals the answer.

## Requirements

- Read `carrd-base.md` first
- Carrd Pro Standard or higher

## Two Approaches

### Approach A — Use Existing Carrd Elements (Recommended)

Build your questions and answers as alternating text elements inside a container, then add the class `faq` to that container. The skill code detects the structure and adds toggle behavior.

Best for: content you want to edit visually in the Carrd editor.

### Approach B — Fully Generated HTML

Provide your Q&A content and the skill generates a complete HTML FAQ block for inline embed.

Best for: more styling control, or when you want the FAQ self-contained.

## Before Generating Code — Ask the User

1. How many Q&A pairs?
2. What are the questions and answers?
3. Single open at a time, or allow multiple open simultaneously?
4. Icon style: plus/minus, chevron arrow, or none?
5. Color scheme for question bar and answer background?

## How It Works

- Answers have `max-height: 0` and `overflow: hidden` by default
- On click, `max-height` is set to `scrollHeight` via JS for smooth expand
- CSS transition handles the animation
- The icon rotates or swaps on toggle
- Event delegation on the container handles all clicks efficiently

## Code Placement

- Approach A: Embed → Code → Hidden → Body End
- Approach B: Embed → Code → Inline (at the position in your page where you want the FAQ)
