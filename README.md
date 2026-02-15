# 🫧 Liquid Glass — Pure HTML & CSS

A single-file showcase of Apple-style liquid glass UI components, built entirely with HTML and CSS. No JavaScript. No frameworks. Just the raw capabilities of modern CSS pushed to their limit.

![Liquid Glass Preview](Liquid%20Glass.png)

## What This Is

This project recreates the translucent, refractive glass material that Apple introduced across its platforms — the kind of surface that feels like it bends light and sits physically above the content behind it. Everything here lives in one self-contained HTML file.

The effect is achieved through a combination of `backdrop-filter`, `color-mix()`, layered `box-shadow` with inset highlights and shadows, and an SVG `feTurbulence` displacement filter that introduces subtle organic distortion to the blur. The result is a surface that genuinely looks like frosted glass rather than a flat overlay with opacity.

## Components

- Menu bar with pill-shaped glass container and nested glass buttons
- Toast notification with icon, metadata, and action button
- Standalone button pairs (Cancel / Confirm)
- Settings icon button with circular glass frame

Each component appears in both light and dark themes, side by side.

## How It Works

The core `.liquid-glass` class does the heavy lifting:

- `backdrop-filter: blur()` combined with an SVG turbulence displacement map creates a non-uniform, organic blur
- `color-mix(in srgb, ...)` controls transparency at every layer without relying on `rgba` or `opacity`
- Six layered `inset box-shadow` values simulate top-light highlights, edge reflections, and internal depth — mimicking how real glass catches and redirects light
- CSS custom properties (`--glass-reflex-opacity-light`, `--glass-reflex-opacity-dark`) let the dark theme dial up shadow intensity and pull back highlights, just as a real material would behave under different lighting

## Usage

Open `liquid-glass-showcase.html` in any modern browser. That's it. There's nothing to install, build, or configure.

For the best visual fidelity, use a Chromium-based browser (Chrome, Edge, Arc) or Safari. Firefox supports `backdrop-filter` but does not apply the SVG displacement filter through `backdrop-filter: url()`, so the organic distortion won't render there.

## Tech Stack

- HTML5
- CSS3 (`backdrop-filter`, `color-mix()`, CSS custom properties)
- Inline SVG filter (`feTurbulence` + `feDisplacementMap`)

## License

This project is licensed under the Apache License 2.0 — see the [LICENSE](LICENSE) file for details.
