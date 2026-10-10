# Portfolio-assignment-1-WSP
## GUI / Interface

### Responsive design (fluid design and media queries)
The site uses fluid design: widths are percentages (and `max-width`), not fixed pixels,
so content stretches and shrinks with the screen. Images and the video scale with their
container. No Flexbox or Grid is used anywhere. The nav links and projects are laid out
with `display: inline-block` and `float`.

There are three separate CSS files, linked in every page with media queries:

| File | Viewport | Why this size |
|---|---|---|
| `css/mobile.css` | Base styles, all screens. Designed for phones about 320px to 767px wide. | Most phones are 360px to 430px wide. This is the default, so any screen gets a working layout. |
| `css/tablet.css` | 768px and up | 768px is the width of an iPad in portrait, the common starting point for tablets. |
| `css/laptop.css` | 1024px and up | 1024px is a small laptop or a tablet in landscape. |

`tablet.css` and `laptop.css` only add or change rules on top of `mobile.css`.

### Gradients
- **Linear gradient (top to bottom):** the `<header>` background on all four pages,
  `linear-gradient(var(--dark), var(--mid))`, in `css/mobile.css`.
- **Angled linear gradient (45 degrees):** the `<footer>` background on all four pages,
  `linear-gradient(45deg, var(--dark), var(--mid))`, in `css/mobile.css`.

### Color scheme
I created the palette at Adobe Color: https://new.express.adobe.com/id/urn:aaid:sc:CAN5:5028cce1-a74d-5d3e-ad57-1416001fd558?accept=true&invite=true&promoid=Z2G1FQKR&mv=other .

| Color | Hex | Used for |
|---|---|---|
| Dark purple | `#533592` | text, header and footer gradients, buttons |
| Medium purple | `#7667b3` | gradients, borders, shadows |
| Soft lavender | `#c7b9d7` | video border, nav hover |
| Pink accent | `#da5399` | project card border, focus outlines |
| Light background | `#F1FAEE` | page background |

The colors are stored as CSS variables at the top of `mobile.css`, so every page
uses the same scheme.