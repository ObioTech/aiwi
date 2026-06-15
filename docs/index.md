# AIWI — AI Workflow Infrastructure
**A local-first Project Brain for AI agents**

AIWI helps coding agents understand project knowledge, source code, decisions, memory, and operational evidence before they act.

---

## What is AIWI?
AIWI is an experimental local-first infrastructure layer that helps AI agents work with project knowledge. 

It connects documents, source code, human-approved memory, operational evidence, and agent profiles into a cohesive **Project Brain**.

## Why local-first?
Project knowledge is sensitive. Source code, internal decisions, bug patterns, requirements, and operational context should not be copied into a remote system by default. 

AIWI is designed to keep project intelligence close to the developer workspace, running locally and keeping your data under your control.

## Core Principles
- **Local-first**: Runs locally on your machine.
- **SQLite-first**: Uses lightweight, local SQLite database files to store governed project state.
- **MCP-native**: Exposes primitive tools natively through the Model Context Protocol.
- **Human-approved memory**: Promotes staging observations to permanent project memory only after explicit developer review.
- **Primitive tools, not workflow SaaS**: Provides fundamental querying capabilities rather than imposing a rigid SaaS workflow.
- **Agent Profiles compose intelligence**: Keeps the infrastructure simple while allowing specialized profiles (e.g., BA, Developer, QA, PM) to define reasoning behavior.

## What AIWI is not
- **Not a Jira/Linear replacement**: It does not track tasks or host backlog boards.
- **Not a PM/BA/QA workflow SaaS**: It does not automate team processes in the cloud.
- **Not a hosted RAG product**: It does not upload your codebase to a remote service.
- **Not a fully autonomous project manager**: It is an assistant, not an autonomous agent that acts without human oversight.

## Current Status
AIWI is currently an early private project. The core package is private, while this public site shares the thinking, architecture notes, and lessons learned from building it.

## Start Reading
- [Why I'm Building AIWI](_posts/2026-06-15-why-im-building-aiwi.md) (Read the blog post)
- [About AIWI](about.md) (Learn about the architecture)
- [Blog / Notes](blog.md) (Explore all posts)
