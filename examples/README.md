# aetumi-3d-components — Examples

Reusable, **production-grade** Three.js (r160) UI components. No build step: open any `.html` file in a modern browser and it runs.

| Example | Description |
| --- | --- |
| [`product-showcase.html`](./product-showcase.html) | A "product showcase" component — a floating platform with a product on a rotating turntable, studio lighting via `RoomEnvironment` + ACES tone mapping, and three material-variant buttons that hot-swap color / roughness / metalness. |

### Expert / production features (every example)

- **Capability detection + graceful fallback** — probes WebGL2 → WebGL → none. With no WebGL context (or `prefers-reduced-motion`) it paints a tasteful CSS gradient poster instead of a blank canvas; low-power devices start at reduced quality and mesh detail.
- **Adaptive performance** — DPR capped at 2; a rolling FPS average steps DPR down below 50 fps and back up above 58 fps with hysteresis. The loop pauses when the component scrolls offscreen (`IntersectionObserver`) or the tab is hidden.
- **Strict cleanup** — one `dispose()` releases the PMREM render target, all geometries/materials, the environment map, listeners and the renderer, on `pagehide`.
- **Accessibility** — the canvas is `role="img"` with an `aria-label`; the variant buttons are native `<button>`s (keyboard-reachable) with `aria-pressed` and visible focus rings; motion respects `prefers-reduced-motion`.
- **Premium look** — image-based studio lighting (`RoomEnvironment`) through a PMREM environment map, ACES Filmic tone mapping, and an emissive accent ring.

Three.js r160 is loaded as ES modules through an importmap on **jsDelivr only** (`three` + `three/addons/`).

Explore more on the hub: **https://aetumi.app** · component gallery → https://aetumi.app/morae
