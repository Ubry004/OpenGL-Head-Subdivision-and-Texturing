# DEMO
Note that the low framerate is simply because of limitations with ezgif(.)com. This simply shows functionality :)

![](./DEMO.gif)

Head model loaded with ASSIMP

Perspective View
- The scene is drawn with a perspective camera that mimics how our eyes perceive
depth with a 45 degree field of view and near/far clipping planes (0.1 units and
100 units).
  
Camera Controls
- Use the ← and → keys to spin the camera around the model horizontally (like
walking in a circle around it).
Use the ↑ and ↓ keys to tilt the camera up and down, following a vertical arc
- The camera always looks at the center of the scene.
- You can also zoom with + and - on the numpad
- The range for y is clamped to avoid any shenanigans

Quick Reset
- Pressing r returns the view and all toggles to their original state: clear
rotations, default display modes, and textures on.
Wireframe Overlay
- The w key switches the model between solid and wireframe rendering
Facetted (UV-Mapped Texture!!) vs. Smooth Head
- Press f to show or hide the original facetted head, which displays the raw
triangle mesh with my face texture.
- Press p to show or hide the smooth version of the same head after subdivision
(level 2 by default).

Subdivision for Smoothness
- The head model is refined using Loop subdivision at two levels.
- Each subdivision step splits each triangle into smaller ones and adjusts their
positions to soften sharp edges.
- The result is a much smoother surface that still follows the shape of the
original mesh.
- You can choose to see just the smooth surface or overlay its control net (the
original coarse triangles) to compare.

Texture Mapping
- A single image is wrapped onto both the facetted and smooth heads.
- UV coordinates built into the mesh ensure the texture stretches and aligns
properly over the curved surface.

Texture Toggle
- Press u to turn the head’s texture on or off, switching between the wrapped image
and a solid color.
