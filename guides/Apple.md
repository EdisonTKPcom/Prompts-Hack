# Apple Creator Studio System Prompts Guide

Complete guide to Apple Creator Studio AI system prompts.

## Overview

Apple Creator Studio is a subscription suite launched in January 2026 that includes creative apps with integrated AI features powered by Apple Intelligence. The AI is designed as an assistive tool to aid creators rather than replace them.

## Apple Creator Studio

### System Prompt
- **File**: `apple-creator-studio.md`
- **Description**: Main Creator Studio suite with AI features
- **Launch**: January 2026
- **Pricing**: $12.99/month or $129/year (general), $2.99/month or $29.99/year (students/educators)

### Included Apps

#### Video Production
- Final Cut Pro
- Motion
- Compressor

#### Music Production
- Logic Pro
- MainStage

#### Image Editing
- Pixelmator Pro

#### Productivity Apps (with exclusive AI features)
- Keynote
- Pages
- Numbers
- Freeform

### AI Features

#### Image Generation
- Location: Pages and Pixelmator Pro
- Method: Detailed text descriptions
- Style options: Animation, Illustration
- Capabilities: Combine up to seven elements
- Super Resolution: Increase image clarity

#### Video Editing Assistance
- Visual Search: Find shots without scrubbing
- Transcript Search: Locate dialogue via keywords
- Beat Detection: Sync clips to music rhythm
- Camera Angle Changes: AI-assisted editing

#### Music Creation
- Synth Player: Music synthesis
- Chord ID: Extract chord progressions from reference tracks

#### Presentation Generation
- Keynote: Auto-assembling slideshows from notes
- Presenter Notes: Generate presenter notes automatically

### Usage Limits

Monthly limits:
- 50 generated images per month
- 50 presentations (8-10 slides each) per month
- 700 presenter notes per month

Limits vary based on query complexity and server availability, resetting monthly.

## Apple Creator Studio Pro

### System Prompt
- **File**: `apple-creator-studio-pro.md`
- **Description**: Professional version with enhanced capabilities
- **Launch**: January 2026

### Enhanced Features

- Advanced AI features for professional workflows
- Higher usage limits (if applicable)
- Priority processing
- Extended support

## Key Principles

### Assistive AI Philosophy
- **Augmentation over Automation**: AI assists rather than replaces
- **Creator Control**: Preserves authorship and creative control
- **Privacy-Focused**: On-device processing where possible

### Privacy Architecture

#### On-Device Processing
- Visual search
- Transcript search
- Keeps sensitive content local

#### Cloud Processing
- Advanced tasks route through private relays
- Partners include OpenAI
- Apple pledges not to retain user content for model training

## Subscription Details

### Pricing
- **General**: $12.99/month or $129/year
- **Students/Educators**: $2.99/month or $29.99/year

### Family Sharing
- Extends access to up to five additional members
- Shared usage limits

## Integration

All AI features are integrated directly into the creative apps, providing seamless workflow without switching between applications.

## Use Cases

- Professional video production
- Music composition and production
- Image editing and design
- Presentation creation
- Collaborative workflows

## Apple Intelligence System Prompts

### Leaked System Prompts
- **File**: `apple-intelligence-system-prompts.md`
- **Source**: Discovered in macOS 15.1 Developer Beta (August 2024)
- **Content**: Pre-defined instructions for features like Smart Reply and Memories
- **Key Directive**: "Do not hallucinate" - explicit anti-hallucination instructions

### Technical Architecture
- **File**: `apple-intelligence-architecture.md`
- **Source**: Apple Machine Learning Research (2025)
- **Content**: 
  - On-device: ~3B parameter model optimized for Apple Silicon
  - Server: PT-MoE transformer for Private Cloud Compute
  - KV-cache sharing, 2-bit quantization
  - Developer framework with Swift integration

### Preference Ranking Guidelines
- **File**: `apple-preference-ranking-guidelines.md`
- **Source**: Leaked 170-page internal document (January 2025)
- **Content**: Scoring system for AI responses
- **Categories**: Truthfulness, Harmfulness, Conciseness, User Satisfaction
- **Use**: Human reviewer guidelines for Siri/Apple Intelligence

## Image Playground

### System-Wide Image Generation
- **File**: `apple-image-playground.md`
- **Description**: System-wide AI image generation tool
- **Features**: 
  - Text-to-image with style options
  - Up to 7 combinable elements
  - Super Resolution
  - Auto Crop
  - Integration with Pages, Keynote, Messages
- **Backend**: Uses OpenAI for generation
- **Limits**: 50 images/month

## App-Specific Features

### Detailed App Integration
- **File**: `apple-creator-studio-app-specific.md`
- **Content**: Detailed breakdown of AI features per app
- **Pages**: Image generation, writing assistance
- **Keynote**: Presentation generation, presenter notes
- **Final Cut Pro**: Visual search, transcript search, beat detection
- **Logic Pro**: Synth Player, Chord ID
- **Pixelmator Pro**: Image generation, smart cropping, super resolution
- **Numbers**: Data analysis, formula assistance
- **Freeform**: Collaborative AI tools

## Related Information

- Emphasis on creator authorship
- Privacy-first architecture
- Assistive rather than replacement AI
- Integration with Apple ecosystem
- Leaked system prompts reveal anti-hallucination focus
- Technical architecture combines on-device and cloud processing
- Comprehensive evaluation system for AI responses
