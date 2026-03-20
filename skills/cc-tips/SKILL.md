---
name: cc-tips
description: Research and compile Claude Code tips and tricks from known experts and official sources into a structured, source-verified markdown document
disable-model-invocation: true
argument-hint: "[output-file] — e.g. cc-tips-2026-03-20.md (default: cc-tips.md)"
allowed-tools: WebSearch,WebFetch,Write,Read,Glob,Grep,Agent
---

# Claude Code Tips & Tricks Researcher

You are a research agent that compiles Claude Code tips and tricks from well-known experts and official sources.

## Your Task

Research, verify, and compile a comprehensive Claude Code tips & tricks document.

**Output file**: Write the result to `$ARGUMENTS` (default: `cc-tips.md` in the current directory).

## Sources to Research

Search the web thoroughly for Claude Code tips from these known contributors and sources. Use multiple search queries per person/source to be thorough.

### Priority Sources (Anthropic Team)

1. **Boris Cherny** — Anthropic engineer, prolific Claude Code content creator
   - Search: "Boris Cherny Claude Code", "@anthropic Boris Cherny tips", his Twitter/X threads
   - Known for: detailed workflow tips, CLAUDE.md best practices, agentic coding patterns

2. **Tariq / Tarik** — Anthropic team member
   - Search: "Tariq Anthropic Claude Code", "Tarik Claude Code tips"

3. **Official Anthropic Sources**
   - Anthropic blog posts about Claude Code best practices
   - Claude Code documentation (https://docs.anthropic.com/en/docs/claude-code)
   - The official Claude Code tips page
   - Search: site:anthropic.com "Claude Code" tips, site:docs.anthropic.com claude-code

### Community Sources

4. **Well-known content creators** — search for popular Claude Code tips threads/posts from:
   - "Claude Code tips and tricks 2025 2026"
   - "Claude Code best practices"
   - "Claude Code workflow"
   - "Claude Code advanced tips"
   - Popular Twitter/X threads about Claude Code
   - YouTube videos with Claude Code tips
   - Dev.to, Medium, HackerNews discussions
   - GitHub awesome lists for Claude Code

5. **Specific topics to search for tips about**:
   - CLAUDE.md best practices
   - Custom slash commands and skills
   - Hooks and automation
   - MCP server usage
   - Multi-agent workflows
   - Git integration tricks
   - Context management
   - Permission modes
   - Keyboard shortcuts
   - IDE integration (VS Code, JetBrains)
   - Memory and persistence
   - Testing workflows
   - Debugging with Claude Code
   - Docker and deployment workflows

## Output Format

Write the document in this exact structure:

```markdown
# Claude Code Tips & Tricks

> Compiled by [CCCL](https://cccl.ai) (Claude Code Central London) — a community plugin.
> Last updated: {today's date}
>
> Every tip includes a source link. Install this plugin to regenerate anytime:
> `claude plugin install https://github.com/vikrampawar/cccl-dailys`

## Table of Contents
{auto-generated TOC}

---

## Basic Tips
{Tips suitable for beginners — getting started, first-day productivity}

### Category Name
| # | Tip | Source |
|---|-----|--------|
| 1 | Tip description | [Author/Title](url) |

---

## Intermediate Tips
{Tips for regular users — workflows, configuration, efficiency}

### Category Name
| # | Tip | Source |
|---|-----|--------|
| 1 | Tip description | [Author/Title](url) |

---

## Advanced Tips
{Tips for power users — hooks, multi-agent, custom tooling, MCP}

### Category Name
| # | Tip | Source |
|---|-----|--------|

---

## Sources & Further Reading
{Full list of all sources with descriptions}

| # | Source | Author | Type | URL |
|---|--------|--------|------|-----|
| 1 | Title | Author | Blog/Tweet/Video/Docs | url |
```

## Rules

1. **EVERY tip MUST have a verified source link** — no link, no inclusion. Do not make up URLs.
2. **Verify links work** — use WebFetch to confirm each source URL loads successfully before including it.
3. **Be thorough** — launch multiple parallel Agent searches to cover all sources.
4. **Deduplicate** — if the same tip appears in multiple sources, pick the best/original source and note others.
5. **Be specific** — tips should be actionable, not vague. Include the exact command, config, or technique.
6. **Attribute correctly** — credit the person who shared the tip, not just the platform.
7. **Categorize thoughtfully**:
   - **Basic**: First-day essentials, simple commands, getting started
   - **Intermediate**: Configuration, workflows, CLAUDE.md, custom commands
   - **Advanced**: Hooks, MCP, multi-agent, plugin development, automation
8. **Aim for 50+ tips minimum** across all categories.
9. **Include code blocks** where relevant (e.g., CLAUDE.md snippets, hook configs, commands).

## Execution Strategy

1. Launch parallel web searches for all priority sources simultaneously
2. For each source found, fetch the content and extract specific tips
3. Search for additional community sources
4. Compile, deduplicate, categorize, and write the output file
5. Do a final verification pass on all links
