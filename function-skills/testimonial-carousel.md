# Testimonial Carousel

An auto-rotating testimonial slider that shows one quote at a time with smooth transitions. Fully code-generated.

## Requirements

- Carrd Pro Standard or higher

## Before Generating Code — Ask the User

1. What are the testimonials? (quote, name, title/company for each)
2. How many testimonials?
3. Auto-rotate speed (default: 5 seconds)?
4. Transition style: fade or slide?
5. Navigation: dots, arrows, both, or none?
6. Include avatar images? If yes, get the URLs
7. Color scheme (background, text, accent)?

## How It Works

- Testimonials are absolutely positioned, stacked
- Fade: opacity transitions between active/inactive
- Slide: `transform: translateX()` moves cards in and out
- `setInterval` handles auto-rotation; pauses on hover
- Navigation dots update `aria-current` for accessibility
- Swipe support via pointer events for mobile

## Code Placement

Embed → Code → Inline (place it at the exact position on your page where you want the carousel)
