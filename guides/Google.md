# Google AI System Prompts Guide

Complete guide to Google's AI system prompts in this repository.

## Overview

Google's AI ecosystem includes Gemini models, Antigravity (agentic IDE), NotebookLM, Workspace integrations, and various specialized assistants. This folder contains system prompts for different Google AI products.

## Gemini Series

### Gemini 3.0
- **Gemini 3 Pro**: `gemini-3-pro.md` - Most capable model
- **Gemini 3 Flash**: `gemini-3-flash.md` - Fast, efficient
- **Gemini 3 Fast**: `Gemini-3-fast.md` - Optimized for speed

### Gemini 2.5
- **Gemini 2.5 Pro**: `gemini-2.5-pro-guided-learning.md`, `gemini-2.5-pro-webapp.md`
- **Gemini 2.5 Flash**: `gemini-2.5-flash-image-preview.md`
- **Gemini 2.0 Flash**: `gemini-2.0-flash-webapp.md`

## Nano Banana (Image Generation)

### Nano Banana
- **File**: `nano-banana.md`
- **Description**: Gemini 2.5 Flash Image (codename: Nano Banana)
- **Launch**: August 2025
- **Features**:
  - Image generation and editing
  - 95%+ character consistency
  - 1-2 second generation time
  - 90% first-try success rate
  - Conversational workflow
  - Multimodal operation
- **Use Cases**: High-volume image generation, fast editing, character consistency

### Nano Banana Pro
- **File**: `nano-banana-pro.md`
- **Description**: Gemini 3 Pro Image Preview (codename: Nano Banana Pro)
- **Features**:
  - Professional asset production
  - Advanced reasoning
  - High-fidelity text rendering
  - Complex instruction following
- **Use Cases**: Professional assets, commercial projects, text-heavy images

## Antigravity (Agentic IDE)

- **File**: `antigravity.md`
- **Description**: Google DeepMind's agentic coding assistant
- **Features**:
  - Browser subagent with WebP recording
  - Codebase search
  - Command execution
  - File operations
  - Knowledge Items (KI) system
  - Workflows and rules
- **Use Cases**: Software development, web app creation, debugging

### Key Components
- Tool definitions (20+ tools)
- Web application development guidelines
- Design aesthetics requirements
- SEO best practices
- Persistent context system

## Specialized Integrations

### Gemini Workspace
- **File**: `gemini-workspace.md`
- **Description**: Google Workspace integration
- **Features**: Document analysis, email assistance, workspace corpus search

### Gemini in Chrome
- **File**: `gemini_in_chrome.md`
- **Description**: Browser extension
- **Features**: Web page analysis, browsing assistance

### NotebookLM
- **File**: `NotebookLM-chat.md`
- **Deeper dive**: `notebooklm-deeper-dive.md` – all leaked prompt versions, custom goals/personas, 1M-token context, citation rules, security (prompt injection / exfiltration)
- **Description**: AI research assistant grounded in user sources (PDFs, web, YouTube, audio, Docs)
- **Features**: Source-grounded chat, [i] citations, tone/style overrides, custom goals (up to 10k chars), 1M-token context (Oct 2025+), document analysis, research

### Google AI Studios
- **File**: `google-ai-studios.md`
- **Description**: AI development platform
- **Features**: Model testing, prompt engineering

## CLI & System Prompts

### Gemini CLI
- **File**: `Gemini-cli system prompt.md`
- **Description**: Command-line interface
- **Features**: Terminal-based AI assistance

## Specialized Models

### Nano Banana Series
- **Nano Banana**: Fast image generation (Gemini 2.5 Flash Image)
- **Nano Banana Pro**: Professional image generation (Gemini 3 Pro Image Preview)
- Available across Gemini app, Search, Lens, Photos, Workspace

### Gemini Diffusion
- **File**: `gemini-diffusion.md`
- **Description**: Image generation model
- **Features**: Text-to-image, image editing

## Key Features Across Models

### Tool Usage
- Extensive tool calling capabilities
- Browser interactions
- File system operations
- Code execution

### Design Philosophy
- Rich aesthetics requirements
- Premium design standards
- Modern typography
- Color theory application

### Safety & Guidelines
- Content moderation
- Safety guardrails
- Usage restrictions

## Usage Tips

1. **Model Selection**: 
   - Pro for complex tasks
   - Flash for speed
   - Antigravity for coding

2. **Integration Selection**:
   - Workspace for documents
   - Chrome for browsing
   - NotebookLM for research

3. **Tool Usage**: Check tool definitions in Antigravity prompt

4. **Design Guidelines**: Follow design aesthetics in Antigravity for web apps

## Related Files

- Various Gemini model configurations
- Integration-specific prompts
- CLI system prompts
