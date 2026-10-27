# Ilorium agent kit

**Planned.** Nothing here runs yet. This repository holds the design and the empty structure; there is no skill, no plugin and no server until the first protocol release is published and these are generated from it.

The agent kit is how agents and people find and use Ilorium without scraping a web page: a skill (a folder with a `SKILL.md`), a plugin that packages it, and a deterministic MCP server named `ilorium`. It belongs to the Lighthouse (`specs/discovery-and-growth-v1.md` in the [protocol repository](https://github.com/ilorium-protocol/protocol)). It is not part of the protocol.

| Directory | What it will hold | Status |
| --- | --- | --- |
| `skill/` | A skill for Claude Code and other agents: read a Spore, read Vital Signs, verify an Evidence Bundle, start an adoption. Read-only. No hidden instructions. | planned |
| `plugin/` | A package that bundles the skill and points at the MCP server. | planned |
| `mcp/` | The `ilorium` MCP server. Deterministic: it calls no language model, so answering costs no tokens. | planned |

## Rules

- **Generated, not edited.** The skill and the descriptor are generated from a release (`protocol/<tag>`) in CI, so they never go stale. Hand edits are rejected. The generation job is designed but not implemented (`DESIGN.md`).
- **Read-only.** The kit never writes to an organism, never holds a key, never publishes.
- **No hidden instructions for agents.** Whatever an agent reads here, a person can read too (the Lighthouse rule).
- **Listing in directories** of each platform is done by the founder, with his own accounts, after checking each directory's current terms.

Status: release 1.0, draft. Interim governance. License: Apache-2.0.
