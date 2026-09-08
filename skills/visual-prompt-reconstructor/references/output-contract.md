# Output Contract

Read this reference for complete, detailed, production-ready, or model-specific requests. Keep the response proportional to the image; this is a decision framework, not a requirement to print every possible field.

## Reconstruction notice

When the user asks for the original or complete prompt, state once that pixels cannot prove the original prompt, model, seed, or production settings. Describe the result as a high-fidelity recreation prompt. Do not repeat the notice throughout the response.

## Visual decomposition

Cover the fields that materially affect reproduction:

- subject and narrative;
- composition, crop, negative space, depth planes, and spatial relationships;
- style and medium;
- palette plus the location and proportion of dominant and accent colors;
- lighting, shadow direction and hardness, reflections, and atmospheric effects;
- material, texture, line, brush, or surface behavior;
- perspective, camera feel, focus hierarchy, and depth of field;
- background, mood, sharpness, grain, and visible artifacts.

Use explicit uncertainty only for consequential claims:

- **관찰:** directly visible or supported by actual metadata.
- **추정:** a plausible interpretation of the pixels.
- **재현 제안:** a new setting chosen to reproduce the look.
- **확인 불가:** information the image cannot establish.

Do not attach these labels to every sentence. A compact uncertainty note is normally enough.

## Reconstruction blueprint

Use these fields when they improve control:

- **Must preserve:** three to seven identity, silhouette, composition, palette, or text anchors.
- **Flexible:** details that can vary without changing the target impression.
- **Must avoid:** image-specific failure modes, not generic quality insults.

For meaningful ambiguity, provide two clearly differentiated alternatives rather than hiding a low-confidence guess inside one prompt.

## Master prompt construction

Compose both Korean and English prompts from the same semantic plan in this order when applicable:

1. subject and identity;
2. pose, action, or narrative;
3. composition and spatial placement;
4. environment and background;
5. medium and concrete style traits;
6. material and texture;
7. palette and color placement;
8. lighting and shadow behavior;
9. perspective, lens feel, focus, and depth of field;
10. finishing constraints and image-specific exclusions.

The English prompt should be idiomatic and immediately usable. It may reorganize grammar, but it must not add or remove visual requirements relative to the Korean prompt.

## Conditional model adaptation

- Always retain a model-neutral Korean and English master prompt.
- Add a model-specific variant only when the user names the model or asks for one.
- Use only syntax known to be supported by the named workflow. Do not invent flags, weights, sampler settings, or negative-prompt support.
- Label seed, steps, guidance, focal length, aperture, renderer, and output size as recreation settings, never source facts.
- If the target has no separate negative field, integrate a few concrete exclusions into natural language.

## Final consistency check

Before answering, check once that:

- the subject, silhouette, crop, and spatial relations match the blueprint;
- dominant and accent colors remain in the intended locations;
- light direction and shadow softness do not contradict each other;
- visible text is identical in all prompt languages;
- character, product, or logo anchors remain stable;
- no unsupported camera, renderer, resolution, or authorship claim appears as fact.
