---
name: visual-prompt-reconstructor
description: "Analyze a user-provided reference image and reconstruct copy-ready Korean and English AI image prompts. Use for 프롬프트 역추적·복원, reverse prompting, 提示词反推, or detailed visual decomposition of photography, illustration, 3D renders, landscapes, typography/logos, products, portraits, and IP characters. Do not use for simple captions, OCR-only work, or generation/editing without reference-prompt analysis."
---

# Visual Prompt Reconstructor

Turn an accessible reference image into a high-fidelity reconstruction blueprint and model-ready prompts. Reconstruct a prompt that can reproduce the visible result; never claim to recover the image's exact original prompt, seed, model, camera, or production workflow from pixels alone.

## Start from the image

- Require an attached image or an accessible image file. If it is missing, unreadable, or too small for the requested detail, ask the user to attach a usable copy rather than inventing content.
- Inspect the image at useful detail before drafting. Use file metadata only when it is actually available and relevant.
- If several images are supplied, analyze them separately unless the user identifies them as references for one shared target.
- Accept an optional target generator or editing workflow. If none is named, produce model-neutral prompts without delaying the task for clarification.

## Classify without forcing one category

Choose one or more labels on two independent axes:

- Medium: photography, illustration, 3D render, or mixed media.
- Subject or overlay: landscape/scene, portrait, product, typography/logo, or IP character.

Apply the shared analysis once, then read only the references needed for the selected labels:

- Photography, portraits, products, or documentary images: [references/photography.md](references/photography.md)
- Drawn, painted, flat, cel-shaded, or graphic work: [references/illustration.md](references/illustration.md)
- Modeled or rendered imagery: [references/3d-render.md](references/3d-render.md)
- Natural, architectural, urban, or environmental scenes: [references/landscape-scene.md](references/landscape-scene.md)
- Lettering, type treatments, wordmarks, or logos: [references/typography-logo.md](references/typography-logo.md)
- Mascots, blind-box figures, chibi designs, or recurring characters: [references/ip-character.md](references/ip-character.md)

For a request framed as complete, detailed, production-ready, or model-specific, also read [references/output-contract.md](references/output-contract.md). Do not load unrelated category references.

## Analyze before compiling

Build one internal visual blueprint from the image:

- subject, identity-defining features, action, and visual narrative;
- composition, crop, spatial relationships, perspective, and depth;
- palette and where primary, secondary, and accent colors appear;
- light direction, size/softness, contrast, shadows, reflections, and atmosphere;
- materials, surface response, texture, line or modeling language;
- background, environment, focus hierarchy, sharpness, grain, and visible artifacts.

Record direct observations separately from interpretation. Surface uncertainty only when it can change the reconstruction. Do not clutter ordinary output with an evidence tag on every sentence.

Treat these as unknown unless metadata or supplied provenance establishes them: exact camera body, lens model, focal length, aperture, shutter, ISO, software, renderer, sampler, seed, workflow, or original output resolution. When useful, recommend a visual equivalent as a recreation choice and label it as such.

## Language contract

- Write the analysis in Korean by default.
- Always provide a Korean full prompt and an English full prompt. Derive both from the same blueprint so their subjects, spatial relations, emphasis, and constraints match.
- Make the English prompt natural and copy-ready, not a mechanically literal translation.
- Add Japanese or Chinese only when the user requests it. If the user requests a different language combination, follow that request.
- Preserve visible source text, capitalization, punctuation, symbols, and brand spelling exactly across every language version. Do not translate text that must appear inside the generated image unless asked.

## Default response

Use only sections that add value:

1. **판정** — concise multi-label classification.
2. **시각 분석** — Korean explanation of the relevant visual structure.
3. **재현 핵심** — what must remain, what may vary, and what to avoid when those distinctions matter.
4. **한국어 완성 프롬프트** — one copy-ready code block.
5. **English full prompt** — one copy-ready code block.

Add conditional sections only when applicable:

- exact text transcription for visible lettering;
- a character lock for recurring IP identity;
- material uncertainties or A/B variants for consequential ambiguity;
- target-model adaptation when a generator is named;
- negative prompts or recommended settings only when supported and useful.

If the user asks for prompts only, omit the explanatory sections except for a brief material uncertainty that prevents misuse.

## Prompt quality

- Write a coherent production description rather than a long bag of fashionable keywords. State important relationships and color placement explicitly.
- Put identity and composition before style polish. Prefer concrete visual traits over generic quality tokens.
- Do not insert `8K`, `masterpiece`, `best quality`, a renderer name, or precise camera settings unless they materially support a requested recreation choice.
- Do not identify an artist or photographer from visual similarity alone. Describe the observable medium, line, palette, lighting, composition, and texture instead.
- Keep text transcription separate from typography analysis. Mark uncertain or illegible characters instead of correcting or completing them silently.
- Use negative prompts only for specific likely failures and only when the target workflow can use them. Otherwise integrate concise exclusions into the main prompt.
- Never present a suggested setting as a fact about the source image.

When the user also asks to generate or edit an image, use the completed reconstruction blueprint in the available image-generation workflow and preserve the user's requested scope.
