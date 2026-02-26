<div align="center">

<img src="forge-logo.png" alt="Forge" width="100">

# Forge

**From agents to teams.**

The program manager your AI agents are missing.

[forge.nxtg.ai](https://forge.nxtg.ai)

</div>

---

## The Problem

Multi-agent inside a single tool works fine. Claude Code runs 20 subagents and they stay aligned because the tool manages that coordination internally.

The problem is multi-tool. Claude Code, Codex CLI, and Gemini CLI on the same repo with no shared state, no file locking, no knowledge capture. Each tool starts from scratch. Decisions evaporate between sessions. Two tools edit the same file and neither knows the other exists.

Forge solves this. One product, three levels.

---

## One Product, Three Levels

<table>
<tr>
<td width="33%" valign="top">

### Level 1: [Forge Plugin](https://github.com/nxtg-ai/forge-plugin)

**Zero-dependency governance for Claude Code.**

Install in 30 seconds. Health scoring, gap analysis, quality gates, and specialized agents.

```bash
claude plugin add nxtg-ai/forge-plugin
```

21 commands; 22 agents; 29 skills; 6 hooks; 8 MCP tools.

</td>
<td width="33%" valign="top">

### Level 2: [Forge Orchestrator](https://github.com/nxtg-ai/forge-orchestrator)

**Multi-tool coordination in a single Rust binary.**

File locking, knowledge capture, task planning, drift detection. Coordinates Claude Code, Codex CLI, and Gemini CLI.

```bash
curl -fsSL https://forge.nxtg.ai/install.sh | sh
forge init
```

4MB binary; 292 tests; 10 MCP tools.

</td>
<td width="33%" valign="top">

### Level 3: [Forge Dashboard](https://github.com/nxtg-ai/forge-ui)

**Full visual platform for multi-tool AI coordination.**

Real-time governance HUD, agent activity feed, and the Infinity Terminal: sessions that survive browser close, network drops, and device switches.

```bash
git clone https://github.com/nxtg-ai/forge-ui
npm install && npm run dev
```

58 components; 4,146 tests; 87% coverage.

</td>
</tr>
</table>

---

## How It Works

```
  forge-orchestrator (Rust, 4MB)
  Policy core. File locking. Knowledge flywheel.
  Governance. MCP server. Multi-tool adapters.

  Policy enforced here. Nowhere else.
         |                    |
    forge-plugin          forge-ui
    (Level 1)             (Level 3)
    Claude Code           React dashboard
    21 commands           Infinity Terminal
    22 agents             Governance HUD
    29 skills             Agent feed
```

Communication: `.forge/` filesystem + MCP stdio. No daemon. No database. State is files.

---

## Why Forge Exists

Every developer running multiple AI tools on the same repo hits the same walls.

**File locking.** Two tools editing the same file at the same time. No locks. No coordination. Forge acquires exclusive locks per file; queued tools get notified.

**Knowledge capture.** Decisions, patterns, learnings captured automatically. Auto-classified and searchable. A Claude Code session's decisions are available to Codex CLI the next day.

**Drift detection.** Your spec says "build auth" but the tool is refactoring CSS. Forge catches divergence early.

**Governance.** Health scores from A through F, computed across 8 quality dimensions. Continuously validated, not just at PR time.

These are the same failure modes that break billion-dollar enterprise programs. The founder spent 23 years solving them with human teams. Forge encodes those patterns for AI tools.

---

## Quick Start

```bash
# Level 1: Governance in 30 seconds
claude plugin add nxtg-ai/forge-plugin

# Level 2: Multi-tool coordination
curl -fsSL https://forge.nxtg.ai/install.sh | sh
forge init

# Level 3: Visual dashboard
git clone https://github.com/nxtg-ai/forge-ui
npm install && npm run dev
```

Each level builds on the last. Nothing forces you to upgrade. Adoption follows the pain.

---

## Open Source

| Repo | Level | Language | Tests |
|:-----|:------|:---------|:------|
| [forge-plugin](https://github.com/nxtg-ai/forge-plugin) | 1: Governance | Markdown + Shell | Structure validation |
| [forge-orchestrator](https://github.com/nxtg-ai/forge-orchestrator) | 2: Coordination | Rust | 292 |
| [forge-ui](https://github.com/nxtg-ai/forge-ui) | 3: Dashboard | TypeScript + React | 4,146 |

---

<div align="center">

**[forge.nxtg.ai](https://forge.nxtg.ai)** | **[nxtg.ai](https://nxtg.ai)** | Built by [@AxW](https://www.linkedin.com/in/-asif-/)

*"The program manager your AI agents are missing."*

</div>
