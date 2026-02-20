---
description: |
  Daily agent for Prompts-Hack: reviews the system prompts collection, suggests
  sync with upstream (asgeirtj/system_prompts_leaks), and creates a short
  status issue with stats and recommendations.

on:
  schedule: daily
  workflow_dispatch:

permissions:
  contents: read
  issues: read
  pull-requests: read

network: defaults

tools:
  github:
    lockdown: false

safe-outputs:
  create-issue:
    title-prefix: "[prompts-hack] "
    labels: [report, daily]
---

# Daily Prompts-Hack Agent

Run a daily check on the Prompts-Hack repository and open an issue with a brief status report.

## What to include

- Count of markdown files and top-level directories (Anthropic, OpenAI, Google, etc.)
- Any notable new folders or files if you can infer from structure
- Optional: compare with upstream [asgeirtj/system_prompts_leaks](https://github.com/asgeirtj/system_prompts_leaks) and note if sync or new prompts might be useful
- Short, actionable suggestions (e.g. “Consider adding a new leak for X”, “README stats may need updating”)

## Style

- Concise and factual
- Use bullet points; one short paragraph at the top is fine
- No fluff; focus on stats and 1–3 concrete recommendations

## Process

1. Read the repository layout (directories and key files under each provider).
2. Compute or summarize basic stats (file counts, folders).
3. Create a single new GitHub issue with the daily report and recommendations.
