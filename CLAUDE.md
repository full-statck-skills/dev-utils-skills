# CLAUDE.md

## Project Overview

`dev-utils-skills` is a Claude Code plugin in the [Full Stack Skills](https://github.com/partme-ai/full-stack-skills) ecosystem. It packages **12 Agent Skills** for developer utilities — each a self-contained `SKILL.md` file loaded on-demand by AI coding agents.

## Skills (12)

| # | Skill | Description |
|---|-------|-------------|
| 1 | `agent-browser` | Browser automation CLI (`agent-browser`) — install, commands, selectors, sessions, CDP/streaming. Heaviest skill (api/ + examples/ + templates/). |
| 2 | `code-generator` | General code generation — functions, modules, scaffolding, multi-language. SKILL.md only. |
| 3 | `documentation-builder` | Documentation generation and formatting. SKILL.md only. |
| 4 | `frontend-design` | Production-grade frontend interfaces — typography, color, animation, distinct aesthetics. SKILL.md only. |
| 5 | `java-code-comments` | JavaDoc/intelligent comments for Java components (Entity, Service, Controller, etc.). Templates + reference. |
| 6 | `maven-search` | Search/retrieve Maven Central artifacts — coordinates, versions, dependency analysis. api/ + examples/ + scripts/. |
| 7 | `mcp-builder` | Build MCP servers (Python FastMCP / TypeScript SDK) — 4-phase process: research → implement → test → evaluate. reference/ + scripts/. |
| 8 | `mybatis-plus-generator` | Generate MyBatis-Plus CRUD code from DB tables — MVC/DDD/Clean architectures, Java/Kotlin, FreeMarker templates. |
| 9 | `test-writer` | Unit/integration/E2E test writing best practices. SKILL.md only. |
| 10 | `theme-factory` | Styling artifacts (slides, docs, HTML) with 10 predefined themes (arctic-frost, midnight-galaxy, etc.). |
| 11 | `web-artifacts-builder` | Multi-component HTML artifacts with modern frontend technologies. scripts/. |
| 12 | `webapp-testing` | Playwright-based local web app testing. examples/ + scripts/. |

## Directory Structure

```
skills/<skill-name>/
├── SKILL.md              # Entry point (YAML frontmatter: name, description, license)
├── api/                  # API reference docs (commands, selectors, options)
├── examples/             # Worked examples and use cases
├── reference/            # Standards, guides, best practices
├── templates/            # Code/comment templates (FreeMarker .ftl for mybatis-plus-generator)
├── scripts/              # Runnable scripts (maven-search, mcp-builder, webapp-testing)
└── themes/               # Visual themes (theme-factory only)
```

Supporting files: `.claude-plugin/plugin.json` (registry), `README.md` / `README.zh-CN.md` (bilingual), `integration-plan.md` (external skill integration assessment).

## SKILL.md Authoring Conventions

- **Frontmatter**: `name` (kebab-case, must match directory), `description` (when to use + trigger guidance), optional `license`
- **Structure**: "When to use this skill" → trigger phrases / exclusions → "How to use this skill" → step-by-step workflow → reference files listing → keywords
- **Progressive disclosure**: SKILL.md is a routing index — sub-files (examples/, reference/, api/) are loaded on-demand via file paths, never inlined
- **Skills with `mybatis-plus-generator/README.md`**: README is a human-oriented overview; SKILL.md is the agent-facing entry point
- **Bilingual**: Larger skills are English-only or bilingual (Chinese); simpler ones are Chinese-only per their target developer audience
- **Avoid false triggers**: Skills like `mybatis-plus-generator` and `java-code-comments` include explicit exclusion rules so they don't fire on generic requests

## Key Files

- `.claude-plugin/plugin.json` — plugin registry (name, version, skill paths)
- `integration-plan.md` — assessment of external repos (mattpocock/skills, Dimillian/Skills, videocut-skills) for potential integration
- `README.md` / `README.zh-CN.md` — bilingual project README with install instructions and skill table
