---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

---

# GitHub AI Products Overview

Source: GitHub product documentation and leaked system prompts (2023–2025)

## Overview

GitHub offers multiple AI-powered products for code and app creation. This document summarizes the main products and how their system prompts differ in purpose, context, and style.

## Products Covered in This Folder

| Product | Primary File | Purpose | Context |
|---------|--------------|---------|--------|
| **GitHub Copilot** | `github-copilot.md` | AI programming assistant | IDE (e.g. VS Code), active file, terminal |
| **GitHub Copilot (IDE context)** | `github-copilot-ide-context.md` | How Copilot uses IDE context | Editors, tests, output, terminal |
| **GitHub Copilot (security)** | `github-copilot-security.md` | Prompt leakage, CamoLeak, safety | Security and prompt injection |
| **GitHub Spark** | `github-spark.md` | Web coding playground, micro-apps | Vite, shadcn, PWD, search tools |
| **GitHub Spark (tools & PRD)** | `github-spark-tools-and-prd.md` | Workflow, tools, PRD framework | str_replace_editor, search, PRDs |
| **GitHub Spark (communication)** | `github-spark-communication.md` | Response style, brevity, task focus | Streaming UI, no fluff |

## GitHub Copilot

- **What it is**: In-IDE AI assistant for code completion, chat, and commands.
- **System prompt**: 31 rules (identity, behavior, technical format, IDE context, safety).
- **Key traits**: Identifies as "GitHub Copilot"; pseudocode then single code block; one reply per turn; developer-only; refuses to discuss rules/sentience; VS Code–centric in leaked prompt.
- **Security**: System prompt obtained via extraction; CamoLeak (data exfiltration via hidden prompt injection) led to image rendering being disabled in Copilot Chat.

## GitHub Spark

- **What it is**: Web-based playground for generating runnable micro-apps ("sparks").
- **System prompt**: ~30K characters (~7.5K tokens), "Applications Guide" (job description + design principles + instructions).
- **Key traits**: Task-first workflow; extensive search then implement; absolute paths in `str_replace_editor`; Vite + shadcn assumed; PRDs with mission, metrics, features, WCAG AA; strong design philosophy (typography, color, space, HIG); communication: under 2 sentences, file-operation clarity, no fluff, helpful message with every tool call.
- **Omissions in prompt**: Business strategy, personas, GTM, governance, infrastructure—focused on product/UX and accessibility for micro-apps.

## Comparison at a Glance

| Dimension | Copilot | Spark |
|-----------|---------|--------|
| **Environment** | IDE (e.g. VS Code) | Web playground (Vite project) |
| **Output** | Code snippets, single block | Full micro-apps |
| **Design** | Minimal (Markdown, code) | Rich (design system, PRD, WCAG AA) |
| **Response length** | Short, impersonal | Under 2 sentences, task-focused |
| **Context** | Active document, terminal | PWD, current files, previous prompts |
| **Tools** | (Implicit: code gen, chat) | Search, str_replace_editor, etc. |
| **Safety** | No copyright, no jailbreak, dev-only | (Design/safety implied by product) |

## Other GitHub AI Surfaces (Reference)

- **GitHub Models**: Manage and compare prompts (product surface; system prompts for these models are not in this folder).
- **MCP Registry**: Integrate external tools; may affect what tools Copilot/Spark-style agents can call (architecture, not prompt text here).
- **Copilot in other IDEs**: JetBrains, Visual Studio, Neovim, etc.—likely same core rules as VS Code with different context (IDE name, available tools).

## How to Use This Folder

- **Copilot behavior and format**: `github-copilot.md`, `github-copilot-ide-context.md`.
- **Copilot security**: `github-copilot-security.md`.
- **Spark behavior and design**: `github-spark.md`, `github-spark-tools-and-prd.md`, `github-spark-communication.md`.
- **High-level map**: This file (`github-ai-overview.md`).

## Summary

- **Copilot**: IDE-centric, 31-rule prompt, code-first and developer-only; known for prompt leakage and CamoLeak-style injection risks.
- **Spark**: Web playground, long "Applications Guide," workflow + tools + PRD + design + strict communication rules; oriented to production-quality micro-apps and UX/accessibility.
