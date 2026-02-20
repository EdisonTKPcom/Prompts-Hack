---
**FAIR USE NOTICE**: This content is provided for educational and research purposes only. System prompts are publicly disclosed/leaked information. All trademarks belong to their respective owners. This repository is not affiliated with or endorsed by any company.

# Claude Agent Teams System Prompt

Source: Anthropic Claude Code - Agent Teams Documentation

## Overview

Agent teams coordinate multiple Claude Code instances working together (currently experimental). Unlike subagents, teammates work independently in separate sessions and can communicate directly with each other.

## Key Differences: Subagents vs. Agent Teams

### Subagents
- Work within a single session
- Share the same context window
- Report results back to the main agent
- Best for: Focused tasks with results reporting back

### Agent Teams
- Work in separate sessions
- Independent context windows
- Can communicate directly with each other
- Best for: Collaborative work requiring coordination

## When to Use Agent Teams

Agent teams are most effective for:

### Cross-layer Coordination
- Spanning frontend, backend, and tests
- Multiple components need simultaneous work
- Different teammates handle different layers

### Parallel Debugging
- Testing competing hypotheses in parallel
- Multiple debugging approaches simultaneously
- Isolating issues across different code paths

### New Feature Development
- Teammates can work independently on different parts
- Parallel implementation of related features
- Coordinated feature rollout

### Research Tasks
- Simultaneous investigation of different aspects
- Parallel exploration of multiple solutions
- Coordinated research across domains

## Team Coordination

Agent teams can:
- Share findings with each other
- Coordinate on implementation decisions
- Self-organize task distribution
- Communicate directly without main agent mediation

## Configuration

Agent teams are configured to work in separate Claude Code sessions, allowing for:
- Independent context management
- Parallel execution
- Direct inter-agent communication
- Coordinated workflows

## Best Practices

**Use agent teams when:**
- Tasks require independent work in separate contexts
- Multiple agents need to collaborate and coordinate
- You need parallel execution across different domains
- Work spans multiple layers or components

**Use subagents when:**
- Tasks are focused and report back to main agent
- You need cost optimization with specialized models
- Tasks require tool restrictions or specialized prompts
- Work stays within a single session context
