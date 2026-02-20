# xAI Grok System Prompts Guide

Complete guide to xAI's Grok system prompts in this repository.

## Overview

xAI's Grok is an AI assistant with multiple model versions and persona configurations. This folder contains system prompts for different Grok variants and personality configurations.

- **Deeper dive**: `xai-deeper-dive.md` – models & access, task/behavior (4.2 team), **media (images, video, Grok Imagine, animation/GIF)**, tools summary, X search, safety, summary table.

## Grok Models

### Grok 3
- **File**: `grok-3.md`
- **Description**: Grok version 3
- **Features**: Advanced capabilities, improved performance

### Grok 4
- **File**: `grok-4.md`
- **Description**: Grok version 4
- **Features**: Enhanced capabilities, latest features

### Grok 4.1 Beta
- **File**: `grok-4.1-beta.md`
- **Description**: Beta version of Grok 4.1
- **Features**: Beta features, experimental capabilities

### Grok 4.2
- **File**: `grok-4.2.md`
- **Description**: Grok version 4.2
- **Features**: Multi-agent team (Harper, Benjamin, Lucas), Grok Imagine (image generation/edit), code execution, X search, web search, render components

## Media: Images, Video, and Animation

- **View**: `view_image` (by URL/id), `view_x_video` (X-hosted video frames/subtitles)
- **Search**: `search_images` (web image search by description); `render_searched_image` for carousel in response
- **Grok Imagine**: `render_generated_image` (text-to-image), `render_edited_image` (edit prior image in chat); confirm before generating where required (Grok 3, 4, personas)
- **Animation / code**: `render_file` from code sandbox – supports **PNG, JPG, GIF, WebP, BMP** (e.g. plots, charts, GIFs from code). No dedicated animation or video-generation tool; video is view-only on X.
- See **Deeper dive** for when-to-use and policy details.

## Grok Personas

### Personas Configuration
- **File**: `grok-personas.md`
- **Description**: Multiple personality configurations for Grok
- **Features**: Different personas with unique characteristics

### Persona Types
- Various personality configurations
- Customizable behavior
- Different interaction styles
- Specialized use cases

## Safety Instructions

### Safety Configuration
- **File**: `grok.com-post-new-safety-instructions.md`
- **Description**: Safety guidelines and instructions
- **Features**: Content moderation, safety guardrails

## Key Features

### Model Evolution
- Progressive model improvements
- Version-specific features
- Performance enhancements
- Capability expansions

### Personality System
- Multiple persona options
- Customizable behavior
- Different interaction styles
- Specialized configurations

### Safety Focus
- Content moderation
- Safety guidelines
- Guardrails implementation
- User protection

## Usage Tips

1. **Model Selection**: Choose based on version features
2. **Persona Selection**: Select persona matching use case
3. **Safety**: Review safety instructions for content guidelines
4. **Updates**: Check for latest version features

## Deeper Dive

- **File**: `xai-deeper-dive.md`
- **Contents**: Models & access (Grok 3/4, SuperGrok, API redirects); task and behavior (4.2 team collab, language, corrections, values); **media** – view_image, view_x_video, search_images, **Grok Imagine** (generate/edit), **animation** (GIF via code + render_file; no video gen); tools summary; X search and media filters; safety; personas; summary table.

## Related Information

- xAI's approach to AI assistants
- Personality customization
- Safety and moderation
- Model evolution and improvements
