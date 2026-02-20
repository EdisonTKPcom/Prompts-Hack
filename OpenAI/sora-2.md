---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. It summarizes OpenAI’s public documentation and prompting guide for Sora 2. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by OpenAI.

---

# Sora 2 – Video Generation (OpenAI)

Source: OpenAI Sora 2 (Video API), [prompting guide](https://developers.openai.com/cookbook/examples/sora/sora2_prompting_guide/), [video generation docs](https://platform.openai.com/docs/guides/video-generation).

## Overview

Sora 2 is OpenAI’s video (and audio) generation model. It creates clips from text prompts, optional image reference (first frame), and supports remix of completed videos. Two API variants: **sora-2** (speed, iteration) and **sora-2-pro** (higher quality, production).

## Models

| Model | Use case | Notes |
|-------|----------|--------|
| **sora-2** | Speed, exploration, social/prototypes | Faster, good quality; rapid iteration, concepting, rough cuts |
| **sora-2-pro** | Production quality | Higher fidelity, longer render, higher cost; cinematic, marketing |

## API Parameters (set in API, not in prompt text)

- **seconds**: `"4"`, `"8"`, `"12"` (default `"4"`). Length cannot be requested in prose.
- **size**: Resolution string `{width}x{height}`.  
  - **sora-2**: 1280x720, 720x1280  
  - **sora-2-pro**: 1280x720, 720x1280, 1024x1792, 1792x1024  
- **model**: `sora-2` or `sora-2-pro`

Shorter clips (e.g. 4s) tend to follow instructions more reliably; longer sequences can be built by generating multiple clips and editing.

## Prompting (effective prompts)

- **Treat the prompt like a storyboard**: camera framing, depth of field, action in beats, lighting, palette. One clear camera move and one clear subject action per shot.
- **Specificity**: Concrete visual cues (e.g. “wet asphalt, zebra crosswalk, neon reflection”) beat vague ones (“beautiful street at night”). Motion in beats (“takes four steps, pauses, pulls curtain”) beats “walks across the room.”
- **Style**: Set style early (e.g. “90s documentary,” “anamorphic 2.0x, shallow DOF”) so the model carries it through.
- **Length**: Shorter, concise prompts often follow more reliably; longer prompts can restrict creativity. Iteration is expected.
- **Multiple shots**: Describe each shot as a block (one camera, one action, one lighting); can be one sequence or separate clips to stitch.
- **Dialogue**: Can be specified in quotes; model can sync dialogue and sound.
- **Ultra-detailed (cinematic)**: For strict control, use production language: format/look, lenses/filtration, grade/palette, lighting, location/framing, wardrobe/props, diegetic sound, shot list with timings and purpose.

## Inputs and remix

- **Image reference** (`input_reference`): First frame; image must match target `size`. Formats: JPEG, PNG, WebP. Input images with human faces are rejected.
- **Remix** (`remix_video_id` + new prompt): Modify a completed video with one focused change (e.g. palette, one added element); preserves structure and reduces artifacts vs full regenerate.

## Guardrails and restrictions (API)

- **Input images**: Images with human faces are rejected.
- **Real people**: Cannot generate real people (including public figures).
- **Copyright**: Copyrighted characters and copyrighted music are rejected.
- **Audience**: Only content suitable for under-18; no bypass in docs at time of writing.
- Prompts, reference images, and (where applicable) transcripts must respect these to avoid failed jobs.

## Summary table

| Aspect | Detail |
|--------|--------|
| **Models** | sora-2 (speed), sora-2-pro (quality) |
| **Duration** | 4, 8, or 12 s (API only) |
| **Resolutions** | 1280x720, 720x1280; Pro also 1024x1792, 1792x1024 |
| **Prompt** | Storyboard-style: framing, action in beats, light, palette; concise often more reliable |
| **Reference** | Optional first-frame image (no faces); remix from completed video |
| **Safety** | No real people, no face input, no copyrighted characters/music; under-18 suitable only |

## References

- [Video generation with Sora](https://platform.openai.com/docs/guides/video-generation)
- [Sora 2 prompting guide](https://developers.openai.com/cookbook/examples/sora/sora2_prompting_guide/)
- [Sora 2 model / API](https://platform.openai.com/docs/models/sora-2)
- [OpenAI Sora 2 announcement](https://openai.com/index/sora-2/)
