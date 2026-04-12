# Maths — Unit Circle Waves (HTML)

This folder contains a **single static web page**, `index.html`, that shows how **sine** and **cosine** arise from a rotating radius on the unit circle and how that motion connects to travelling waves and complex numbers.

The page is an **interactive trigonometry visualisation** linking the circle, the graphs of **sin** and **cos**, angular frequency **ω**, phase shift **φ**, and the complex-exponential form **z = r e<sup>iα</sup>**.

## What the page covers

- **Unit circle motion** — a rotating radius with horizontal and vertical projections
- **Sine and cosine graphs** — plotted against angle as the radius turns
- **Travelling wave view** — showing how sinusoidal motion becomes a moving wave
- **Angular frequency and phase** — how **ω** and **φ** affect the motion
- **Euler / complex-plane connection** — relating the rotation to **z = r e<sup>iα</sup>**
- **Multiple representations at once** — circle, graphs, and wave strip shown together

## Interactive features

- **Play / pause / step** controls for the angle animation
- **Sine / cosine visibility** controls
- **Radians / degrees** display switch for the angle axis
- **Amplitude, phase, ω, cycles, and revolutions** sliders
- **Reset** and **Start again** controls
- **Save PNG** export option
- **Optional Euler panel** and in-app help overlay

## How to view

Open `index.html` in any modern web browser. No build step or server is required, although a simple local server can help if a browser limits some `file://` behaviour.

If you later add or regenerate favicon and Apple-touch assets, keep them beside `index.html` so desktop browsers and Safari can find them correctly.

## Assets in this folder

| File | Purpose |
|------|---------|
| `index.html` | Main interactive page for unit-circle motion and wave graphs |
| `README.md` | Project summary and usage notes |
| `header-logo.svg` | Official rectangular Hal AI by CJF header logo used on the page |
| `logo.svg` | Compact square SVG favicon/icon asset |
| `favicon-32.png` | 32 × 32 PNG favicon for browsers such as Safari |
| `favicon-16.png` | 16 × 16 PNG favicon for smaller browser icon contexts |
| `apple-touch-icon.png` | **180 × 180** icon for iPhone and iPad home-screen use |

## Notes

- The page is entirely client-side HTML, CSS, canvas, SVG, and JavaScript.
- Safari tends to prefer the PNG favicon files over SVG for tab icons, which is why both PNG and SVG assets are included.
- The content is intended for educational use in trigonometry, waves, and the link to complex exponentials.

---

*Educational summary only — intended as a visual explanation of sine, cosine, rotation, and their connection to waves and complex numbers.*
