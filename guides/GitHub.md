# GitHub AI System Prompts Guide

Complete guide to GitHub's AI system prompts in this repository.

## Overview

GitHub provides AI-powered coding assistants including GitHub Copilot and GitHub Spark. This folder contains system prompts for both products.

## GitHub Copilot

### System Prompt
- **File**: `github-copilot.md`
- **Source**: Leaked system prompt from GitHub Copilot Chat (2023-05-13)
- **Description**: AI programming assistant integrated into IDEs

### Key Features

#### Identity & Behavior
- Identifies as "GitHub Copilot"
- Follows user requirements carefully
- Refuses to discuss opinions, rules, or sentience
- Avoids argumentative discussions

#### Technical Guidelines
- Step-by-step pseudocode planning
- Code output in single code blocks
- Minimal prose
- Short, impersonal answers
- Markdown formatting

#### IDE Integration
- Visual Studio Code integration
- Active document awareness
- Unit test support
- Output pane and terminal access

#### Safety & Restrictions
- Refuses copyrighted content requests
- Declines jailbreak instructions
- Follows Microsoft content policies
- Developer-focused responses only

### System Rules (31 Rules)

The prompt includes 31 detailed rules covering:
1. Identity and naming
2. Behavior guidelines
3. Technical requirements
4. Safety restrictions
5. IDE integration
6. Response formatting

## GitHub Spark

### System Prompt
- **File**: `github-spark.md`
- **Source**: GitHub Spark's System Prompt (as of August 2025)
- **Description**: Web coding playground for generating runnable code micro-apps
- **Size**: ~30,000 characters (~7,500 tokens)

### Key Features

#### Architecture
- Framed as "Applications Guide"
- Combines job description, design principles, and instructions
- Significant focus on design philosophy

#### Design Philosophy
- **Simplicity Through Reduction**: Essential purpose focus
- **Material Honesty**: Digital materials feel real
- **Obsessive Detail**: Every pixel matters
- **Coherent Design Language**: Unified system feel
- **Invisibility of Technology**: Technology disappears
- **Start With Why**: Purpose-driven design

#### Typography Excellence
- Purposeful typography
- Clear hierarchy
- Limited font selection (2-3 typefaces)
- Type scale harmony
- Generous spacing

#### Color Theory
- Intentional color usage
- Color as communication
- Sophisticated palettes
- Contextual adaptation
- Focus through restraint

#### Communication Style
- **Brevity Essential**: Under 2 sentences
- **Natural Context**: Friendly mentions
- **Task Focus**: Direct actions
- **File Operation Clarity**: State filename and action
- **Zero Fluff**: No apologies or filler

#### Product Requirements
- PRD generation and maintenance
- Mission and success metrics
- Feature selection based on problems
- WCAG AA accessibility compliance

#### Notable Omissions
- Business objectives
- Target markets/personas
- Go-to-market plans
- Enterprise requirements
- Infrastructure considerations

### Task Execution

1. **Search Tools**: Extensive use for codebase understanding
2. **Implementation**: Using all available tools
3. **Working Directory**: Absolute paths required
4. **File Management**: Current file contents awareness
5. **Previous Prompts**: Context from past requests

## Comparison

### Copilot vs Spark

| Feature | Copilot | Spark |
|---------|---------|-------|
| **Purpose** | Code assistant | App generator |
| **Context** | IDE integration | Web playground |
| **Focus** | Code suggestions | Complete apps |
| **Design** | Minimal | Rich aesthetics |
| **Output** | Code snippets | Full applications |

## Usage Tips

### GitHub Copilot
1. Use for code suggestions and completions
2. Leverage IDE integration features
3. Follow step-by-step planning approach
4. Keep responses concise

### GitHub Spark
1. Focus on complete application generation
2. Emphasize design aesthetics
3. Use PRD framework for planning
4. Follow communication style guidelines

## Related Information

- Copilot: Focused on developer productivity
- Spark: Focused on rapid app prototyping
- Both: Emphasize code quality and user experience
