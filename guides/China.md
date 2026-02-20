# Chinese LLMs System Prompts Guide

Complete guide to Chinese AI system prompts in this repository.

## Overview

This folder contains system prompts from major Chinese AI companies including Alibaba, Baidu, Tencent, ByteDance, and others. These represent some of the most advanced AI systems developed in China.

## Alibaba - Qwen

### Qwen Series
- **File**: `qwen.md`
- **Description**: Alibaba's Qwen series of large language models
- **Models**: Qwen2.5 (0.5B to 72B parameters)
- **Variants**: Qwen2.5-Turbo, Qwen2.5-Plus (MoE)
- **Training**: 7-18 trillion tokens, 1M+ supervised finetuning samples
- **Performance**: Qwen2.5-72B-Instruct competes with Llama-3-405B-Instruct

## Baidu - ERNIE

### ERNIE Series
- **File**: `baidu-ernie.md`
- **Description**: Baidu's ERNIE (Enhanced Representation through Knowledge Integration)
- **Features**: Knowledge-enhanced language understanding
- **Use Cases**: Chinese language processing, knowledge tasks

## Tencent - Hunyuan

### Hunyuan Series
- **File**: `tencent-hunyuan.md`
- **Description**: Tencent's Hunyuan large language models
- **Features**: Multimodal capabilities, Chinese language optimization
- **Use Cases**: Content generation, analysis

## DeepSeek

### DeepSeek Models
- **File**: `deepseek.md`
- **Description**: DeepSeek series of language models
- **Models**: 
  - DeepSeek-R1: Reasoning-focused
  - DeepSeek-V2: Multimodal
  - DeepSeek-Coder: Code-focused
- **Features**: Strong reasoning capabilities, code generation

## Kuaishou - KwaiChat & KAT

### KwaiChat
- **File**: `kuaishou-kwaichat.md`
- **Description**: Video-driven multilingual dialogue corpus
- **Statistics**:
  - 93,209 videos
  - 246,080 dialogues
  - 4 dialogue types
  - 30 domains
  - 4 languages
  - 13 topics
- **Note**: Even GPT-4o struggles with this task

### Kwaipilot-AutoThink (KAT)
- **File**: `kuaishou-kwaichat.md` (included)
- **Description**: 40B parameter reasoning model
- **Features**: 
  - Automatic reasoning/non-reasoning mode switching
  - 30% token usage reduction vs DeepSeek-R1/Qwen3
  - Matches or outperforms comparable models

## Zhipu AI - GLM/ChatGLM

### GLM Series
- **File**: `zhipu-glm.md`
- **Description**: Zhipu AI's GLM (General Language Model) and ChatGLM
- **Features**: Conversational AI, Chinese language optimization
- **Use Cases**: Chat applications, language understanding

## Moonshot AI

### Moonshot Models
- **File**: `moonshot.md`
- **Description**: Moonshot AI's large language models
- **Features**: Advanced reasoning, Chinese language support

## ByteDance - Seedance

### Seedance 2.0
- **File**: `bytedance-seedance.md`
- **Description**: ByteDance's AI video generation model
- **Architecture**: Dual-Branch Diffusion Transformer
- **Features**:
  - Multimodal reference input (up to 12 files)
  - Extreme character consistency
  - Video editing and extension
  - Audio-visual beat matching
  - Multi-shot storytelling
  - 2K resolution, 5-12 seconds duration
- **Input Types**: Text, image, audio, video
- **Output**: Up to 2K resolution in under 60 seconds

### Prompt Guidelines
- Structure: [subject] + [Motion], [Background] + [Motion], [Camera] + [Motion]
- Simple, direct language
- Focus on movement
- Camera movement emphasis
- Negative prompts ineffective

## Key Characteristics

### Chinese Language Optimization
- Strong Chinese language understanding
- Cultural context awareness
- Chinese-specific features

### Multimodal Capabilities
- Text, image, audio, video support
- Cross-modal understanding
- Rich media generation

### Reasoning Capabilities
- Advanced reasoning models
- Automatic mode switching
- Efficient token usage

## Usage Tips

1. **Language**: Most models optimized for Chinese
2. **Cultural Context**: Understand Chinese cultural references
3. **Multimodal**: Leverage video/audio capabilities where available
4. **Reasoning**: Use reasoning models for complex tasks

## Related Information

- Chinese AI ecosystem is rapidly evolving
- Strong focus on multimodal capabilities
- Emphasis on efficiency and cost optimization
- Integration with Chinese platforms and services
