# AI Agent Guide: creating new skills

This document guides you on how to draft a new skill for this project. All skills must be placed in the `./skills` directory.

## 1. Skill Location
- Create a new directory for the skill: `./skills/<skill-name-kebab-case>/`.
- The main definition file must be named `SKILL.md` inside that directory.

## 2. Directory Structure
Ensure the skill follows this structure:
```text
skills/<skill-name>/
├── SKILL.md          # REQUIRED: The core definition
├── scripts/          # OPTIONAL: Executable scripts (Python/Node/Bash)
├── resources/        # OPTIONAL: Static files, templates, or docs
└── requirements.txt  # OPTIONAL: Dependencies
```

## 3. SKILL.md Format
The `SKILL.md` file MUST use the following format with YAML frontmatter.

```markdown
---
name: <skill-name-kebab-case>
description: <One-sentence summary of what this skill does and WHEN to use it>
version: 1.0.0
---

# <Skill Name Title>

## Capability
Describe what this skill allows the agent to do. Keep it concise.

## Triggers
- List specific keywords or user intents that should trigger this skill.
- Example: "User asks to analyze a CSV file."

## Instructions
1.  Step-by-step instructions on how to execute the skill.
2.  Mention strictly which scripts to run.
3.  Be specific about input/output formats.

## Tools / Commands
List the executable commands available in the `scripts/` folder.
- `python scripts/example_script.py --arg <value>`: Description of what this command does.

## Examples
Provide a few-shot example of a user request and the corresponding action.
User: "<Example user prompt>"
Action: <Description of action or exact command to run>
```

## 4. Drafting Rules
- **Naming**: Use `kebab-case` for folder names (e.g., `pdf-processing`).
- **Scripts**: Prefer independent CLI scripts in the `scripts/` folder over complex library imports.
- **Paths**: All paths in instructions should be relative to the project root or the skill directory as appropriate (usually project root for execution).
- **Conciseness**: Keep the description and instructions sharp. Agents use the description to decide whether to load the full skill.

## 5. Documentation
Update readme skills table accordingly.