---
name: addskill
description: Use when the user wants to create a reusable terminal workflow or command sequence.
---

# Add Skill

## When to use this

When the user wants to save a sequence of terminal commands for later reuse.

Examples:
- "Create a skill called deploy-node"
- "Remember these commands as a skill"
- "Save this workflow"

## Procedure

1. Ask for:
   - Skill name
   - Description
   - Procedure

2. Create a markdown file in:

hackaton-agent-starter/.opencode/skills/skillName/<name>

3. Store:

# Name

<skillname>

## Description

<description>

## Commands

```bash
command1
command2
command3