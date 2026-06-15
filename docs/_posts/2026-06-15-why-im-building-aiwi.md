---
layout: post
title: "Why I’m Building AIWI"
date: 2026-06-15
permalink: /posts/why-im-building-aiwi/
---

# Why I’m Building AIWI

## The Problem

AI agents are getting better at coding, but they still forget the project.

Out of the box, an LLM or a generic coding agent does not naturally know:
- Why a specific architectural decision was made.
- Which conventions matter for this codebase.
- Which module is risky or fragile to touch.
- Which bug patterns have occurred here in the past.
- Which business requirement is still fresh and active.
- Which ticket is actually important, and which is only operational noise.

A generic context window search or broad codebase search often gets overwhelmed by noise, leading to suggestions that break conventions or re-introduce old bugs.

## The Idea

AIWI is my attempt to build a **local-first Project Brain** for AI agents.

AIWI acts as a dedicated context layer that sits alongside the developer workspace.
- It does not replace the agent.
- It does not replace Jira or Linear.
- It does not replace your IDE.

Instead, it feeds the agent the exact project memory and evidence it needs before it acts.

## The Principles

AIWI is designed around these foundational principles:

- **Local-first**: Project intelligence runs on your machine, under your direct control.
- **SQLite-first**: Structured memory and state are saved in simple, portable local SQLite databases.
- **MCP-native**: It exposes simple, powerful tool primitives using the Model Context Protocol.
- **Human-approved memory**: AI memory should not write itself into truth. Observations must be staged and approved by a developer before becoming permanent.
- **Primitive tools, not workflow SaaS**: It focuses on exposing context rather than building complex, opinionated task-tracking pipelines.
- **Agent Profiles compose intelligence**: Specialized personas (Developer, QA, PM, BA) are configured via reasoning instructions, keeping the infrastructure layer lightweight.

## Why This Matters

A typical AI coding assistant can read files and generate diffs. But real software engineering requires understanding more than just syntactical code completion. 

It requires understanding:
- Product decisions and business rules.
- Historical bug patterns and regression scope.
- Architecture boundaries and safe human approval points.

AIWI is an experiment in giving agents that missing project brain.

## Current Status

AIWI is still in its early stages. 

The core package is currently private as I iterate on the local indexing engine and profiles. I am starting by sharing the core concepts, architecture notes, and lessons learned here in public.

## What's Next

In upcoming posts, I'll dive deeper into:
- **Project Brain vs. Workflow Suite**: Why separation of concerns matters for AI context.
- **Local-first AI infrastructure**: How to keep developer workspaces fast and private.
- **Human-approved memory**: The design of our staging and curation workflow.
- **MCP primitive tools**: Exposing deep context over simple protocols.
- **Requirement Impact Analysis**: Tracing specifications down to code changes and tests.
