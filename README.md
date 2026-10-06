# threadctx for Claude Code

Check what your coding agents are told, from inside Claude Code.

```
/plugin marketplace add threadctx-dev/claude-plugin
/plugin install threadctx@threadctx
```

## What you get

- **`/context-check`**: grade this repository's AGENTS.md, CLAUDE.md, Cursor rules, Copilot instructions,
  GEMINI.md and MCP configs, and list dead paths, undefined scripts, duplicated or conflicting instructions,
  hidden characters, secrets and unpinned MCP servers.
- **`/context-explain <file>`**: which instruction files Claude Code, Cursor, Copilot and Gemini each load for
  a file, in order, with token estimates.
- **`/context-fix`**: apply the safe, mechanical fixes and show the diff. Never commits.
- **A skill** that reminds Claude to check context files after editing them and to keep them minimal.
- **A read-only MCP server** (`check_context`, `get_effective_context`, `explain_rule`) so Claude can check its
  own instructions. It never writes files and makes no network calls.

The MCP server runs `npx -y threadctx@0.2.1 mcp`, pinned to an exact version.

Same engine on the command line: `npx threadctx scan` ([npm](https://www.npmjs.com/package/threadctx)),
and on pull requests: [threadctx-dev/action](https://github.com/threadctx-dev/action).

Licence: Apache-2.0.
