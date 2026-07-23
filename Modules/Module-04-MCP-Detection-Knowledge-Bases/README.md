# Module 04 – MCP: Detection Knowledge Bases

## Overview

This module expanded my understanding of the Model Context Protocol (MCP) by introducing **Resources**.

While Module 3 focused on creating MCP **Tools** that perform actions, this module showed how to create MCP **Resources** that provide structured knowledge for Claude to read.

Instead of repeatedly pasting detection rules into conversations, Claude can browse a knowledge base containing Sigma rules, ATT&CK mappings, and detection coverage.

---

## What I Learned

During this module I learned:

- Difference between MCP Tools and MCP Resources
- How Resources expose structured knowledge
- How Resource URIs organize information
- How to build a detection knowledge base
- How Sigma rules map to MITRE ATT&CK
- How Claude reads detection coverage
- How Resources and Tools work together

---

## Resources vs Tools

### MCP Tool

A Tool performs an action.

Examples:

- Run Hayabusa
- Execute a scan
- Analyze logs
- Query a SIEM

Think:

> Claude, do this.

---

### MCP Resource

A Resource provides information.

Examples:

- Sigma Rules
- ATT&CK mappings
- Incident Playbooks
- Detection Documentation

Think:

> Claude, read this.

---

## What I Built

This module focused on building a Detection Engineering Knowledge Base.

The project exposes:

- Sigma Detection Rules
- ATT&CK Technique Mappings
- Detection Coverage
- Rule Metadata

Instead of uploading rules every session, Claude can browse them directly.

---

## Example Resource URIs

```text
detection://rules

detection://rules/lsass_memory_access

detection://rules/by-technique/T1003.001

detection://attack/techniques/T1003.001
```

These URIs allow Claude to retrieve information whenever it is needed.

---

## Folder Structure

```text
mcp-detection-kb/

├── CLAUDE.md
├── server.py
├── rules/
│   ├── lsass_memory_access.yml
│   ├── kerberoasting.yml
│   ├── dcsync.yml
│   └── ...
├── mappings/
└── .claude/
```

---

## Hands-on Skills

During this module I practiced:

- Working with MCP Resources
- Building Resource URIs
- Organizing Sigma Rules
- Mapping ATT&CK Techniques
- Detection Coverage Analysis
- Detection Engineering concepts

---

## Explain It Like I'm 10

Imagine Claude is a new security analyst.

Without Resources...

You have to hand Claude your notebook every single day.

With Resources...

Claude has its own library and can read the information whenever it needs it.

Instead of asking:

"Here are my Sigma rules..."

Claude already knows where to find them.

---

## Real-World Applications

Detection engineers can use this approach to expose:

- Sigma Rules
- YARA Rules
- SOC Playbooks
- ATT&CK Mappings
- Threat Intelligence
- Incident Response Procedures
- Asset Inventories

This makes investigations faster and more consistent.

---

## Key Takeaways

✔ MCP Resources provide knowledge

✔ MCP Tools perform actions

✔ Resources help Claude understand your environment

✔ Resources improve detection engineering workflows

✔ Resources reduce repetitive work

---

## Personal Reflection

This module completely changed how I think about AI assistants.

Before this lesson, I assumed AI only answered questions.

Now I understand that Claude can be connected to my own knowledge base, making it far more useful for cybersecurity investigations.

Instead of constantly copying and pasting information, I can provide structured resources that Claude can browse whenever they are needed.

This approach makes AI feel much more like a real cybersecurity teammate than just a chatbot.
