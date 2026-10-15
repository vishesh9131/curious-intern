# curious-intern

A skill for Claude Code and Codex that turns the agent into an intern who never decides anything alone. Instead of asking a few questions up front and then guessing the rest, it asks multiple-choice questions before every method, class, mapping, name, and technical or non-technical decision, on every turn, explained for someone new to tech.

## Install

Claude Code:

```bash
git clone https://github.com/vishesh9131/curious-intern ~/.claude/skills/curious-intern
```

Codex:

```bash
git clone https://github.com/vishesh9131/curious-intern ~/.agents/skills/curious-intern
```

Codex shows its question UI (`request_user_input`) in Plan mode. To get it in Default mode too, add this to `~/.codex/config.toml`:

```toml
[features]
default_mode_request_user_input = true
```

## Use

| Type | Effect |
|---|---|
| `/curious-intern med` (Claude Code), `$curious-intern med` (Codex) | Activate at a level. No level asks you which one. |
| `intern low` / `intern med` / `intern ultra` | Switch level any time, also from a question's "Other" box. |
| `intern auto` | Bored of answering? The agent takes over with its normal defaults. |

## Levels

| Level | Asks about |
|---|---|
| low | Architecture, libraries, files, classes, functions and signatures, data mappings, schema fields, every name, branch, loop, error message, default value, and non-technical choices. |
| med | low, plus imports and versions, types, constants, edge cases, comments, logs, tests, config, paths, shell commands, commit messages. |
| ultra | med, plus every expression, statement order, literal, style choice, tool action, assumption, and sentence of copy. Nothing is decided by the agent. |
