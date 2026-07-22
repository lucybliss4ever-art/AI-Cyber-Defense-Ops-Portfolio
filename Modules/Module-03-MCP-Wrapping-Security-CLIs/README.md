# Module 03 – MCP: Wrapping Security CLIs

##  Overview

This module introduced me to the Model Context Protocol (MCP), a standardized way for AI assistants like Claude to securely communicate with external tools.

Instead of manually switching between applications, MCP allows Claude to invoke approved security tools directly, making investigations faster and more efficient.

The hands-on project focused on creating an MCP server that wraps the Hayabusa command-line tool for Windows Event Log analysis.

---

#  What I Learned

During this module I learned:

- What Model Context Protocol (MCP) is
- The difference between MCP Tools and MCP Resources
- How MCP Servers work
- How to build a Python-based MCP Server
- How to wrap command-line security tools
- How Claude Code communicates with MCP Servers
- How to configure MCP using `.claude/settings.json`
- How to troubleshoot MCP connections using `/doctor`
- How Claude Desktop can also use MCP Servers

---

#  Hands-On Lab

In this module I built:

- A Python MCP Server
- A Hayabusa wrapper
- A `scan_evtx` MCP tool
- Claude Code integration
- Claude Desktop integration

I also learned how to:

- Register MCP servers
- Configure settings
- Test tool execution
- Troubleshoot server connections
- Extend Claude with external cybersecurity tools

---

#  Explain It Like I'm 10

Imagine Claude is a superhero.

The superhero is very smart but can't open doors.

MCP gives Claude a keyring.

Each key opens a different tool.

One key opens Hayabusa.

Another key could open YARA.

Another could open Volatility.

Instead of only talking about investigations, Claude can actually use approved tools to help perform them.

---

#  Real-World Application

Without MCP:

1. Run Hayabusa manually.
2. Copy the results.
3. Paste them into Claude.
4. Ask for analysis.

With MCP:

Claude can securely run Hayabusa, collect the results, and immediately begin analyzing suspicious activity.

This greatly improves Security Operations Center (SOC) workflows by reducing manual steps.

---

#  Key Takeaways

The biggest lesson from this module was understanding that MCP transforms AI from a chatbot into an assistant capable of securely interacting with external cybersecurity tools.

Once a tool is wrapped inside an MCP Server, Claude can reuse it across projects and sessions.

---

#  Skills Demonstrated

- Model Context Protocol (MCP)
- Python MCP Servers
- AI Tool Integration
- Hayabusa
- Windows Event Log Analysis
- Security Automation
- Claude Code Configuration
- Claude Desktop Integration
- Troubleshooting

---

#  Interview Questions

## What is MCP?

Model Context Protocol (MCP) is a standard that allows AI assistants to securely communicate with external tools and resources.

---

## What is an MCP Server?

An MCP Server exposes tools and resources that Claude can safely access during conversations.

---

## What is the difference between MCP Tools and Resources?

**Tools** perform actions.

Examples:

- Run Hayabusa
- Execute YARA
- Perform IOC lookups

**Resources** provide information.

Examples:

- Documentation
- Configuration files
- Threat intelligence data

---

## Why would a SOC analyst use MCP?

Because it allows AI to automate repetitive work, execute approved tools, analyze results, and speed up investigations.

---

#  Lucy's Reflection

Before this module, I thought AI only answered questions.

Now I understand that AI can securely interact with external cybersecurity tools through MCP.

Learning how Hayabusa could become an AI-powered tool completely changed how I think about automation in cybersecurity.

This module showed me how AI can become an active teammate during investigations rather than simply acting as a chatbot.

#  Beyond the Course

After completing this module, I realized the same MCP pattern could be used with many cybersecurity tools, including:

- Volatility
- Chainsaw
- YARA
- Sigma CLI
- Nmap
- WHOIS lookups
- VirusTotal integrations
- Threat Intelligence APIs

Understanding this pattern opened my eyes to how AI assistants can become powerful cybersecurity teammates.
