# 3D Render

Use this reference for modeled, sculpted, product-visualization, motion-design, clay, toy-like, or photoreal rendered imagery.

## Observe

- Modeling language: primitive-based, sculpted, low-poly, subdivided, hard-surface, inflated, beveled, or miniature.
- Edge treatment, bevel width, topology-visible artifacts, thickness, seams, joints, and contact with the ground or base.
- Surface response: matte or glossy, roughness, metalness, transparency, refraction, subsurface scattering, anisotropy, clear coat, and microtexture.
- Lighting structure: key/fill/rim relationship, environment light, practical emitters, shadow softness, reflections, ambient occlusion, caustic-like effects, and volumetric light.
- Camera view, focal hierarchy, depth of field, scale cues, background sweep, and composition.
- Render finish: path-traced cleanliness, stylized shading, denoising softness, sampling noise, bloom, chromatic effects, or compositing.

## Infer cautiously

Pixels rarely establish whether C4D, Blender, Octane, Redshift, Cycles, Eevee, or another tool produced the image. Name software or a renderer only when provenance is supplied. Otherwise describe its visual equivalent or label a named workflow as a recreation choice, for example a clean path-traced studio look or a real-time stylized render.

Do not treat `PBR`, `8K`, or three-point lighting as mandatory quality tokens. Use them only when the visible material behavior or requested production target warrants them.

## Compile

Order the prompt around object geometry, material response, color placement, lighting/reflections, camera, and finish. Prevent contradictions between matte surfaces and mirror reflections, opaque materials and strong refraction, or miniature scale and full-scale environmental cues unless intentionally mixed.
