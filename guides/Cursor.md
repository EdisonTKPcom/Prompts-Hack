# Cursor IDE Guide

Guide to Cursor-related content in this repository.

## Overview

Cursor is an AI-powered code editor (VS Code–based) that uses rules, codebase context, and tools (including MCP) to support inline chat and agent (Composer) mode. This folder does not contain a leaked system prompt; it documents **how Cursor is configured and used** from public documentation and common practice.

## Contents

### Deeper Dive

- **File**: `cursor-deeper-dive.md`
- **Description**: Architecture and behavior of Cursor’s AI context and instructions.
- **Covers**:
  - **Rules system** – Project (`.cursor/rules/`), User, Team, AGENTS.md; activation (always, auto, agent-decided, manual); precedence; .md vs .mdc.
  - **Agent (Composer)** – Tool use (read, edit, grep, glob, terminal, MCP); context (open file, @-mentions, codebase).
  - **MCP** – Model Context Protocol; external tools and resources.
  - **Skills** – Optional agent extensions.
  - **Context and @-mentions** – @file, @folder, @codebase, @rules, etc.
  - Summary table and references.

## Key Concepts

### Rules

- Persistent instructions so the AI follows project or user preferences without repeating them.
- Stored in `.cursor/rules/` (project), user settings (global), or team dashboard.
- AGENTS.md in the project root is a simple way to give the agent high-level instructions.

### Agent Tools

- Read/edit files, search codebase (grep, glob), run terminal commands, and call MCP tools when configured.
- Prefer existing project conventions and verify dependencies before suggesting new ones.

### MCP

- Connect external services (APIs, DBs, custom tools) to the agent via MCP servers and tool descriptors.

## Usage Tips

1. Put project-wide conventions in `.cursor/rules/` or AGENTS.md.
2. Use glob-based or agent-decided rules so only relevant rules are attached.
3. Use @-mentions to pull in specific files or folders when asking the agent to change code.
4. Configure MCP servers for tools the agent should use (e.g. DB, HTTP APIs).

## Related

- **Deeper dive**: [cursor-deeper-dive.md](../Cursor/cursor-deeper-dive.md)
- [Cursor Docs](https://docs.cursor.com)
