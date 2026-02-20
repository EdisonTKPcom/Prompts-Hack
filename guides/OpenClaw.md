# OpenClaw System Prompts Guide

Complete guide to OpenClaw AI coding assistant system prompts.

## Overview

OpenClaw is an open-source AI coding assistant that builds custom system prompts for every agent run. It uses a modular, compact system prompt structure.

- **Deeper dive**: `openclaw-deeper-dive.md` – fixed sections, prompt modes (none/minimal/full), bootstrap files and limits, skills, safety, tooling, summary table.

## System Prompt Architecture

### File
- **File**: `openclaw.md`
- **Description**: OpenClaw AI coding assistant system prompt

### Key Features

#### Custom System Prompts
- Builds custom system prompt for every agent run
- OpenClaw-owned (no default prompt)
- Intentionally compact structure

### System Prompt Sections

#### Fixed Sections

1. **Reasoning**
   - Current visibility level
   - /reasoning toggle hint

2. **Runtime**
   - Host information
   - Operating system
   - Node version
   - Model information
   - Repository root
   - Thinking level

3. **Heartbeats**
   - Heartbeat prompt
   - Acknowledgment behavior

4. **Reply Tags**
   - Optional syntax for supported providers

5. **Current Date & Time**
   - User-local time
   - Timezone
   - Format

6. **Sandbox**
   - Sandboxed runtime details (when enabled)

7. **Workspace Files**
   - Indicates injected bootstrap files

8. **Documentation**
   - Local path to OpenClaw docs

9. **Workspace**
   - Working directory location

10. **OpenClaw Self-Update**
    - Instructions for config and updates

11. **Skills**
    - How to load skill instructions on demand

12. **Safety**
    - Guardrails to avoid power-seeking behavior

13. **Tooling**
    - Current tool list with descriptions

## Prompt Modes

### None Mode
- Returns only base identity
- Minimal system prompt

### Minimal Mode
- Used for sub-agents
- Omits Skills, Memory Recall, and other sections
- Keeps context small
- Optimized for sub-agent execution

### Full Mode (Default)
- Includes all sections
- Complete system prompt
- Maximum functionality

## Injected Bootstrap Files

### Default Files
By default, OpenClaw injects workspace files under Project Context:

- **MEMORY.md**: Memory and context information
- **BOOTSTRAP.md**: Bootstrap configuration
- **HEARTBEAT.md**: Heartbeat instructions
- **USER.md**: User information
- **IDENTITY.md**: Agent identity
- **TOOLS.md**: Tool definitions
- **SOUL.md**: Core behavior guidelines
- **AGENTS.md**: Agent configuration

### File Size Limits
- **Per File**: 20,000 characters maximum
- **Total**: 150,000 characters maximum
- Files are trimmed and injected on every turn
- Consumes tokens per injection

## Key Characteristics

### Modular Design
- Compact, structured sections
- Progressive disclosure
- On-demand skill loading

### Context Management
- File size limits prevent overload
- Trimming and injection system
- Token consumption awareness

### Safety Focus
- Guardrails against power-seeking
- Safety guidelines
- Controlled tool access

## Usage Tips

1. **Prompt Mode**: Choose based on use case (minimal for sub-agents, full for main agent)
2. **Bootstrap Files**: Understand what gets injected
3. **File Limits**: Be aware of size constraints
4. **Skills**: Load skills on demand to optimize context

## Deeper Dive

- **File**: `openclaw-deeper-dive.md`
- **Contents**: Full structure table (reasoning, runtime, heartbeats, reply tags, date/time, sandbox, workspace files, docs, workspace, self-update, skills, safety, tooling); prompt modes (none, minimal, full) and when to use each; bootstrap file roles and size limits (20k/file, 150k total); on-demand skills; safety guardrails; summary table.

## Related Information

- Open-source AI coding assistant
- Modular system prompt architecture
- Focus on efficiency and safety
- Customizable for different use cases
