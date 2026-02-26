# dotnet-agent-harness-plugin

Distribution packages for [dotnet-agent-harness](https://github.com/rudironsoni/dotnet-agent-harness) — comprehensive .NET development guidance for modern C#, ASP.NET Core, MAUI, Blazor, and cloud-native apps.

## What's included

- **131 skills** — deep guidance on .NET patterns, architectures, and frameworks
- **14 specialist agents** — architect, security reviewer, performance analyst, testing specialist, and more
- **Commands, hooks, and MCP config** — full development workflow support

## Installation

### Via RuleSync (recommended)

```bash
rulesync fetch rudironsoni/dotnet-agent-harness:.rulesync
rulesync generate --targets "*" --features "*"
```

Or with declarative sources in `rulesync.jsonc`:

```jsonc
{
  "sources": [
    { "source": "rudironsoni/dotnet-agent-harness", "path": ".rulesync" }
  ]
}
```

```bash
rulesync install && rulesync generate --targets "*" --features "*"
```

### Per-platform zip bundles

Download the zip for your AI coding agent from the [latest release](https://github.com/rudironsoni/dotnet-agent-harness-plugin/releases/latest) and extract into your project root:

| Platform | Bundle | Extract to |
|---|---|---|
| Claude Code | `dotnet-agent-harness-claudecode.zip` | `.claude/` |
| OpenCode | `dotnet-agent-harness-opencode.zip` | `.opencode/` + `AGENTS.md` |
| GitHub Copilot | `dotnet-agent-harness-copilot.zip` | `.github/` |
| Codex CLI | `dotnet-agent-harness-codexcli.zip` | `.codex/` + `AGENTS.md` |
| Gemini CLI | `dotnet-agent-harness-geminicli.zip` | `.gemini/` + `GEMINI.md` |
| Antigravity | `dotnet-agent-harness-antigravity.zip` | `.agent/` |
| AGENTS.md | `dotnet-agent-harness-agentsmd.zip` | `.agents/` + `AGENTS.md` |

### OpenCode npm plugin

```bash
npm install @dotnet-agent-harness/opencode-plugin
```

Then add to your `opencode.json`:

```json
{
  "plugins": {
    "dotnet-agent-harness": "@dotnet-agent-harness/opencode-plugin"
  }
}
```

## Supported platforms

| Platform | Rules | Commands | Subagents | Skills | MCP | Hooks |
|---|---|---|---|---|---|---|
| Claude Code | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| OpenCode | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| GitHub Copilot | ✅ | ✅ | ✅ | ✅ | ✅ | |
| Codex CLI | ✅ | ✅ | ✅ | ✅ | ✅ | |
| Gemini CLI | ✅ | ✅ | | ✅ | ✅ | |
| Antigravity | ✅ | ✅ | | ✅ | | |
| AGENTS.md | ✅ | | | ✅ | | |

## Source

This repo contains distribution packages only. Source content lives in [dotnet-agent-harness](https://github.com/rudironsoni/dotnet-agent-harness).

## License

MIT
