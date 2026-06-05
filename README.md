<div align="center">

# dev-utils-skills

**Developer utility skills — code generation, test writing, MCP builder, frontend design**

[![GitHub](https://img.shields.io/badge/github-full--statck--skills%2Fdev-utils-skills-green.svg)](https://github.com/full-statck-skills/dev-utils-skills)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Compatible-purple.svg)](https://agentskills.io)

English | [简体中文](./README.zh-CN.md)

[Introduction](#-introduction) ·
[Install](#-install) ·
[Skills](#-skills) ·
[Supported Agents](#-supported-agents) ·
[Ecosystem](#-ecosystem)

</div>

---

## 📖 Introduction

**Dev Utilities Skills** is a curated collection of Agent Skills for AI coding agents, part of the [Full Stack Skills](https://github.com/partme-ai/full-stack-skills) ecosystem maintained by [PartMe.AI](https://github.com/partme-ai).

This package includes **12 skills**. Each skill is a self-contained `SKILL.md` file that AI agents load on-demand.

## 📦 Install

```bash
npx skills add full-statck-skills/dev-utils-skills
```

Or install specific skills:

```bash
npx skills add full-statck-skills/dev-utils-skills --skill <skill-name>
```

## 🎯 Skills (12)

| Skill | Description |
|-------|-------------|
| `agent-browser` | A comprehensive skill for using agent-browser, a CLI tool for browser automation designed for AI agents, developed by... |
| `code-generator` | Provides comprehensive guidance for code generation including template-based generation, code scaffolding, and automa... |
| `documentation-builder` | Provides comprehensive guidance for building documentation including documentation generation, formatting, and docume... |
| `frontend-design` | Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks ... |
| `java-code-comments` | | |
| `maven-search` | Provides comprehensive guidance for searching and retrieving Maven components from Maven Central Repository (https://... |
| `mcp-builder` | Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external servi... |
| `mybatis-plus-generator` | | |
| `test-writer` | Provides comprehensive guidance for writing tests including test case creation, test structure, and testing best prac... |
| `theme-factory` | Toolkit for styling artifacts with a theme. These artifacts can be slides, docs, reportings, HTML landing pages, etc.... |
| `web-artifacts-builder` | Suite of tools for creating elaborate, multi-component claude.ai HTML artifacts using modern frontend web technologie... |
| `webapp-testing` | Toolkit for interacting with and testing local web applications using Playwright. Supports verifying frontend functio... |

## 🤖 Supported Agents

Works with [Claude Code](https://code.claude.com), [Codex](https://developers.openai.com/codex), [Cursor](https://cursor.com), [OpenCode](https://opencode.ai), [Gemini CLI](https://geminicli.com), [GitHub Copilot](https://github.com/features/copilot), [Windsurf](https://codeium.com/windsurf), and [70+ others](https://agentskills.io/clients).

### Claude Code Installation

**Option 1: npx skills CLI (Recommended)**

```bash
npx skills add full-statck-skills/dev-utils-skills
```

**Option 2: Manual Installation**

```bash
git clone https://github.com/full-statck-skills/dev-utils-skills.git
cp -r dev-utils-skills/skills/* .claude/skills/
```

For more details, see the [Claude Code Skills Guide](https://code.claude.com/docs/en/skills) and [Agent Skills Spec](https://agentskills.io/).

## 🌐 Ecosystem

| Resource | Link |
|----------|------|
| **Full Stack Skills** | [github.com/partme-ai/full-stack-skills](https://github.com/partme-ai/full-stack-skills) |
| **All Skill Groups** | [github.com/full-statck-skills](https://github.com/full-statck-skills) |
| **Agent Skills Spec** | [agentskills.io](https://agentskills.io) |
| **Skills CLI** | [github.com/vercel-labs/skills](https://github.com/vercel-labs/skills) |

## 📄 License

Apache 2.0 — see [LICENSE](LICENSE).
