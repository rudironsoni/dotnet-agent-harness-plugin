# dotnet-harness-plugin

Distribution packages for [dotnet-harness](https://github.com/rudironsoni/dotnet-harness) — comprehensive .NET development guidance for modern C#, ASP.NET Core, MAUI, Blazor, and cloud-native apps.

## What's included

- **131 skills** — deep guidance on .NET patterns, architectures, and frameworks
- **14 specialist agents** — architect, security reviewer, performance analyst, testing specialist, and more
- **Commands, hooks, and MCP config** — full development workflow support

## Installation

### Via RuleSync (recommended)

```bash
rulesync fetch rudironsoni/dotnet-harness:.rulesync
rulesync generate --targets "*" --features "*"
```

Or with declarative sources in `rulesync.jsonc`:

```jsonc
{
  "sources": [{ "source": "rudironsoni/dotnet-harness", "path": ".rulesync" }],
}
```

```bash
rulesync install && rulesync generate --targets "*" --features "*"
```

### Per-platform zip bundles

Download the zip for your AI coding agent from the [latest release](https://github.com/rudironsoni/dotnet-harness-plugin/releases/latest) and extract into your project root:

| Platform       | Bundle                           | Extract to                 |
| -------------- | -------------------------------- | -------------------------- |
| Claude Code    | `dotnet-harness-claudecode.zip`  | `.claude/`                 |
| OpenCode       | `dotnet-harness-opencode.zip`    | `.opencode/` + `AGENTS.md` |
| GitHub Copilot | `dotnet-harness-copilot.zip`     | `.github/`                 |
| Codex CLI      | `dotnet-harness-codexcli.zip`    | `.codex/` + `AGENTS.md`    |
| Gemini CLI     | `dotnet-harness-geminicli.zip`   | `.gemini/` + `GEMINI.md`   |
| Antigravity    | `dotnet-harness-antigravity.zip` | `.agent/`                  |
| AGENTS.md      | `dotnet-harness-agentsmd.zip`    | `.agents/` + `AGENTS.md`   |

### Platform npm packages

```bash
npm config set @rudironsoni:registry https://npm.pkg.github.com
```

- OpenCode: `@rudironsoni/dotnet-harness-opencode`
- Claude Code: `@rudironsoni/dotnet-harness-claudecode`
- GitHub Copilot: `@rudironsoni/dotnet-harness-copilot`
- Codex CLI: `@rudironsoni/dotnet-harness-codexcli`
- Gemini CLI: `@rudironsoni/dotnet-harness-geminicli`
- AGENTS.md: `@rudironsoni/dotnet-harness-agentsmd`
- Antigravity: `@rudironsoni/dotnet-harness-antigravity`

OpenCode plugin install example:

```bash
npm install @rudironsoni/dotnet-harness-opencode
```

For private package authentication, configure a GitHub token with `read:packages` in your `.npmrc`.

Then add to your `opencode.json`:

```json
{
  "plugins": {
    "dotnet-harness": "@rudironsoni/dotnet-harness-opencode"
  }
}
```

## Supported platforms

| Platform       | Rules | Commands | Subagents | Skills | MCP | Hooks |
| -------------- | ----- | -------- | --------- | ------ | --- | ----- |
| Claude Code    | ✅    | ✅       | ✅        | ✅     | ✅  | ✅    |
| OpenCode       | ✅    | ✅       | ✅        | ✅     | ✅  | ✅    |
| GitHub Copilot | ✅    | ✅       | ✅        | ✅     | ✅  |       |
| Codex CLI      | ✅    | ✅       | ✅        | ✅     | ✅  |       |
| Gemini CLI     | ✅    | ✅       |           | ✅     | ✅  |       |
| Antigravity    | ✅    | ✅       |           | ✅     |     |       |
| AGENTS.md      | ✅    |          |           | ✅     |     |       |

## Source

This repo contains distribution packages only. Source content lives in [dotnet-harness](https://github.com/rudironsoni/dotnet-harness).

## License

MIT
