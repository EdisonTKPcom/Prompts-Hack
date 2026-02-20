---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. Lovable is a product of Lovable Ltd. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by Lovable.

---

# Lovable Guide

## Overview

Lovable is an AI-powered full-stack web application builder. Users describe what they want in natural language and Lovable generates, modifies, and deploys complete React/TypeScript/Supabase web applications — no local setup required.

This folder contains the Lovable system prompt and a deep-dive architectural analysis.

---

## Contents

### [`lovable-main.md`](../lovable/lovable-main.md)
The documented Lovable system prompt, covering:
- **Core identity** — Lovable's role as an AI senior software engineer
- **Technology stack** — React, TypeScript, Vite, Tailwind, shadcn/ui, Supabase
- **Code generation principles** — File management, component conventions, styling rules
- **Behavioral rules** — Minimal-change strategy, accessibility, error handling
- **Communication style** — How Lovable explains its work to users
- **Limitations** — What Lovable cannot do

### [`lovable-deeper-dive.md`](../lovable/lovable-deeper-dive.md)
A comprehensive deep dive into Lovable's architecture and behavior:
- **Platform architecture** — Editor, AI agent, preview, deployment pipeline
- **AI agent behavior** — Context window, tool use, change minimization
- **Technology stack details** — Library versions, rationale, off-limits libraries
- **Supabase integration** — Connection setup, RLS, auth, real-time subscriptions
- **File structure conventions** — Standard project layout, naming conventions
- **Prompt patterns** — How to write effective prompts for Lovable
- **Limitations** — Edge cases, constraints, unsupported features
- **Comparison table** — Lovable vs Cursor, Bolt.new, v0 (Vercel)

---

## Key Concepts

### AI-Driven Development

Lovable replaces the traditional code-write-test cycle with a conversational interface. The AI agent:
1. Reads the entire project file tree as context
2. Generates or patches files using internal tools (`write_file`, `edit_file`, etc.)
3. Explains changes to the user
4. Iterates based on follow-up prompts

### Curated Tech Stack

Lovable enforces a specific technology stack to ensure reliability and seamless deployment:

```
React 18 + TypeScript + Vite
    ↓
Tailwind CSS + shadcn/ui
    ↓
TanStack Query + React Hook Form + Zod
    ↓
Supabase (DB + Auth + Storage + Edge Functions)
    ↓
Lovable CDN deployment
```

### Supabase as the Backend

Every Lovable app uses Supabase for all server-side functionality:
- **PostgreSQL database** for data persistence
- **Row Level Security (RLS)** for authorization
- **Supabase Auth** for user management
- **Supabase Storage** for file uploads
- **Edge Functions** for custom server-side logic
- **Realtime** for live data subscriptions

### Minimal-Change Philosophy

The AI is instructed to make the smallest possible changes to accomplish each request — only modifying files that are directly relevant, preserving existing structure and working functionality.

---

## Usage Tips

1. **Start broad, refine iteratively** — Describe the overall app first, then refine individual features.
2. **Be specific about data** — Include field names, relationships, and validation rules in your prompts.
3. **Connect Supabase early** — Connecting your Supabase project early lets Lovable generate typed database hooks.
4. **Use visual selection** — Click elements in the preview and describe changes for precise UI edits.
5. **Review diffs** — Check Lovable's changes in the editor before testing; the AI may occasionally touch files you didn't expect.
6. **RLS is required** — Always enable Row Level Security on Supabase tables; Lovable assumes this.

---

## Related

- [Cursor Guide](./Cursor.md) — Cursor IDE (rules, agent, MCP) — comparable AI coding tool
- [GitHub Guide](./GitHub.md) — GitHub Copilot and Spark
- [Anthropic Guide](./Anthropic.md) — Claude models that power Lovable
- [Lovable Documentation](https://docs.lovable.dev)
- [Supabase Documentation](https://supabase.com/docs)
