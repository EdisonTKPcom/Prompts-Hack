---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. It summarizes publicly documented Cursor IDE behavior and configuration. Cursor is a product of Cursor, Inc. This repository is not affiliated with or endorsed by Cursor.

---

# Cursor IDE Deeper Dive

Source: Cursor documentation, public guides, and common usage. Cursor’s full system prompt is not disclosed here; this doc covers **rules**, **agent behavior**, and **context** as documented and observed.

## Overview

Cursor is an AI-powered code editor (VS Code–based) that provides inline chat, Composer (agent mode), and context-aware coding. The AI receives **rules** (persistent instructions), **codebase context** (open files, @-mentions, codebase index), and **tools** (read, edit, terminal, search, MCP). This deeper dive focuses on how instructions and context are supplied rather than the exact internal system prompt.

## Rules System

Persistent instructions are merged into the model’s context so the AI follows project- or user-specific guidance without repeating it every time.

### Rule Types

| Type | Location | Scope |
|------|----------|--------|
| **Project rules** | `.cursor/rules/` (`.md` or `.mdc`) | Repo; version-controlled |
| **User rules** | Cursor settings (global) | All chats and Agent usage |
| **Team rules** | Dashboard (Team/Enterprise) | Whole team |
| **AGENTS.md** | Project root | Simple markdown instructions for the agent |
| **Legacy** | `.cursorrules` (single file) | Deprecated in favor of `.cursor/rules/` |

### Activation

Rules can be applied in four ways:

- **Always apply** – Every chat and file interaction.
- **Auto-attached** – When the agent (or context) touches files matching a glob (e.g. `**/*.ts`).
- **Agent-decided** – Model uses rule description to decide when to include it.
- **Manual** – Only when the user references with `@rule-name` (or equivalent).

### Precedence (when rules conflict)

1. Team rules (highest)
2. Project rules (`.cursor/rules/`)
3. User rules
4. Legacy (`.cursorrules`)
5. AGENTS.md

### File formats

- **.md** – Plain markdown; activation depends on rule type/settings.
- **.mdc** – Markdown with YAML frontmatter for activation type, globs, and descriptions.

## Agent (Composer) Behavior

- **Composer / Agent** – Multi-step task execution: plan, read/edit files, run commands, search codebase.
- **Tools** – The agent typically has access to: read file, read many files, search replace, write, grep, glob, list dir, run shell command, and (optionally) MCP tools. Exact tool set and names are implementation-defined.
- **Context** – Current file, @-mentioned files/folders, codebase index, and active rules.
- **Best practices (documented)** – Prefer project conventions; verify libraries exist before use; use absolute paths where required; run tests/lint after changes; avoid unnecessary comments; be concise in chat.

## MCP (Model Context Protocol)

- **MCP servers** – External tools (databases, APIs, custom scripts) can be exposed to the agent via MCP.
- **Tool descriptors** – Stored as JSON (e.g. in an mcps folder or server config); the agent receives tool name, parameters, and descriptions.
- **Usage** – Agent calls MCP tools by name with the required arguments; resources (e.g. docs) can be fetched when relevant.

## Skills

- **Agent skills** – Optional, reusable “skills” (e.g. from a skills registry or `.cursor` config) that extend the agent with domain workflows or conventions.
- **Invocation** – Skills can be triggered by user intent or by the agent when a task matches the skill’s description.

## Context and @-mentions

- **@file** – Add a file to context.
- **@folder** – Add a folder (often indexed) to context.
- **@codebase** – Broad codebase context (index/search).
- **@web** / **@docs** – When available, add web or documentation context.
- **@rules** – Reference specific rules.

## Summary Table

| Aspect | Detail |
|--------|--------|
| **Rules** | Project (`.cursor/rules/`), User, Team, AGENTS.md, legacy `.cursorrules` |
| **Activation** | Always, auto (glob), agent-decided, manual (@rule) |
| **Precedence** | Team > Project > User > .cursorrules > AGENTS.md |
| **Agent tools** | Read, edit, write, grep, glob, list_dir, run_terminal_cmd, MCP |
| **Context** | Open file, @-mentions, codebase index, active rules |
| **MCP** | External tools/servers; JSON descriptors; optional resources |
| **Skills** | Optional agent extensions; intent- or task-triggered |

## References

- [Cursor Docs – Rules](https://docs.cursor.com/context/rules)
- [Cursor Docs – Context](https://docs.cursor.com/context)
- Project rules and AGENTS.md in repositories using Cursor
