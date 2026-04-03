# Sine & cosine from the unit circle

A self-contained web page that animates how sine and cosine arise from a radius rotating on a circle, and how angle and angular frequency relate over time.

## How to run

Open `index.html` in a modern desktop browser (Chrome, Edge, Firefox, Safari). No build step or server is required. If your browser blocks downloads when using `file://`, use a simple local server or open the file from disk as your environment allows.

## Icon and logo

- **`logo.svg`** — Vector logo in the page header; also listed as an SVG favicon for browsers that support it.
- **`favicon-32.png`** / **`favicon-16.png`** — PNG favicons used first in `index.html` because **Safari often does not use SVG for the tab icon** (it may show “?”), especially with `file://` URLs.
- **`apple-touch-icon.png`** — 180×180 PNG for **Safari** and iOS when the page is added to the **Home Screen** or **Dock** (`rel="apple-touch-icon"`).

Keep these files next to `index.html`. If the tab icon stays wrong after changes, clear the cache or close and reopen the tab.

## What it shows

1. **Unit circle (complex plane)**  
   A radius of length **r** starts on the positive **x**-axis and turns counter-clockwise. The tip is at angle **θ + φ** and position **(r cos(θ+φ), r sin(θ+φ))**. Faint lines show the vertical (sine) and horizontal (cosine) legs.

2. **Upper graph — sin(θ+φ) and cos(θ+φ) vs θ**  
   The horizontal axis is **θ** in radians (tick labels can be switched to degrees). The curves draw as **θ** advances. Faint “ghost” curves show the full cycle; vertical lines mark each **2π**. When **θ** reaches **(revolutions × 2π)**, **θ** and simulation time **t** reset so the pattern repeats.

3. **Lower panel — traveling waves**  
   Uses the **same ω** as the circle: **sin(x − ωt + φ)** and **cos(…)** versus horizontal phase **x**. While **Play** is on, peaks move **right** at that rate, so **f = ω / 2π** Hz (readout under **ω** and in the canvas caption) matches real-time motion. **Cycles across window** sets how many **2π** of **x** fit on screen (spatial density only). When the upper **θ** sweep resets after **revolutions per cycle**, **θ** and **t** jump back but the lower wave’s phase does not, so the strip stays smooth.

4. **Optional “Euler / complex plane” panel**  
   Explains **z = r e^{iα}** with **α = θ + φ**, and shows live numeric values for **α**, **e^{iα}**, **z**, and **|z|**. When enabled, the circle is labelled **Re** / **Im**.

## Main controls (summary)

| Control | Role |
|--------|------|
| **Show** | Sine only, cosine only, or both (colour-coded). |
| **Pause / Play, Step θ** | Pause, or advance **θ** by a small angle while paused — each step also advances the lower wave’s phase by the same Δθ (= ω Δt), consistent with **ω**. |
| **Reset (1, 0)** | **θ**, **t**, **φ**, and the travel phase to 0 (standard position on the circle), pauses. |
| **Start again** | Resume playback. |
| **Radians / Degrees** | Tick labels on the **θ**-axis only. |
| **Revolutions per cycle** | How many full turns before **θ** (and **t**) reset (upper sweep only; lower wave phase is unchanged). |
| **Cycles across window** | How many full periods **2π** of **x** fit horizontally in the lower panel. |
| **Amplitude (r)** | Scales circle and wave heights together. |
| **Phase φ** | Shifts the waves and rotates the radius on the circle. |
| **ω** | Angular frequency (rad/s) for **dθ/dt** and the lower wave; readout shows **f = ω/2π** Hz. |
| **Save PNG** | Downloads a snapshot of the canvas. |
| **Show Euler…** | Toggles the complex-number panel and on-canvas **Re/Im** labels. |

In-app **?** opens a fuller help overlay.

## Implementation

- Single file: `index.html` (HTML, CSS, and JavaScript together).  
- Drawing uses a **canvas**; layout is responsive to window width.

## Licence / use

Educational use. Adapt or redistribute as you prefer for teaching trigonometry, rotation, and the link to complex exponentials.
