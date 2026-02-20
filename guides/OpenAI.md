# OpenAI System Prompts Guide

Complete guide to OpenAI's GPT system prompts in this repository.

## Overview

OpenAI's GPT models include GPT-5 series, GPT-4 series, O-series (o3, o4-mini), and various tool-specific configurations. This folder contains system prompts for different personalities, tools, and API configurations.

## GPT-5 Series

### Personalities

- **Default**: `gpt-5.1-default.md` - Standard personality
- **Nerdy**: `gpt-5.1-nerdy.md` - Technical, detailed
- **Quirky**: `gpt-5.1-quirky.md` - Playful, creative
- **Candid**: `gpt-5.1-candid.md` - Direct, honest
- **Cynical**: `gpt-5.1-cynical.md` - Skeptical, critical
- **Professional**: `gpt-5.1-professional.md` - Formal, business-oriented
- **Friendly**: `gpt-5.1-friendly.md` - Warm, approachable
- **Efficient**: `gpt-5.1-efficient.md` - Concise, focused
- **Listener**: `gpt-5-listener-personality.md` - Empathetic, attentive
- **Robot**: `gpt-5-robot-personality.md` - Mechanical, precise
- **Cynic**: `gpt-5-cynic-personality.md` - Critical, questioning

### Thinking Models

- **GPT-5 Thinking**: `gpt-5-thinking.md` - Reasoning-focused
- **GPT-5.2 Thinking**: `gpt-5.2-thinking.md` - Enhanced reasoning

## GPT-4 Series

- **GPT-4.1**: `GPT-4.1.md`
- **GPT-4.1 Mini**: `GPT-4.1-mini.md`
- **GPT-4.5**: `GPT-4.5.md`
- **GPT-4o**: `GPT-4o-advanced-voice-mode.md` (legacy voice mode and deprecation guideline moved to `Old/`)
- **GPT-4o WhatsApp**: `GPT-4o-WhatsApp.md`

## O-Series (Reasoning Models)

### O3
- **O3**: `o3.md`
- **API Versions**: `API/o3-low-api.md`, `API/o3-medium-api.md`, `API/o3-high-api.md`

### O4-Mini
- **O4-Mini**: `o4-mini.md`
- **High**: `o4-mini-high.md`
- **API Versions**: `API/o4-mini-low-api.md`, `API/o4-mini-medium-api.md`, `API/o4-mini-high.md`

## Tool-Specific Prompts

### Research & Search
- **Web Search**: `tool-web-search.md`
- **Deep Research**: `tool-deep-research.md`
- **File Search**: `tool-file_search.md`

### Code & Development
- **Python**: `tool-python.md`
- **Python Code**: `tool-python-code.md`
- **Canvas/Canmore**: `tool-canvas-canmore.md`

### Memory & Context
- **Advanced Memory**: `tool-advanced-memory.md`
- **Memory Bio**: `tool-memory-bio.md`

### Media
- **Image Generation**: `tool-create-image-image_gen.md`
- **Video (Sora 2)**: `sora-2.md` – Sora 2 / Sora 2 Pro; API params (seconds, size); prompting guide (storyboard-style, style, motion); image reference & remix; guardrails

## Specialized Versions

### Codex
- **Codex**: `Codex.md` - Code-focused model
- **Codex CLI**: `codex-cli.md` - Command-line interface

### ChatGPT Variants
- **ChatGPT Atlas**: `chatgpt-atlas.md`
- **Agent Mode**: `ChatGPT-GPT-5-Agent-mode-System-Prompt.md`

### Study & Learning
- **Study and Learn**: `Study and learn.md`

## API Configurations

Located in `API/` folder:
- O3 API configurations (low/medium/high reasoning effort)
- O4-Mini API configurations
- GPT-5 reasoning effort configurations
- API-specific system messages

## Safety & Policies

- **Image Safety Policies**: `Image safety policies.md`
- **Prompt Image Safety**: `prompt-image-safety-policies.md`
- **Automation Context**: `prompt-automation-context.md`

## Legacy Versions

Located in `Old/` folder:
- **chatgpt.com-o4-mini.md** – Older ChatGPT.com o4-mini
- **chatgpt-4o-mini.txt** – 4o-mini (text)
- **GPT-4o-legacy-voice-mode.md** – Legacy GPT-4o voice mode
- **2026-02-04-GPT-4o-with-deprecation-guideline.md** – GPT-4o deprecation (Feb 2026) system prompt

## Key Features

### Personality Instructions
- Detailed personality definitions
- Behavioral guidelines
- Tone and style specifications

### Tool Usage
- Extensive tool calling capabilities
- Specialized tool configurations
- API integration guidelines

### Safety Guidelines
- Content moderation rules
- Safety guardrails
- Usage restrictions

## Usage Tips

1. **Personality Selection**: Choose based on use case (professional vs. friendly)
2. **Model Selection**: GPT-5 for latest features, GPT-4 for stability
3. **Tool Configuration**: Check tool-specific prompts for specialized tasks
4. **API Usage**: Review API folder for API-specific configurations

## Related Files

- `Old/2026-02-04-GPT-4o-with-deprecation-guideline.md`: GPT-4o deprecation system prompt (in Old)
- `4o-2025-09-03-new-personality.md`: Personality updates
