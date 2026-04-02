# Sine & cosine from the unit circle

A self-contained web page that animates how sine and cosine arise from a radius rotating on a circle, and how angle and angular frequency relate over time.

## How to run

Open `index.html` in a modern desktop browser (Chrome, Edge, Firefox, Safari). No build step or server is required. If your browser blocks downloads when using `file://`, use a simple local server or open the file from disk as your environment allows.

## What it shows

1. **Unit circle (complex plane)**  
   A radius of length **r** starts on the positive **x**-axis and turns counter-clockwise. The tip is at angle **θ + φ** and position **(r cos(θ+φ), r sin(θ+φ))**. Faint lines show the vertical (sine) and horizontal (cosine) legs.

2. **Upper graph — sin(θ+φ) and cos(θ+φ) vs θ**  
   The horizontal axis is **θ** in radians (tick labels can be switched to degrees). The curves draw as **θ** advances. Faint “ghost” curves show the full cycle; vertical lines mark each **2π**. When **θ** reaches **(revolutions × 2π)**, **θ** and simulation time **t** reset so the pattern repeats.

3. **Lower graphs — time domain**  
   - **θ(t)** — cumulative angle **∫ ω(t) dt** (slope **dθ/dt = ω(t)**).  
   - **ω(t)** — instantaneous angular frequency in rad/s. With **variation** at 0, **ω** is constant (flat line). With a **pattern**, **ω** can vary sinusoidally (FM-style) or ramp up/down each segment (segment length tied to a nominal full cycle at **ω base**).

4. **Optional “Euler / complex plane” panel**  
   Explains **z = r e^{iα}** with **α = θ + φ**, and shows live numeric values for **α**, **e^{iα}**, **z**, and **|z|**. When enabled, the circle is labelled **Re** / **Im**.

## Main controls (summary)

| Control | Role |
|--------|------|
| **Show** | Sine only, cosine only, or both (colour-coded). |
| **Pause / Play, Step θ** | Pause animation or advance **θ** in small steps (handles multiple revolutions per step correctly). |
| **Reset (1, 0)** | **θ**, **t**, and **φ** to 0 (standard position on the circle), clears traces, pauses. |
| **Start again** | Resume playback. |
| **Radians / Degrees** | Tick labels on the **θ**-axis only. |
| **Rotation speed** | Scales how fast simulation time and **θ** advance (default **0.4×**). |
| **Revolutions per cycle** | How many full turns before **θ** (and **t**) reset. |
| **Amplitude (r)** | Scales circle and wave heights together. |
| **Phase φ** | Shifts the waves and rotates the radius on the circle. |
| **ω base** | Centre angular frequency (rad/s); **dθ/dt = ω(t)**. |
| **ω variation** | How much **ω** swings around the base (0 ⇒ constant **ω**). |
| **ω vs time pattern** | Constant, sinusoidal **ω(t)**, or ramp **ω** up/down each segment. |
| **Save PNG** | Downloads a snapshot of the canvas. |
| **Show Euler…** | Toggles the complex-number panel and on-canvas **Re/Im** labels. |

In-app **?** opens a fuller help overlay.

## Implementation

- Single file: `index.html` (HTML, CSS, and JavaScript together).  
- Drawing uses a **canvas**; layout is responsive to window width.

## Licence / use

Educational use. Adapt or redistribute as you prefer for teaching trigonometry, rotation, and the link to complex exponentials.
