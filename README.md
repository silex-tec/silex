# Silex — evidence-based code archaeology

**Understand the codebase before changing the code.**

Silex reconstructs architecture, dependencies, workflows and business rules
from your source code — and serves that understanding to your AI coding
agents via [MCP](https://modelcontextprotocol.io). Every claim is anchored to
`file:line` with a verified quote. What Silex can't prove, it tells you.

**Local-first.** Your code never leaves your machine. No account, no card,
no telemetry.

→ **Site & docs: https://silex.tec.br** · [Concepts](https://silex.tec.br/concepts/) · [MCP tool reference](https://silex.tec.br/referencia-tools/) · [llms.txt](https://silex.tec.br/llms.txt)

## Install (free tier)

```bash
# Python 3.10+
pip install silex-archaeology
```

> Until the PyPI release lands you can install the wheel from
> [Releases](../../releases):
> `pip install https://github.com/silex-tec/silex/releases/latest/download/silex_archaeology-py3-none-any.whl`

Connect it to your MCP client (Claude Code, Cursor, Claude Desktop, Windsurf,
Cline, Continue, Zed) — stdio config:

```json
{
  "mcpServers": {
    "silex": { "command": "silex-mcp-server", "args": ["serve", "--stdio"] }
  }
}
```

Full install guide (Windows/PowerShell notes included): https://silex.tec.br/docs/

## Try it on a real codebase

Clone Microsoft's [eShop](https://github.com/dotnet/eShop) (MIT) and point a
scan at it — the [Concepts page](https://silex.tec.br/concepts/) shows the
community graph, the recovered order state machine and anchored findings from
that exact scan, so you can compare your output against a published reference.

## What you get (free)

- Local MCP server, full codebase scan (C#, JS/TS, Java, PHP, COBOL, VB…)
- Community map — the real shape of the system, vendor/generated classified
  out of the way by default
- Evidence anchored to `file:line`, confidence with provenance
- Unknown-territory detection: what can't be proven is flagged, not guessed
- Shareable evidence report
- Works with the AI seat you already pay for

**Pro tier** (team workspaces, deep architecture visualization, refactoring
trust contracts): coming soon — [join the waitlist](https://silex.tec.br/#waitlist).

## Issues & feedback

Bug reports and field feedback are welcome in
[Issues](../../issues). The engine is proprietary; this repository hosts
distribution, documentation and the public roadmap conversation.

---

© 2026 SILEX. All rights reserved.
