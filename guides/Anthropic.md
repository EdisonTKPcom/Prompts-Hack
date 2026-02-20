# Anthropic Claude System Prompts Guide

Complete guide to Anthropic's Claude system prompts in this repository.

## Overview

Anthropic's Claude models include Opus, Sonnet, and Haiku variants, each with different capabilities and system prompts. This folder also contains specialized versions like Claude Code and various integrations.

## Model Variants

### Claude Opus 4.6
- **File**: `claude-opus-4.6.md`
- **Description**: Most capable Claude model
- **Features**: Advanced reasoning, long context, tool use
- **Use Cases**: Complex tasks, research, analysis

### Claude Sonnet 4.6
- **File**: `claude-sonnet-4.6.md`
- **Description**: Balanced performance model
- **Features**: Good balance of capability and speed
- **Use Cases**: General tasks, coding, analysis

### Claude Code
- **File**: `claude-code.md`
- **Description**: Specialized coding assistant
- **Features**: Code generation, debugging, refactoring
- **Use Cases**: Software development, code review

## Specialized Versions

### Claude Agent
- **File**: `claude-agent.md`
- **Description**: Agent SDK implementation
- **Features**: Tool use, multi-step tasks, autonomous operation

### Claude Subagents
- **File**: `claude-subagents.md`
- **Description**: Specialized sub-agents
- **Types**: Explore, Plan, General-purpose
- **Use Cases**: Parallel tasks, cost optimization

### Claude Agent Teams
- **File**: `claude-agent-teams.md`
- **Description**: Multi-agent collaboration
- **Features**: Independent sessions, coordination
- **Use Cases**: Complex projects, parallel work

## Integrations

### Claude for Chrome
- **File**: `claude-in-chrome.md`
- **Description**: Browser integration
- **Features**: Web browsing, page analysis

### Claude for Excel
- **File**: `claude-for-excel.md`
- **Description**: Spreadsheet assistant
- **Features**: Data analysis, formula generation

### Claude Cowork
- **File**: `claude-cowork.md`
- **Description**: Desktop app cowork mode
- **Features**: Local execution, workspace access

## Legacy Versions

Located in `old/` folder:
- Claude 3.7 Sonnet
- Claude 4.5 Sonnet
- Claude 4.1 Opus (Thinking)
- Various tool configurations

## Raw Versions

Located in `raw/` folder:
- Unprocessed system prompts
- Original format preservation

## Key Features Across Models

- **Past Chats Tools**: Search previous conversations
- **Tool Usage**: Extensive tool calling capabilities
- **Safety Guidelines**: Content moderation rules
- **Response Behaviors**: Communication style guidelines

## Usage Tips

1. **Model Selection**: Choose Opus for complex tasks, Sonnet for balance, Haiku for speed
2. **Tool Usage**: Check tool definitions in each prompt
3. **Context Management**: Understand context window limits
4. **Safety**: Review safety guidelines for content restrictions

## Related Files

- `claude.ai-injections.md`: Injection techniques
- `default-styles.md`: Default response styles
