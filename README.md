# CSO Standalone Skill

Standalone Chief Security Officer security review skill adapted from the gstack
CSO workflow.

This skill runs a read-only, infrastructure-first audit covering:

- secrets and repository hygiene
- dependencies and supply chain
- CI/CD and release pipeline security
- authentication and authorization
- OWASP Top 10 and STRIDE threat modeling
- LLM, agent, MCP, and skill supply-chain risks

It does not require gstack binaries, telemetry, routing, update checks, or
`~/.gstack` state.

## Installation

Copy `SKILL.md` into your agent skills directory under a `cso` folder.

For Codex:

```bash
mkdir -p ~/.codex/skills/cso
cp SKILL.md ~/.codex/skills/cso/SKILL.md
```

For Claude-style skill directories:

```bash
mkdir -p ~/.claude/skills/cso
cp SKILL.md ~/.claude/skills/cso/SKILL.md
```

## Usage

Invoke the skill with any of:

```text
/cso
/cso --comprehensive
/cso --diff
/cso --infra
/cso --code
/cso --skills
/cso --supply-chain
/cso --owasp
```

Without flags, the skill runs a daily audit and reports only findings with
confidence 8/10 or higher. Use `--comprehensive` for broader threat discovery
with tentative findings included.

## Source Note

This standalone skill is adapted for local use from the public gstack CSO
concept:

https://github.com/garrytan/gstack/tree/main/cso
