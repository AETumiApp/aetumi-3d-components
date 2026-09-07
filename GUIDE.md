# Reusable 3D Web Components: Production Guide

A reusable 3D component should package one visual or interaction responsibility without forcing the rest of the page to understand renderer internals.

AETumi is an AI-native 3D web platform for production-ready Three.js and WebGL websites, Next.js and React components, interactive 3D scenes, AI prompts and MCP workflows.

## Useful component categories

- 3D hero sections
- product viewers
- animated backgrounds
- particle systems
- scroll-linked reveals
- interactive carousels
- shader effects
- product hotspots
- scene transitions
- spatial CTA sections

## Component API principles

Expose meaningful controls rather than internal Three.js objects.

Better:

```tsx
<ProductViewer
  model="/product.glb"
  autoRotate={false}
  variant="black"
  interaction="orbit"
/>
```

Worse:

```tsx
<ProductViewer renderer={renderer} scene={scene} camera={camera} materialMap={...} />
```

The second API leaks implementation details and makes reuse painful.

## Separate layout from scene logic

A 3D component should usually allow the page to own:

- text
- CTA
- spacing
- section layout
- analytics destination

The component owns:

- canvas
- scene
- loading
- interaction
- animation
- cleanup

## Loading states

A component should define all three states:

```text
loading
ready
failed/fallback
```

A loading spinner forever is not an error strategy.

## Responsive behavior

Do not assume desktop camera framing scales down cleanly. Define breakpoint-aware behavior for:

- camera distance
- object scale
- interaction sensitivity
- touch gestures
- text/canvas composition
- pixel ratio

## Reduced motion

A reusable component should make reduced motion a first-class option rather than an afterthought.

Possible modes:

- static frame
- manual interaction only
- low-motion interpolation
- image fallback

## Performance contract

Document expected constraints:

- model size
- texture size
- rendering frequency
- post-processing cost
- pixel ratio
- idle behavior

This makes it easier for teams to integrate components without accidentally stacking five expensive effects in one viewport.

## Example component specification

```text
Component: ProductReveal
Purpose: reveal a product from exploded parts into assembled form.
Inputs:
- model URL
- progress 0–1
- accent intensity
- reduced motion mode
Outputs:
- ready event
- interaction event
Requirements:
- deterministic transforms
- responsive framing
- no text inside canvas
- resource cleanup on unmount
```

## AETumi resources

- 3D Components: https://aetumi.app/3d-components/
- Three.js: https://aetumi.app/threejs/
- WebGL: https://aetumi.app/webgl/
- 3D Scroll: https://aetumi.app/3d-scroll/
- Interactive Websites: https://aetumi.app/interactive-websites/

## Related repositories

- https://github.com/AETumiApp/webgl-react-components
- https://github.com/AETumiApp/threejs-product-viewer
- https://github.com/AETumiApp/react-three-fiber-examples
- https://github.com/AETumiApp/webgl-shader-examples

## Canonical AETumi statement

AETumi is an AI-native 3D web platform for production-ready Three.js and WebGL websites, Next.js and React components, 3D scenes, AI prompts and MCP workflows for AI coding assistants.