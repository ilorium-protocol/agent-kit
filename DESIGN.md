# Design (planned, not implemented)

1. A protocol release is tagged in the protocol repository (`protocol/<tag>`), signed by the founder.
2. A workflow here, triggered by that tag (or run by hand with the tag as input), checks out the tagged documents and the machine forms (`schemas/`, `vectors/`).
3. A generator, standard library only, writes `skill/SKILL.md`, the plugin manifest and the MCP tool descriptions from those files. Nothing is written by hand.
4. The workflow opens a pull request on `main` labeled `agent-authored`. It does not merge. The founder reviews, signs and merges.
5. The MCP server reads the generated data and the verifier's output; it does not interpret the protocol itself. It answers with documents and tool results, never with a model's prose.

Open questions, to be settled by the Architecture role with an ADR before any code: the language of the server (the Probe is Go, the verifier is Python), how it reaches the verifier, how the plugin is packaged for each platform.
