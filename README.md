# Codex Skills

Engineering skills for disciplined Rust/WebAssembly development with [OpenAI Codex CLI](https://github.com/openai/codex).

## Installation

### Global Installation (All Projects)

```bash
# Clone the repository
git clone https://github.com/terraphim/codex-skills.git

# Copy skills to Codex home directory
cp -r codex-skills/skills/* ~/.codex/skills/
```

### Per-Project Installation

```bash
# Copy to project's .codex directory
mkdir -p .codex/skills
cp -r codex-skills/skills/* .codex/skills/
```

### Using Skill Installer

If you have the `$skill-installer` skill available:

```
$skill-installer terraphim/codex-skills
```

## Usage

Skills are automatically discovered by Codex CLI. Use them explicitly with `$skill-name` or let Codex select them implicitly based on your task.

```bash
# List available skills
codex /skills

# Use a skill explicitly in your prompt
codex "use $disciplined-research to analyze this codebase"
```

## Available Skills (30)

### Disciplined Development (V-Model)

| Skill | Phase | Description |
|-------|-------|-------------|
| `disciplined-research` | 1 | Deep problem understanding before design |
| `disciplined-design` | 2 | Create implementation plans from research |
| `disciplined-specification` | 2.5 | Probe specs through user interviews |
| `disciplined-implementation` | 3 | Execute plans step by step with tests |
| `disciplined-verification` | 4 | Unit/integration testing with traceability |
| `disciplined-validation` | 5 | UAT and stakeholder sign-off |

### Core Development

| Skill | Description |
|-------|-------------|
| `architecture` | System design, ADRs, API planning (no code) |
| `implementation` | Production-ready code with tests |
| `testing` | Unit, integration, property-based tests |
| `debugging` | Systematic root cause analysis |

### Rust Expertise

| Skill | Description |
|-------|-------------|
| `rust-development` | Idiomatic Rust patterns and ecosystem |
| `rust-performance` | Profiling, benchmarking, optimization |

### Quality & Security

| Skill | Description |
|-------|-------------|
| `code-review` | Bug, security, performance feedback |
| `security-audit` | Vulnerability assessment, unsafe code review |
| `git-safety-guard` | Block destructive git/filesystem commands |
| `quality-gate` | Orchestrates verification/validation |
| `requirements-traceability` | REQ to test traceability matrix |
| `acceptance-testing` | UAT plans and scenarios |
| `visual-testing` | Visual regression testing |

### Documentation & DevOps

| Skill | Description |
|-------|-------------|
| `documentation` | API docs, README, guides |
| `md-book` | MD-Book documentation sites |
| `devops` | CI/CD, Docker, GitHub Actions |

### Open Source

| Skill | Description |
|-------|-------------|
| `open-source-contribution` | Quality PRs, good issues |
| `community-engagement` | Release notes, contributor engagement |

### Terraphim Integration

| Skill | Description |
|-------|-------------|
| `terraphim-hooks` | Knowledge graph text replacement |
| `session-search` | AI session history search |
| `local-knowledge` | Personal notes search |

### Desktop UI

| Skill | Description |
|-------|-------------|
| `gpui-components` | GPUI components (Zed patterns) |

### Infrastructure

| Skill | Description |
|-------|-------------|
| `1password-secrets` | 1Password CLI secret management |
| `caddy` | Caddy server configuration |

## Skill Discovery

Codex loads skills by precedence (highest to lowest):

| Scope | Location |
|-------|----------|
| Module | `.codex/skills/` in current directory |
| Repository | `.codex/skills/` at repo root |
| User | `~/.codex/skills/` |
| System | `/etc/codex/skills/` |

## Related

| Repository | Platform | Installation |
|------------|----------|--------------|
| [terraphim/codex-skills](https://github.com/terraphim/codex-skills) | OpenAI Codex CLI | `~/.codex/skills/` |
| [terraphim/opencode-skills](https://github.com/terraphim/opencode-skills) | OpenCode | `~/.config/opencode/skill/` |
| [terraphim/terraphim-skills](https://github.com/terraphim/terraphim-skills) | Claude Code | Plugin marketplace |

## License

Apache-2.0
