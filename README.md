# carrdsite-kit

A collection of Claude skills for building custom components on [Carrd](https://try.carrd.co/xperian) sites — no coding experience needed.

Tell Claude what you want. Get code to paste directly into Carrd's Embed element.

---

## Requirements

- **[Carrd Pro Standard](https://try.carrd.co/xperian)** or higher (for Embed elements)
- A [Claude](https://claude.ai) account

---

## Installation

### Step 1 — Install Core Skills

In a new Claude chat, run:

```
/skill-creator make all these skills for me https://github.com/iruhdam1/carrdsite-kit/tree/main/core-skills
```

### Step 2 — Install Function Skills (optional)

```
/skill-creator make all these skills for me https://github.com/iruhdam1/carrdsite-kit/tree/main/function-skills
```

### Step 3 — Install Style Skills (optional)

```
/skill-creator make all these skills for me https://github.com/iruhdam1/carrdsite-kit/tree/main/style-skills
```

---

## Usage

After installing, just describe what you want:

> "I need a sticky nav with links to #about, #work, and #contact. White background when fixed, with a subtle shadow."

> "Add a FAQ accordion with 5 questions. One open at a time, chevron icon, dark background."

> "Give me a back-to-top button, circle shape, bottom-right, my brand color is #6c47ff."

Claude will generate code ready to paste into **Carrd → Embed → Code**.

---

## Skills

### Core Skills

| Skill | What it does |
|---|---|
| `carrd-base` | Essential rules for writing Carrd-compatible code |
| `carrd-classes-reference` | Quick lookup for all custom classes |
| `sticky-nav` | Navigation bar that fixes to top on scroll |
| `mobile-menu` | Hamburger menu for small screens |

### Function Skills

| Skill | What it does |
|---|---|
| `faq-accordion` | Expandable Q&A sections |
| `popup-modal` | Modal with click, timer, or exit-intent triggers |
| `back-to-top` | Floating scroll-to-top button |
| `testimonial-carousel` | Auto-rotating testimonial slider |

### Style Skills

| Skill | What it does |
|---|---|
| `scroll-animations` | Entrance animations triggered by scroll |
| `typing-effect` | Typewriter text animation |
| `dark-mode-toggle` | Light/dark theme switcher |
| `custom-cursor` | Replace the default cursor with a custom design |
| `draggable-containers` | Let visitors move containers around the page |

---

## How to Add a Class

Some skills require adding a class to a Carrd element:

1. Click the element in the editor
2. Click the gear icon ⚙️
3. Go to **Advanced → Classes**
4. Click **Add class** and type the class name

---

## Contributing

Pull requests welcome. Each skill is a single `.md` file — easy to add, fork, or remix.
