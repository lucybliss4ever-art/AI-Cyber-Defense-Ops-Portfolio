#  Module 05 – Skills: Codifying Methodology

## Overview

This module taught me how Claude Code Skills can be used to store and apply repeatable cybersecurity standards.

In earlier modules, I gave Claude access to tools and knowledge. In this module, I learned how to teach Claude **how work should be done**.

The hands-on project focused on creating a Detection Engineering Skill that automatically applies specific standards when writing, reviewing, or validating detection rules.

---

## What I Learned

During this module, I learned:

- What Claude Code Skills are
- How Skills differ from Slash Commands
- How Skills auto-activate based on context
- How to create a `SKILL.md` file
- How YAML frontmatter controls activation
- How to write strong trigger descriptions
- How to include validation scripts
- How to add reference documents
- How to test whether a Skill activates correctly
- How to review third-party Skills for security risks
- How Skills can help standardize cybersecurity workflows

---

## Explain It Like I’m 10

Imagine Claude is a new employee.

Without a Skill, I have to keep reminding the employee:

- Follow the rules
- Check the severity
- Add the ATT&CK mapping
- Document false positives
- Include a test case

With a Skill, I give the employee a handbook.

Now every time the employee works on detection rules, the handbook is automatically followed.

That handbook is the Skill.

---

## Skills vs. Slash Commands

| Feature | Skills | Slash Commands |
|---|---|---|
| Activation | Automatic or manual | Manual only |
| Trigger | Context-based | User types `/command-name` |
| Main purpose | Apply methodology and standards | Run a specific workflow |
| Example | Detection rule standards | `/investigate-alert` |

A Slash Command waits for the user to call it.

A Skill can activate automatically when Claude recognizes that the task matches its trigger description.

---

## What I Built

I created a Detection Engineering Skill with this structure:

```text
.claude/
└── skills/
    └── detection-engineering/
        ├── SKILL.md
        ├── scripts/
        │   └── validate-rule.py
        └── references/
            ├── example-rules/
            │   └── lsass_memory_access.yml
            ├── severity-guide.md
            └── false-positive-patterns.md
