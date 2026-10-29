<p align="center">
  <img src="./banner.svg" width="100%" alt="Yusuf Orçan" />
</p>

<h1 align="center">Yusuf Orçan</h1>

<p align="center">
  <b>Systems &amp; Compiler Engineering · C++17 &amp; Go · Creator of <a href="https://github.com/orhunlang">@orhunlang</a></b>
</p>

<p align="center">
  Building <a href="https://github.com/orhunlang/orhun"><b>Orhun</b></a> — a Turkish-first programming language runtime in C++17 —<br/>
  and contributing to compilers, graph algorithms, static analysis scanners, and local-first developer tooling.
</p>

<p align="center">
  <a href="https://github.com/orhunlang/orhun"><img alt="Orhun Runtime" src="https://img.shields.io/badge/Orhun-Language%20Runtime%20v1.1.0-00f2fe?style=flat-square&labelColor=0b1220" /></a>
  <a href="https://github.com/orhunlang/setup-orhun"><img alt="setup-orhun Action" src="https://img.shields.io/badge/GitHub%20Action-setup--orhun-7c3aed?style=flat-square&labelColor=0b1220" /></a>
  <img alt="C++17" src="https://img.shields.io/badge/C%2B%2B17-00599C?style=flat-square&labelColor=0b1220" />
  <img alt="Go" src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&labelColor=0b1220" />
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&labelColor=0b1220" />
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&labelColor=0b1220" />
</p>

> [!NOTE]
> **Availability (Nov–Dec 2026):** Stepping back from active GitHub contributions for ~2 months. Responses to issues and PR reviews may be delayed until January 2027.

---

## 1 · Flagship Project — [Orhun (`orhunlang/orhun`)](https://github.com/orhunlang/orhun)

A Turkish-first programming language runtime with native UTF-8 lexical analysis, teaching diagnostics, dual execution engines (tree-walk interpreter + bytecode VM), and a clear path from a C++17 bootstrap core toward self-hosting.

<p align="center">
  <img src="./card-orhun.svg" width="100%" alt="Orhun terminal demo" />
</p>

| Layer | Implementation Details |
| :--- | :--- |
| **Language Contract** | Stable `1.0` specification · `v1.1.0` current release · `.oh` source files |
| **Execution Pipeline** | `Lexer` → `AST Parser` → `Tree-Walk Interpreter` → `Bytecode Compiler` → `Stack VM` → `Standard Library` |
| **Core & Tooling** | Written in **C++17** · UTF-8 Turkish keywords (`işlev`, `eğer`, `döndür`, `tip`) with English aliases · Package verification & CLI tooling |
| **CI/CD & Ecosystem** | Cross-platform CI (Linux, macOS, Windows) · Official GitHub Action: [**`orhunlang/setup-orhun`**](https://github.com/orhunlang/setup-orhun) |

```bash
# Install on Linux / macOS
curl -fsSL https://raw.githubusercontent.com/orhunlang/orhun/v1.1.0/install.sh | bash
```

```powershell
# Install on Windows (PowerShell)
irm https://raw.githubusercontent.com/orhunlang/orhun/v1.1.0/install.ps1 | iex
```

<p>
  → <a href="https://github.com/orhunlang/orhun"><b>Repository</b></a> ·
  <a href="https://github.com/orhunlang/orhun/tree/main/docs"><b>Documentation</b></a> ·
  <a href="https://github.com/orhunlang/orhun/blob/main/docs/PROJECT_STATUS.md"><b>Project Status &amp; Roadmap</b></a> ·
  <a href="https://github.com/orhunlang/orhun/blob/main/docs/CHEATSHEET.md"><b>Language Cheatsheet</b></a> ·
  <a href="https://github.com/orhunlang/setup-orhun"><b>setup-orhun Action</b></a>
</p>

---

## 2 · Selected Open-Source Engineering

Focusing on compiler/IR codegen, graph data structures & algorithms, static analysis rules, and developer CLI infrastructure:

| Area & Repository | Technical Problem Solved | Pull Requests |
| :--- | :--- | :--- |
| **GPU Shader & Compute IR**<br/>[`CrossGL/crosstl`](https://github.com/CrossGL/crosstl) *(Python / CUDA / HIP)* | • Fixed CUDA builtin scalar type conversion for `f64` and numeric casts during IR codegen.<br/>• Emitted pointer targets instead of by-value operands for HIP system-scoped atomics (`atomic*_system`).<br/>• Added `crosstl doctor` environment & backend toolchain verifier. | [#2771](https://github.com/CrossGL/crosstl/pull/2771) *(Merged)*<br/>[#2760](https://github.com/CrossGL/crosstl/pull/2760) *(Merged)* |
| **Graph Algorithms & DAGs**<br/>[`hmdsefi/gograph`](https://github.com/hmdsefi/gograph) *(Go)* | • Enforced `ErrNotDirected` invariant on topological sort over undirected graphs.<br/>• Cleared dangling incident edges on vertex removal and documented neighbor snapshot semantics.<br/>• Bounded shortest-path priority queue allocations and preserved edge indexes in induced subgraphs & custom directed graphs. | [#281](https://github.com/hmdsefi/gograph/pull/281) *(Merged)*<br/>[#275](https://github.com/hmdsefi/gograph/pull/275) *(Merged)*<br/>[#273](https://github.com/hmdsefi/gograph/pull/273) *(Merged)*<br/>[#272](https://github.com/hmdsefi/gograph/pull/272) *(Merged)*<br/>[#271](https://github.com/hmdsefi/gograph/pull/271) *(Merged)* |
| **Service Orchestration CLI**<br/>[`flisk-sh/flisk`](https://github.com/flisk-sh/flisk) *(TypeScript)* | • Eliminated redundant per-command filesystem discovery scans in the CLI hot path.<br/>• Built deterministic verification & unit test suites across Tilt Starlark codegen, L4 health probes, port-listener fallback, crashloop recovery, and secret redaction (**33 merged PRs · Top-3 contributor**). | [#1690](https://github.com/flisk-sh/flisk/pull/1690) *(Merged)*<br/>[#1878](https://github.com/flisk-sh/flisk/pull/1878) *(Merged)*<br/>[#1893](https://github.com/flisk-sh/flisk/pull/1893) *(Merged)*<br/>[All 33 Merged PRs](https://github.com/flisk-sh/flisk/pulls?q=is%3Apr+author%3Ayoreva-01+is%3Amerged) |
| **Security & Static Analysis**<br/>[`GauravKarakoti/SecureFlow`](https://github.com/GauravKarakoti/SecureFlow) *(TypeScript)* | • Fixed recursive glob matcher so `**` only acts as a multi-segment wildcard on full path-segment boundaries, preventing false path matches. | [#1450](https://github.com/GauravKarakoti/SecureFlow/pull/1450) *(Merged)* |
| **LLM Schema Optimizer**<br/>[`rakeshnitb23/toolism`](https://github.com/rakeshnitb23/toolism) *(Python)* | • Implemented `SL103 drop-titles` annotation-level schema slimmer, end-to-end savings measurement examples, and offline tokenizer regression tests. | [#47](https://github.com/rakeshnitb23/toolism/pull/47) *(Merged)*<br/>[#50](https://github.com/rakeshnitb23/toolism/pull/50) *(Merged)*<br/>[#49](https://github.com/rakeshnitb23/toolism/pull/49) *(Merged)* |
| **Agent Hooks & Diagnostics**<br/>[`nrzz/claude-chat-ferry`](https://github.com/nrzz/claude-chat-ferry) · [`claude-md-doctor`](https://github.com/nrzz/claude-md-doctor) · [`everyhook`](https://github.com/nrzz/everyhook) *(Node.js)* | • Built Gemini CLI session reader (`claude-chat-ferry` v1.1.0), `pyproject.toml` `pdm`/`hatch`/`poe` task checker (`claude-md-doctor` v1.1.0), and Rust Cargo starter kit (`claude-code-starter-kits` v1.1.0).<br/>• Added contract-event (`--event`), hook-name (`--hook`), and problem-only (`--problems`) filters across local-first zero-token agent CLIs (**16 merged PRs**). | [chat-ferry #2](https://github.com/nrzz/claude-chat-ferry/pull/2) · [md-doctor #4](https://github.com/nrzz/claude-md-doctor/pull/4) · [starter-kits #4](https://github.com/nrzz/claude-code-starter-kits/pull/4)<br/>[everyhook #8](https://github.com/nrzz/everyhook/pull/8) · [windows-doctor #14](https://github.com/nrzz/claude-windows-doctor/pull/14) · [session-tidy #13](https://github.com/nrzz/claude-session-tidy/pull/13) |

---

## 3 · Engineering Principles

```text
quiet focus      →  ship the smallest change that removes a real technical blocker
clean contracts  →  explicit invariants beat cleverness; document the sharp edges
evidence first   →  verify against real binaries, compilers, and regression tests
local first      →  deterministic tools that run offline with zero wasted tokens
fail loudly      →  a silent fallback in a compiler or systems tool is a landmine
```

<p align="center">
  <i>"If a tool can’t explain why it did something, it isn’t done."</i>
</p>

<p align="center">
  <a href="https://github.com/orhunlang/orhun"><b>Orhun Language</b></a> ·
  <a href="https://github.com/orhunlang/setup-orhun"><b>setup-orhun</b></a> ·
  <a href="https://github.com/orhunlang"><b>@orhunlang</b></a>
</p>
