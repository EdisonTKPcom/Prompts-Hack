---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

# ByteDance Seedance System Prompt

Source: ByteDance Seedance - AI Video Generation Model

## Overview

Seedance is ByteDance's AI video generation model that creates high-quality videos from text, images, or audio inputs. Seedance 2.0 is the next-generation version launched in February 2026.

## Architecture

Built on a unified multimodal audio-video joint generation architecture using a Dual-Branch Diffusion Transformer, Seedance 2.0 generates video and audio simultaneously in a single forward pass.

## Key Capabilities

**Seedance 2.0** features:

- Multimodal reference input supporting up to 12 files (images, videos, audio)
- Extreme character consistency across sequences
- Video editing and extension capabilities
- Native audio-visual beat matching and synchronization
- Multi-shot storytelling with cinematic camera control
- Output up to 2K resolution, 5-12 seconds duration, in under 60 seconds

**Core Features:**

- Text-to-Video: Natural language scene descriptions
- Image-to-Video: Animating still images with motion
- Audio-to-Video: Using custom audio as control signal
- Native audio generation with dialogue, foley, and ambience layers

## Input Capabilities

The model supports four input modalities—text, image, audio, and video—with up to 12 mixed files accepted at once:
- Up to 9 images
- Up to 3 video clips
- Up to 3 audio clips
- Plus text instructions

## Prompt Guidelines

For effective results with Seedance, follow these principles:

- **Structure**: [subject] + [Motion], [Background] + [Motion], [Camera] + [Motion]
- **Use simple, direct language** - the model expands prompts based on understanding
- **Negative prompts are ineffective**
- **Focus on movement** rather than static elements
- **Avoid contradictions** with the input image content
- **Support multiple continuous actions** and subjects in sequence
- **Camera movement** is a strength - describe lens changes naturally (zoom, pan, follow, etc.)
- **Use adverbs of degree** to highlight action intensity and frequency

**Important Notes:**

- Negative prompts don't work with this system
- The model cannot infer motion intensity from images alone—you must specify it explicitly in prompts

## Performance

Seedance 2.0 delivers substantial improvements over Version 1.5, achieving industry-leading performance on multimodal tasks and excelling at complex interaction and motion scenes that previous models struggled with.

## Output Specifications

- Maximum 2K resolution
- 5-12 second video duration
- Generation time under 60 seconds
- 15-second high-quality multi-shot output with dual-channel audio
