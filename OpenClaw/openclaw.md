---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

📚 **Deeper dive:** See [openclaw-deeper-dive.md](./openclaw-deeper-dive.md) for structure, modes, bootstrap files, skills, safety, and summary table.

# OpenClaw System Prompt

Source: OpenClaw - Open Source AI Coding Assistant

## Overview

OpenClaw builds a custom system prompt for every agent run that is OpenClaw-owned and does not use a default prompt. The system prompt is intentionally compact and includes fixed sections.

## Structure

The system prompt includes the following sections:

- **Reasoning**: current visibility level and /reasoning toggle hint
- **Runtime**: host, OS, node, model, repo root, and thinking level
- **Heartbeats**: heartbeat prompt and acknowledgment behavior
- **Reply Tags**: optional syntax for supported providers
- **Current Date & Time**: user-local time, timezone, and format
- **Sandbox**: sandboxed runtime details (when enabled)
- **Workspace Files**: indicates injected bootstrap files
- **Documentation**: local path to OpenClaw docs
- **Workspace**: working directory location
- **OpenClaw Self-Update**: instructions for config and updates
- **Skills**: how to load skill instructions on demand
- **Safety**: guardrails to avoid power-seeking behavior
- **Tooling**: current tool list with descriptions

## Prompt Modes

OpenClaw can render different system prompts based on runtime context:

- **none**: returns only base identity
- **minimal**: used for sub-agents; omits Skills, Memory Recall, and other sections to keep context small
- **full** (default): includes all sections

## Injected Bootstrap Files

By default, OpenClaw injects workspace files under Project Context, including:

- MEMORY.md
- BOOTSTRAP.md
- HEARTBEAT.md
- USER.md
- IDENTITY.md
- TOOLS.md
- SOUL.md
- AGENTS.md

These files are trimmed and injected on every turn, consuming tokens. File sizes are capped at:
- 20,000 characters per file
- 150,000 characters total by default
