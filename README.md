# Tenant Isolation Reviewer

**English** | [Português (Brasil)](README.pt-BR.md)

An agent skill that reviews **data isolation between users and tenants** (IDOR / broken access control, focused on ownership).

It discovers the project's access model, compares each endpoint with the canonical pattern and reports confirmed IDORs and hardening gaps.

The skill is **read-only**: it analyzes and reports without editing files.

It follows the open [Agent Skills](https://agentskills.io) format (`SKILL.md` with `name` and `description` frontmatter) and works with Claude Code, Cursor and other compatible agents. The skill instructions are written in Brazilian Portuguese.

## Installation

The target folder must be named `tenant-isolation-reviewer` (the skill name), not the repository name.

### Claude Code

```bash
# All projects
git clone https://github.com/jrcarls/skill-tenant-isolation-reviewer.git ~/.claude/skills/tenant-isolation-reviewer

# A single project
git clone https://github.com/jrcarls/skill-tenant-isolation-reviewer.git .claude/skills/tenant-isolation-reviewer
```

### Cursor

```bash
git clone https://github.com/jrcarls/skill-tenant-isolation-reviewer.git .cursor/skills/tenant-isolation-reviewer
```

## Usage

The agent loads the skill automatically when the task matches its description. To invoke it explicitly in Claude Code:

```text
/tenant-isolation-reviewer
```

## Related skills

This skill is part of a complementary set:

- `skill-owasp-security-reviewer` — OWASP Top 10
- `skill-llm-security-reviewer` — OWASP LLM Top 10
- `skill-tenant-isolation-reviewer` — IDOR / ownership
- `skill-lgpd-compliance-advisor` — LGPD compliance
- `skill-qa-verifier` — functional verification
- `skill-vue-reviewer` — Vue frontend review

## License

[MIT](LICENSE)
