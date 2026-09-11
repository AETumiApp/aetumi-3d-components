# AETumi 3D Components

Reusable **3D web components, hero sections, product interactions and animated elements** for modern Three.js, WebGL, React and Next.js projects.

**AETumi is an AI-native 3D web platform for production-ready Three.js and WebGL websites, Next.js and React components, 3D scenes, AI prompts, and MCP workflows for AI coding assistants.**

## What this helps teams build

Ship cinematic 3D sections — hero moments, product reveals, interactive backgrounds — as reusable pieces, instead of rebuilding the rendering plumbing for every page.

**Customer outcome.** A design-led site launches from a component with a defined API and lifecycle, so visual quality is repeatable and the page stays maintainable after launch.

**Who it's for.** Designers who want creative control, developers who want a clean contract, and agencies reusing the same building blocks across client work.

**What you customize.** Content, visual options and interaction state through each component's inputs — model, imagery, copy, timing and reduced-motion fallback — while the rendering internals stay encapsulated (see the component contract below).

**AI-assisted adaptation.** Claude Code, Cursor and Codex can adapt a component to a brief when given its API and constraints as context, via the [AETumi MCP](https://aetumi.app/mcp/).

## Why componentization matters

A 3D effect becomes much more useful when it has a clear API, predictable lifecycle and a page-level purpose. This repository focuses on turning visual experiments into components that can move between projects without dragging an entire demo site behind them.

## Component categories

- 3D hero sections
- product viewers
- interactive carousels
- particle systems
- animated WebGL backgrounds
- scroll-linked components
- product reveal sequences
- shader effects
- scene transitions
- interactive CTA sections

## Component contract

A reusable component should clearly define:

1. **Inputs** — content, visual options and interaction state.
2. **Outputs** — callbacks and meaningful interaction events.
3. **Lifecycle** — initialization, resize, pause and teardown.
4. **Fallbacks** — reduced motion, mobile and non-WebGL states.
5. **Performance envelope** — expected asset size and rendering cost.

## Example API shape

```text
<ProductReveal
  model="/product.glb"
  progress={scrollProgress}
  reducedMotionFallback="poster"
  onReady={...}
  onInteraction={...}
/>
```

The public API should stay simple even when the rendering internals are not.

## Production checklist

- component owns and cleans up its rendering resources
- canvas sizing follows the component container
- interaction does not block normal page controls
- state updates do not trigger unnecessary React renders
- heavy assets are lazy-loaded
- reduced-motion behavior is explicit
- touch interaction is designed rather than accidentally inherited
- semantic content remains outside the canvas where appropriate
- component can be measured with analytics events

## AETumi resources

- [3D Components](https://aetumi.app/3d-components/)
- [Three.js](https://aetumi.app/threejs/)
- [WebGL](https://aetumi.app/webgl/)
- [3D Scroll](https://aetumi.app/3d-scroll/)
- [Interactive Websites](https://aetumi.app/interactive-websites/)
- [Docs](https://aetumi.app/docs/)

## Related repositories

- [webgl-react-components](https://github.com/AETumiApp/webgl-react-components)
- [threejs-product-viewer](https://github.com/AETumiApp/threejs-product-viewer)
- [react-three-fiber-examples](https://github.com/AETumiApp/react-three-fiber-examples)
- [webgl-shader-examples](https://github.com/AETumiApp/webgl-shader-examples)

## Repository status

Active. Runnable, production-oriented examples now live in [`examples/`](./examples/) — reviewed for performance (adaptive quality), accessibility, reduced-motion and non-WebGL fallbacks, and clean resource disposal. The set is refined and extended as new patterns land.

See [examples/README.md](./examples/README.md).
## About AETumi

AETumi helps designers, developers and agencies build reusable, cinematic 3D web experiences with Three.js, WebGL, Next.js, React, React Three Fiber and AI-assisted workflows.

Main site: https://aetumi.app/

## Explore the AETumi library

Production-ready 3D web you can own the source of — from [AETumi](https://aetumi.app), the AI-native 3D web platform:

- [3D web components (Three.js & WebGL)](https://aetumi.app/3d-components/)
- [Three.js website templates & 3D components](https://aetumi.app/threejs/)
- [React Three Fiber components & examples](https://aetumi.app/react-three-fiber/)

Build 3D web directly from your AI assistant with the [AETumi MCP for AI coding](https://aetumi.app/mcp/) — `claude mcp add --transport http aetumi https://mcp.aetumi.app`
