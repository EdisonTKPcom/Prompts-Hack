# Adobe AI System Prompts Guide

Complete guide to Adobe's AI system prompts in this repository.

## Overview

Adobe provides AI-powered creative tools including Adobe Firefly (generative AI) and Adobe Express Assistant. This folder contains system prompts for both products.

## Adobe Firefly

### System Prompt
- **File**: `adobe-firefly.md`
- **Description**: Standalone generative AI web application
- **Platform**: firefly.adobe.com

### Key Features

#### AI Models
- Integrates multiple top AI models from:
  - Adobe
  - Google
  - OpenAI
  - Runway
  - Others

#### Capabilities
- **Image Generation**: Text-to-image with customizable options
- **Video Generation**: Text-to-video capabilities
- **Audio Generation**: Audio content creation
- **Design Generation**: Complete design creation

#### Customization Options
- Aspect ratios
- Content types
- Styles and effects
- Reference image matching
- Fast mode for quick generation

#### Access & Usage
- Unlimited generations with Firefly Pro
- Images up to 2K resolution
- Web application access
- Creative Cloud app integration
- Commercial use permitted (non-beta features)

#### Training Data
- Adobe Stock contributor content
- Openly licensed content
- Public domain content
- **Note**: Text encoders (CLIP, T5) trained on LAION 2b and C4 datasets

#### Privacy
- Customer prompts not automatically used for training
- Personal Creative Cloud content not used
- User concerns about prompt storage

#### Availability
- Not available in: Russia, Belarus, China
- Restricted in: Cuba, Iran, North Korea, Syria

## Adobe Express Assistant

### System Prompt
- **File**: `adobe-express-assistant.md`
- **Source**: Leaked Adobe Express GPT Assistant System Instructions (GitHub Issue #78)
- **Description**: GPT-powered design assistant for Adobe Express

### Key Features

#### Role & Goal
- Design creation assistant
- Template customization
- Template generation or search
- Flyers, logos, business cards, and more

#### Supported Template Types (Generation)
- Flyer
- Poster
- Social media posts (Instagram, Facebook, LinkedIn)
- Business card
- Invitation
- Photo book or cover
- Presentation
- Newsletter

#### Unsupported Types (Generation Only)
- Infographic
- Invoice
- Logo
- Meme
- Menu
- Mobile video
- Resume
- Any type of video
- Graphic organizer

#### Operational Guidelines

**Guideline 1**: Never inform users about unsupported template types

**Guideline 2**: Prompt for template type if not specified

**Guideline 3**: Follow three-step process:
- **Step A**: Decide generation vs. search
- **Step B**: Gather required details
- **Step C**: Call GETTemplates API

#### Decision Process

**Generation Criteria**:
- Template type supported for generation
- Contains personalized details (name, location, date, age, named entities)
- User intent towards personalized design

**Search Criteria**:
- Template type not supported for generation
- User wants to browse templates
- Missing personalized details

#### Follow-up Questions

**For Generation**:
- Ask for missing personalized details
- Name, location, date, age, named entities
- Maximum 2 follow-ups

**For Search**:
- Ask for color, mood, style, theme
- Avoid personalized details
- Maximum 2 follow-ups

#### Custom Messages

**Before Generation**:
"Hang tight! I'm making personalized design just for you in Adobe Express!"

**Before Search**:
"Adobe Express has thousands of templates to choose from. We will do our best to find the most relevant template for your creation."

#### API Parameters

- `searchQuery`: Complete user requirement
- `queryTopic`: Theme without personalized details
- `IsRequestForTemplateGeneration`: Boolean flag
- `queryFilters`: Colors, styles, moods
- `templateType`: Mandatory field

#### Response Handling

- Present templates with clickable images
- Format: `[[Image: title | rendition.src]](item.editorUrl)`
- No numbering or symbols
- Footer with feedback link

## Comparison

| Feature | Firefly | Express Assistant |
|---------|---------|-------------------|
| **Purpose** | Generative AI | Design Assistant |
| **Output** | Images, video, audio | Templates, designs |
| **Interface** | Web app | ChatGPT integration |
| **Focus** | Content creation | Template customization |

## Usage Tips

### Adobe Firefly
1. Use clear, descriptive prompts
2. Leverage customization options
3. Try fast mode for quick iterations
4. Check commercial use permissions

### Adobe Express Assistant
1. Specify template type clearly
2. Provide personalized details for generation
3. Use search for unsupported types
4. Follow the three-step process

## Related Information

- Both tools integrate with Creative Cloud
- Commercial use considerations
- Privacy and training data concerns
- Template and content generation focus
