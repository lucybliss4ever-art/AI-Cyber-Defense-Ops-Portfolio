# Module 02 – Building Your First Security Tool

##  Overview

This module taught me how to work with Claude Code through an iterative development process.

Instead of expecting perfect results from one prompt, I learned to describe what I wanted, review Claude’s output, test the result, provide corrections, and continue refining the project until it worked as expected.

The practical project for this module was a Python-based Sysmon XML parser.

---

##  What I Learned

- How to initialize a Claude Code project using `/init`
- How to use `CLAUDE.md` to define project goals and conventions
- How to reference files directly using `@filename`
- How to add temporary session context using `#`
- How to use Plan Mode for larger changes
- How to monitor context using `/context`
- How to free context space using `/compact`
- How to run long tasks in the background with `Ctrl+B`
- How to undo changes using `Esc Esc`
- How to preserve progress with Git and `HANDOFF.md`

---

##  What I Built

I built a Python tool that parses Sysmon Event ID 1 XML files.

The parser extracts important detection fields such as:

- Event ID
- UTC time
- Image
- Command line
- User
- Integrity level
- Parent image
- Parent command line
- Computer name
- Hashes

The finished tool also supports:

- Single-event and multi-event XML files
- Filtering by process, user, or integrity level
- JSON, JSONL, and CSV output
- Basic statistics for quick triage

---

##  Explain It Like I’m 10

Imagine you ask a very smart teammate to build something for you.

The first version may not be perfect.

So you check it and say:

> “This part works, but this field is missing.”

Your teammate fixes it.

Then you test again and say:

> “Now make it work with several events, not just one.”

That is the iteration process.

You explain, Claude tries, you review, and together you improve the result.

---

##  The Iteration Workflow

1. Describe what you want
2. Let Claude attempt it
3. Review the result
4. Test it
5. Give specific feedback
6. Repeat until complete

This taught me that Claude Code works best as a collaborative assistant, not as a one-click magic solution.

---

##  Commands and Features Used

| Command or Feature | Purpose |
|---|---|
| `/init` | Initialize the project and create `CLAUDE.md` |
| `/context` | Check context window usage |
| `/compact` | Summarize the session and free context space |
| `Shift+Tab` | Enter or exit Plan Mode |
| `Ctrl+B` | Run long tasks in the background |
| `Esc Esc` | Revert Claude’s most recent change |
| `@filename` | Point Claude directly to a file |
| `#` | Add temporary session context |
| `claude --resume` | Resume a previous session |

---

##  Real-World Application

A Sysmon parser can help security analysts transform raw Windows event XML into structured data that is easier to review, search, filter, and send into other tools.

The same development workflow can also be used for:

- Windows Security events
- Linux audit logs
- AWS CloudTrail
- Azure Activity Logs
- Other structured security data

The tool may change, but the workflow remains the same.

---

##  Key Takeaways

The biggest lesson from this module was that communication matters.

Claude performs better when the goal, requirements, examples, and corrections are clear.

I also learned that context management is important during long sessions. Files such as `CLAUDE.md` and `HANDOFF.md` help preserve important project decisions so work can continue across sessions.

---

##  Skills Demonstrated

- Claude Code workflow
- Python scripting
- Sysmon event analysis
- XML parsing
- JSON, JSONL, and CSV output
- Prompt refinement
- Debugging
- Context management
- Git version control
- Technical documentation

---

##  Interview Questions

### What did you build in this module?

I built a Python-based Sysmon Event ID 1 parser that extracts important process creation fields and outputs structured data.

### What is the iteration workflow?

It is the process of describing a task, reviewing the result, testing it, providing feedback, and refining the solution until it meets the requirements.

### Why is `CLAUDE.md` important?

It gives Claude stable project context, including goals, conventions, requirements, and design decisions.

### When would you use Plan Mode?

I would use Plan Mode before making a large or complex change so Claude can examine the current project and propose an implementation approach before editing files.

### Why use a `HANDOFF.md` file?

It preserves session state, completed work, pending tasks, and design decisions so the project can be resumed later.

---

##  Lucy’s Reflection

This module helped me understand that working with AI is a collaborative process.

At first, I expected Claude to understand everything from one prompt. I learned that better results come from giving clear instructions, testing the output, and providing specific feedback.

Building the Sysmon parser also gave me practical experience working with real security event data.

The biggest lesson I learned was that I do not need to know every line of code before starting. I need to understand the goal, communicate clearly, review the result, and keep improving it.
