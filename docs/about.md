# About ObiBrain

ObiBrain is a local-first Project Brain for AI agents. 

It helps agents retrieve project documents, source code context, approved memories, operational evidence, and workflow guidance before making recommendations or changes. Rather than letting an AI agent guess or act blindly, ObiBrain establishes a structured evidence layer.

## High-Level Architecture

ObiBrain organizes project knowledge into a few key conceptual layers:

- **RAG1 (Documents & Specifications)**: Indexes static documentation, architectural decision records (ADRs), wikis, and system requirements.
- **RAG2 (Source Code Intelligence)**: Provides AST-aware search, symbol descriptions, and code context retrieval to pinpoint where behaviors are implemented.
- **Memory (Human-Approved Decisions)**: Governs conventions, prior decisions, and recurring bug patterns. Changes to permanent memory must go through explicit developer review and approval.
- **OAL (On-Demand Operational Evidence)**: Retrieves short-lived operational context, such as ticket status, pull request context, or read-only database evidence, without turning it into permanent project memory.
- **MCP (Primitive Tool Surface)**: Exposes all retrieval operations via standardized Model Context Protocol (MCP) tools, making it easy to plug into any compatible AI client.
- **Agent Profiles**: Defines role-specific reasoning behaviors (e.g., Developer, QA, PM, Business Analyst) that coordinate these primitive tools to solve specific problems.

By splitting the infrastructure (MCP tools) from the intelligence (Agent Profiles), ObiBrain keeps the system predictable, local, and fully under developer control.
