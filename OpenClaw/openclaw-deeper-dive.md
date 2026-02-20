---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

---

# OpenClaw Deeper Dive

Source: OpenClaw – open-source AI coding assistant. Custom system prompt per run; no default prompt; compact, modular structure.

## Overview

OpenClaw builds a **custom system prompt for every agent run**. The prompt is OpenClaw-owned (no single “default” prompt), intentionally **compact**, and composed of **fixed sections** plus **injected bootstrap files**. Different **prompt modes** (none, minimal, full) control how much context is included, e.g. for main agent vs sub-agents.

## System Prompt Structure (Fixed Sections)

| Section | Purpose |
|--------|---------|
| **Reasoning** | Current visibility level; hint for /reasoning toggle |
| **Runtime** | Host, OS, Node version, model, repo root, thinking level |
| **Heartbeats** | Heartbeat prompt and how to acknowledge |
| **Reply Tags** | Optional reply syntax for supported providers |
| **Current Date & Time** | User-local time, timezone, format |
| **Sandbox** | Sandboxed runtime details when enabled |
| **Workspace Files** | Indicates which bootstrap files were injected |
| **Documentation** | Local path to OpenClaw docs |
| **Workspace** | Working directory location |
| **OpenClaw Self-Update** | How to update config and OpenClaw itself |
| **Skills** | How to load skill instructions on demand |
| **Safety** | Guardrails to avoid power-seeking behavior |
| **Tooling** | Current tool list with descriptions |

Sections are kept short; detail lives in bootstrap files and on-demand skills.

## Prompt Modes

| Mode | Use case | Content |
|------|----------|---------|
| **none** | Base identity only | Minimal system prompt; only base identity |
| **minimal** | Sub-agents | Omits Skills, Memory Recall, and other heavy sections to keep context small; optimized for sub-agent execution |
| **full** (default) | Main agent | All sections; complete system prompt and maximum functionality |

Choose **minimal** for sub-agents to reduce tokens and latency; **full** for the primary agent.

## Injected Bootstrap Files (Project Context)

These workspace files are **trimmed and injected on every turn** and count toward token usage:

| File | Typical role |
|------|-------------------|
| **MEMORY.md** | Memory and context information |
| **BOOTSTRAP.md** | Bootstrap configuration |
| **HEARTBEAT.md** | Heartbeat instructions |
| **USER.md** | User information |
| **IDENTITY.md** | Agent identity |
| **TOOLS.md** | Tool definitions |
| **SOUL.md** | Core behavior guidelines |
| **AGENTS.md** | Agent configuration |

### Size Limits

- **Per file**: 20,000 characters max  
- **Total**: 150,000 characters max (default)  
- Files are trimmed as needed; injection happens every turn, so large bootstrap sets consume tokens continuously.

## Skills

- Skills provide extra instructions (workflows, conventions, domain knowledge).
- Loaded **on demand** to avoid bloating the base prompt; the **Skills** section explains how to load them.
- Keeps the main prompt compact while allowing optional depth.

## Safety

- **Safety** section includes guardrails to avoid **power-seeking behavior** and to keep tool use and autonomy within intended bounds.
- Complements tool access and sandbox settings.

## Tooling

- The **Tooling** section contains the **current tool list with descriptions** for the run (read, edit, run, search, etc.).
- Tool set can vary by run; the prompt is built with the actual tools available so the agent knows what it can call.

## Summary Table

| Aspect | Detail |
|--------|--------|
| **Ownership** | OpenClaw-owned prompt per run; no default prompt |
| **Structure** | Fixed sections (reasoning, runtime, heartbeats, reply tags, date/time, sandbox, workspace files, docs, workspace, self-update, skills, safety, tooling) |
| **Modes** | none (identity only), minimal (sub-agents), full (default) |
| **Bootstrap** | MEMORY, BOOTSTRAP, HEARTBEAT, USER, IDENTITY, TOOLS, SOUL, AGENTS |
| **Limits** | 20k chars/file; 150k total (default); trimmed each turn |
| **Skills** | On-demand loading to keep context small |
| **Safety** | Guardrails against power-seeking behavior |

## References

- **Main prompt summary**: `openclaw.md`
- **Guide**: `guides/OpenClaw.md`
- OpenClaw project (open-source AI coding assistant)
