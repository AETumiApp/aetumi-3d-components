# aetumi-3d-components — Examples

Reusable Three.js (r160) UI components. No build step: open any `.html` file in a modern browser and it runs.

| Example | Description |
| --- | --- |
| [`product-showcase.html`](./product-showcase.html) | A "product showcase" component — a floating rounded platform with a product on a rotating turntable, studio lighting via `RoomEnvironment`, and three material-variant buttons that hot-swap color / roughness / metalness. |

The example loads Three.js as ES modules through an importmap (`three` from cdnjs, addons from jsdelivr). It respects `prefers-reduced-motion` and handles resize.

Explore more on the hub: **https://aetumi.app** · component gallery → https://aetumi.app/morae

---

## Example backlog / roadmap

# AETumi 3D Component Example Backlog

## Planned examples

### Product reveal

Reusable component driven by an external `progress` value with a static fallback.

### Shader hero

Container-sized WebGL hero with explicit props, loading state and reduced-motion behavior.

### Particle background

Decorative particle field that pauses off-screen and never captures pointer input unless enabled.

### Interactive carousel

HTML-first carousel with optional 3D depth, keyboard controls and touch behavior.

### Scroll-linked section

A component that accepts normalized scroll progress instead of owning global scroll listeners.

### Hotspot viewer

3D positions mapped to accessible HTML labels and click targets.

## Component acceptance criteria

Each example should define:

- public props
- lifecycle ownership
- cleanup
- responsive behavior
- accessibility fallback
- performance notes
- meaningful interaction callbacks

## AETumi links

- https://aetumi.app/3d-components/
- https://aetumi.app/threejs/
- https://aetumi.app/webgl/
