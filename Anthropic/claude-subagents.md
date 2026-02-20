---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

# Claude Subagents System Prompt

Source: Anthropic Claude Code - Subagents Documentation

## Overview

Subagents are specialized AI assistants within Claude Code that handle specific task types. Each subagent runs in its own context window with a custom system prompt, specific tool access, and independent permissions.

## Key Benefits

- **Control costs**: Route tasks to faster, cheaper models like Haiku
- **Specialize behavior**: Focused system prompts for specific domains
- **Reuse configurations**: Share configurations across projects
- **Enforce constraints**: Limit tool access to reduce unintended actions
- **Preserve context**: Isolate exploration from main conversation

## Built-in Subagents

Claude Code includes several pre-built subagents:

### Explore
- Fast, read-only agent for codebase search and analysis
- Uses Haiku model for speed and cost efficiency
- Ideal for: Codebase exploration, finding files/functions, understanding project structure

### Plan
- Research agent used during plan mode
- Gathers context before presenting plans
- Ideal for: Pre-implementation research, requirement gathering

### General-purpose
- Capable agent for complex, multi-step tasks
- Requires both exploration and action capabilities
- Ideal for: Multi-step implementations, complex refactoring

## Custom Subagents

You can create custom subagents by defining configuration with frontmatter fields including:

- **Description**: What the subagent does
- **Model selection**: Which Claude model to use (Haiku, Sonnet, Opus)
- **Tool restrictions**: Which tools the subagent can access
- **Permission modes**: Read-only vs. read-write access

Claude automatically delegates to subagents based on their descriptions when appropriate.

## Subagent Configuration

Subagents can be defined three ways:

1. **Built-in general-purpose**: Default subagent for complex tasks
2. **Filesystem-based**: Markdown files with frontmatter configuration
3. **Programmatically**: Via the `agents` parameter in the SDK

## Usage Guidelines

- Use subagents for focused tasks with results reporting back to the main agent
- Subagents run within a single session
- Multiple subagents can run concurrently to speed up workflows
- Each subagent maintains its own context window
- Tool access can be restricted per subagent

## When to Use Subagents

**Use subagents when:**
- You need to parallelize independent tasks
- You want to protect the main context from information overload
- Tasks require specialized expertise or tools
- You need cost optimization (using Haiku for simple tasks)

**Don't use subagents when:**
- Tasks require coordination with the main conversation
- You need to share context between multiple agents
- The task is simple enough for direct execution
