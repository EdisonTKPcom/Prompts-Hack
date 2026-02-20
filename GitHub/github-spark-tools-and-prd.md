---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

---

# GitHub Spark: Tools, Workflow & PRD Framework

Source: GitHub Spark system prompt (Applications Guide, ~30K characters, August 2025)

## Overview

GitHub Spark is a web coding playground that generates runnable "sparks" (micro-apps). The system prompt defines task workflow, tool usage, and a Product Requirements Document (PRD) framework. Sparks are treated as production-ready apps: no placeholders or TODOs.

## Task Workflow (Recommended Steps)

1. **Use search tools** to understand the codebase and the user's query. Use them extensively, in parallel and sequentially, especially when starting or when there is no project context.
2. **Implement** the solution using all tools available.
3. **Working directory**: You are given a working directory via `PWD`. All tool usage in `str_replace_editor` must use **absolute paths** prefixed with this directory.
4. **Current file contents**: You are given "Current file contents" for the core files that already exist (with filler). Assume **all shadcn components** are installed in `@/components/ui` and do not need to be created or modified. Other files are a standard **Vite** default project.
5. **Previous prompts**: You may receive `previousPrompts` (already satisfied requests). If empty, there are no prior user queries.

**Constraint**: Sparks are real applications for production. They must be complete at every stage—no boilerplate placeholders or "todos." Finish the feature fully or do not include it.

## Tool: str_replace_editor

- Used for editing files.
- **Paths**: Must use **absolute paths** to files, prefixed with the given `PWD`.
- Implies a single, coherent edit or set of edits per call (replace blocks of content).

## Tool: Search Tools

- Used to understand the codebase and the user's query.
- Encouraged to be used **extensively**, in parallel and sequentially.
- Critical when starting or when there is no context.

(Other tools may exist—e.g. file read, run, etc.—but the prompt explicitly names search tools and `str_replace_editor` in the workflow.)

## Environment Assumptions

- **Framework**: Default is a **Vite** project.
- **UI**: **shadcn** components in `@/components/ui`; assume installed, do not create or modify.
- **Core files**: Provided as "Current file contents"; may include filler that can be replaced.

## PRD Framework (Product Requirement Documents)

The prompt requires generating and maintaining **PRDs** with:

- **Mission, success metrics, and user experience qualities**
- **Feature selection** based on specific problems and **pivotal user interactions** (key journeys to the goal)
- **WCAG AA** accessibility compliance

### What the PRD Covers

- **Product level**: Mission, success metrics, UX qualities.
- **Feature level**: Which features to build, tied to problems and pivotal interactions.
- **Compliance**: WCAG AA.

### What the Prompt Omits (Notable Omissions)

- Business objectives, strategic concerns, product–market fit
- Target market, users, personas
- Go-to-market plans
- Governance, policy, enterprise requirements
- Infrastructure (orchestration, cost, etc.)

So Spark’s "PRD" is scoped to **product/UX and accessibility**, not full business or infra planning—aligned with "micro-apps" and rapid prototyping.

## Token Budget (Reported)

The full Spark prompt is ~30,000 characters (~7,500 tokens). Public analyses suggest a large share of the token budget is spent on:

- **Design philosophy** (principles, typography, color, space, human interface)
- **Communication rules** (brevity, task focus, file-operation clarity, no fluff)
- **Task and tool workflow** (steps above, PWD, str_replace_editor, search)
- **PRD requirements** (mission, metrics, features, WCAG AA)

So the "Applications Guide" functions as both **job description** and **design + implementation playbook**.

## Summary

| Area | Content |
|------|--------|
| **Workflow** | Search → Implement with tools → Use PWD and absolute paths in str_replace_editor; assume Vite + shadcn. |
| **Completeness** | No placeholders or TODOs; finish features fully or omit them. |
| **PRD** | Mission, success metrics, UX qualities; features from problems and pivotal interactions; WCAG AA. |
| **Omissions** | Business strategy, personas, GTM, governance, infrastructure. |
| **Tools** | Search tools (extensive use); str_replace_editor (absolute paths from PWD). |
