## Hi there 👋
<p align="center"> <img src="./banner.svg" width="100%" alt="Yusuf Orçan" /> </p> <h1 align="center">Yusuf Orçan</h1> <p align="center"> <b>I design languages and the tools that keep them honest.</b> </p> <p align="center"> Building <a href="https://github.com/orhunlang/orhun"><b>Orhun</b></a>, a Turkish-first programming language,<br/> and a local-first toolkit that makes coding agents explain themselves. </p>
Two things, one story
1. Orhun — a language with a contract
Turkish-first syntax and diagnostics. C++17 bootstrap today, self-hosting tomorrow.

Version	1.1.0 · stable 1.0 language contract
Pipeline	lexer → parser → interpreter → bytecode compiler → VM → stdlib
Proof	CI on Windows / Linux / macOS · release notes · cheatsheet


bash

Kopyala
# Linux / macOS
curl -fsSL https://raw.githubusercontent.com/orhunlang/orhun/v1.1.0/install.sh | bash
powershell

Kopyala
# Windows
irm https://raw.githubusercontent.com/orhunlang/orhun/v1.1.0/install.ps1 | iex
orhun

Kopyala
yaz "Merhaba Orhun"
→ Repository · Docs · Status

2. everyhook — one hook, every coding agent
Claude Code, Codex CLI, Gemini CLI, Copilot CLI, Cursor.
Same contract, one adapter per agent.

Evidence	
Agents	5 adapters
Fixtures	64 real captured documents, bench-tested
Tokens	0 for the tool and for an installed hook, unless it returns a reason
Deps	None — Node 18+, node: modules only


bash

Kopyala
npx -y github:nrzz/everyhook explain
bash

Kopyala
git clone https://github.com/nrzz/everyhook
node everyhook/bin/everyhook.mjs install everyhook/examples/block-force-push.mjs --all
→ Repository · Examples

The rest of the ecosystem
Agent diagnostics that answer why, not just what.
Each CLI is zero-token, local-first, and labels every claim verified / documented / not verified.

Tool	Answers
claude-windows-doctor	Which shell the model gets on Windows — and the fix
claude-mcp-check	MCP servers Claude will load, cost, and why they fail
claude-settings-doctor	Merged settings with sources; dead rules removed
claude-permission-doctor	Why Claude asked — rule by rule
claude-cost-guard	Budgets from local transcripts; hard stop before the bill
codex-config-doctor	What Codex will actually do with your config


<details> <summary><b>Full toolkit</b></summary> <br/>
Tool	What it does
agent-windows-doctor	Shell identity for every coding agent
claude-md-doctor	What CLAUDE.md costs per session
claude-hook-bench	Hooks against the exact JSON agents send
claude-session-replay	Session → HTML replay or Markdown
claude-session-tidy	Keep what matters past cleanup
claude-code-guardrails	Safety presets, cost zero until they stop something
claude-code-handover	Short sessions, durable decisions
claude-code-starter-kits	Lean .claude/ in one command
claude-code-team-sync	Share context, not logins
claude-chat-ferry	Move a chat across agents
claude-relocate	XDG paths and a safe config move
claude-automode-doctor	Decode auto-mode classifier verdicts


</details>
How I work
text

Kopyala
quiet focus      smallest change that removes a real blocker
clean contracts  clear beats clever; document the sharp edges
evidence first   verified · documented · not verified
local first      your machine, your tokens, your control
fail loudly      a quiet bug is a landmine
<p align="center"> <i>If a tool can’t say why it did something, it isn’t done.</i> </p> <p align="center"> <a href="https://github.com/orhunlang/orhun">Orhun</a> · <a href="https://github.com/yoreva-01/everyhook">everyhook</a> · <a href="https://github.com/yoreva-01?tab=repositories">all repositories</a> </p>
