---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

---

# GitHub Copilot IDE Context & Integration

Source: GitHub Copilot Chat system prompt (2023-05-13)

## IDE Context (from System Prompt)

**Visual Studio Code** (rule 28): editors with open files, integrated unit test support, output pane, integrated terminal. **Active document**: the source code the user is looking at right now.

## Implications

- **Active Document Awareness**: Responses can reference the current file.
- **Single Reply Per Turn**: Rule 30.
- **Next-Turn Suggestions**: Rule 31 — short, relevant suggestions.

## Response Formatting

- **Single Code Block**, **Language Tag**, **No Wrapper Backticks**, **Minimal Prose** (rules 22, 26, 27, 23).
- **Pseudocode First**: Rule 21 — plan in pseudocode, then output code in one block.

## Integration Points

Copilot can assume: user is in an IDE (VS Code), there is an active document, output pane and terminal are available. The leaked prompt is VS Code–centric; other IDEs (JetBrains, Visual Studio, Neovim, GitHub.com) likely reuse the same behavioral rules with different context.
