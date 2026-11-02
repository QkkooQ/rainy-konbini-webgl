# Implementation Notes

## Rendering

The scene uses Three.js r160 with a WebGL renderer. Geometry is assembled from
boxes, cylinders, tubes, planes, points, and canvas-generated textures. The
warm storefront lighting, cool night environment, animated rain, fog, and
reflected geometry create the rainy-night atmosphere.

## Interaction

Pointer events support drag rotation, panning, and two-finger pinch zoom.
Wheel input controls camera distance. The camera slowly returns to an idle
rotation after interaction.

## Accessibility and performance

- The canvas has a descriptive accessible label and a screen-reader summary.
- `prefers-reduced-motion` disables rain updates, light animation, ripples, and
  idle camera rotation.
- Device pixel ratio is capped at 2 to limit GPU cost on high-density displays.
- The scene responds to container resizing without reloading.

## Privacy

The standalone page contains no networking, analytics, cookies, or user data
storage. Three.js is served from the local repository.

