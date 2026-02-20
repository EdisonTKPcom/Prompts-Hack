# Workflows

## Daily Update (GitHub Actions)

**File:** `daily-update.yml`

- **Schedule:** Runs daily at 00:05 UTC (`cron: '5 0 * * *'`).
- **Manual:** Trigger via **Actions → Daily Update → Run workflow**.
- **What it does:** Checks out the repo, counts markdown files and top-level directories, and writes the stats to the workflow run **Summary** (no commit).

No secrets required. Uses default `GITHUB_TOKEN` (read-only is enough).

## Daily Agent (GitHub Agentic Workflows)

**File:** `daily-agent.md`

Uses [GitHub Agentic Workflows](https://github.github.io/gh-aw/) (gh-aw) so an **AI agent** runs on a schedule and can open issues with status and recommendations.

- **Schedule:** Daily (fuzzy time when compiled with gh-aw).
- **What it does:** Agent reviews the repo layout, summarizes stats, optionally compares with upstream [asgeirtj/system_prompts_leaks](https://github.com/asgeirtj/system_prompts_leaks), and creates a GitHub issue with a short report.

### Enabling the daily agent

1. **Install gh-aw**
   ```bash
   gh extension install github/gh-aw
   ```

2. **Compile the workflow** (from repo root)
   ```bash
   gh aw compile
   ```
   This generates the YAML that Actions runs from the `.md` file.

3. **Add an AI provider secret** (one of):
   - `COPILOT_GITHUB_TOKEN` (GitHub Copilot)
   - `ANTHROPIC_API_KEY` (Claude)
   - `OPENAI_API_KEY` (OpenAI)

4. **Commit and push** the compiled workflow (and any lock file) under `.github/workflows/`.

5. **Run once manually** (optional):
   ```bash
   gh aw run daily-agent
   ```

See [Quick Start – GitHub Agentic Workflows](https://github.github.io/gh-aw/setup/quick-start/) and [Scheduled Workflows](https://github.github.io/gh-aw/examples/scheduled/) for details.
