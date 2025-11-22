# coditect-core-framework

**Core Repository - AZ1.AI CODITECT Ecosystem**

---

## Overview

**coditect-core-framework** is the intended distributable version of the CODITECT framework, designed for external developers who want to adopt CODITECT patterns in their own projects. This repository will extract the essential agent, skill, and command patterns from `coditect-core` into a clean, packageable distribution suitable for standalone installation.

**Status:** Planning/Stub
**Category:** core
**Priority:** P1
**Type:** Library/Framework

---

## Purpose

### What Problem This Solves

Currently, the CODITECT framework exists as `coditect-core` - a comprehensive but complex system with 50 specialized AI agents, 72 slash commands, and 24 reusable skills. While powerful, this full system is tightly integrated with the AZ1.AI ecosystem and requires understanding of:

- Git submodule management
- Symlink architecture patterns
- Project-specific `.claude/` configurations
- MEMORY-CONTEXT session management

**coditect-core-framework** will provide a streamlined entry point for external developers who want to:

1. **Adopt CODITECT patterns** without the full ecosystem
2. **Start with a minimal footprint** and scale up as needed
3. **Integrate specific agents or skills** into existing projects
4. **Learn the architecture** before committing to full adoption

### Target Audience

| Audience | Use Case |
|----------|----------|
| **External Developers** | Integrate CODITECT patterns into personal/company projects |
| **AI Engineers** | Study agent orchestration and skill composition patterns |
| **Framework Evaluators** | Test CODITECT capabilities in isolated environment |
| **Open Source Contributors** | Build extensions or customizations |

### How It Fits Into CODITECT

```
CODITECT Ecosystem Distribution
================================

coditect-core          coditect-core-framework
(Internal Full System)           (External Distribution)
        |                                |
        v                                v
+------------------+            +------------------+
| 50 Agents        |            | Core Agents      |
| 72 Commands      | =========> | Essential Cmds   |
| 24 Skills        |  Extract   | Key Skills       |
| Training (240K)  |            | Quickstart Docs  |
| Full Ecosystem   |            | Standalone PKG   |
+------------------+            +------------------+
        |                                |
   Used by AZ1.AI                  Used by External
   Internal Projects               Developers
```

---

## Key Features

- **Modular Agent System** - Select only the agents you need
- **Packageable Distribution** - pip install, npm package, or direct download
- **Standalone Operation** - Works without full CODITECT ecosystem
- **Configuration Templates** - Pre-built `.claude/` configurations for common use cases
- **Migration Guides** - Paths to upgrade to full CODITECT when ready
- **Example Projects** - Working demonstrations of framework usage

---

## Current Status

### What Exists Now

This repository is currently a **planning stub** containing:

```
coditect-core-framework/
├── .coditect -> ../../../.coditect    # Distributed intelligence symlink
├── .claude -> .coditect               # Claude Code compatibility
├── .git                               # Git submodule reference
├── .gitignore                         # Standard ignores
├── PROJECT-PLAN.md                    # Development roadmap (stub)
├── README.md                          # This file
└── TASKLIST.md                        # Task tracking
```

### What Will Be Built

The framework will be structured as:

```
coditect-core-framework/
├── agents/                            # Core agent definitions
│   ├── core/                          # Essential agents
│   │   ├── orchestrator.md
│   │   ├── code-analyst.md
│   │   └── documentation-writer.md
│   └── specialized/                   # Domain-specific agents
│
├── skills/                            # Reusable capabilities
│   ├── code-generation/
│   ├── testing/
│   └── documentation/
│
├── commands/                          # Slash commands
│   ├── development/
│   └── workflow/
│
├── templates/                         # Configuration templates
│   ├── minimal/                       # Basic setup
│   ├── standard/                      # Recommended setup
│   └── enterprise/                    # Full feature set
│
├── examples/                          # Working examples
│   ├── python-project/
│   ├── typescript-project/
│   └── rust-project/
│
├── docs/                              # Documentation
│   ├── quickstart.md
│   ├── architecture.md
│   ├── migration-guide.md
│   └── api-reference.md
│
├── scripts/                           # Automation
│   ├── install.sh
│   ├── setup-project.py
│   └── validate-config.py
│
├── dist/                              # Distribution packages
│   ├── pip/
│   └── npm/
│
├── README.md
├── CHANGELOG.md
├── LICENSE
└── pyproject.toml / package.json
```

---

## Technology Stack

### Planned Technologies

- **Language:** Python 3.11+, TypeScript (for distribution flexibility)
- **Package Format:** pip (PyPI), npm (for broader reach)
- **Configuration:** YAML/Markdown (matching Claude Code conventions)
- **Templating:** Jinja2 (for configuration generation)
- **Testing:** pytest, vitest
- **Documentation:** MkDocs or Sphinx

### Dependencies

**Runtime Dependencies:**
- Python 3.11+ or Node.js 18+
- Claude Code (Anthropic CLI)
- Git

**Development Dependencies:**
- pytest / vitest for testing
- black / prettier for formatting
- mypy / TypeScript for type checking

---

## Quick Start

### Current State (Stub)

Since this repository is in planning phase, there is no functional quick start yet.

### Planned Installation

Once developed, installation will be:

**Option 1: pip install (Python)**
```bash
pip install coditect-framework

# Initialize in your project
coditect init --template standard
```

**Option 2: npm install (Node.js)**
```bash
npm install -g @coditect/framework

# Initialize in your project
coditect init --template standard
```

**Option 3: Direct Download**
```bash
# Download and run setup
curl -fsSL https://coditect.ai/install.sh | bash

# Initialize in your project
./coditect-init.sh --template standard
```

### Planned Usage

```bash
# Create new project with CODITECT framework
mkdir my-project && cd my-project
coditect init --template standard

# This creates:
# .claude/
# ├── CLAUDE.md              # AI configuration
# ├── agents/                 # Selected agents
# │   └── orchestrator.md
# ├── skills/                 # Selected skills
# │   └── code-generation.md
# └── commands/               # Selected commands
#     └── help.md

# Use Claude Code with framework
claude "analyze this codebase using the orchestrator agent"
```

---

## Directory Structure

```
coditect-core-framework/
├── .coditect -> ../../../.coditect    # Distributed intelligence symlink
├── .claude -> .coditect               # Claude Code compatibility
├── PROJECT-PLAN.md                    # Development roadmap
├── README.md                          # This file
└── TASKLIST.md                        # Task tracking
```

**Note:** Full structure will be built during development phase.

---

## Distributed Intelligence

This repository is part of the CODITECT distributed intelligence architecture:

```
.coditect -> ../../../.coditect  # Links to master brain
.claude -> .coditect             # Claude Code compatibility
```

### How Symlinks Work

CODITECT uses a symlink chain pattern to share a single "brain" across all projects:

```
coditect-rollout-master/
├── .coditect                          # THE BRAIN (actual directory)
│   └── [50 agents, 72 commands, 24 skills]
│
└── submodules/
    └── core/
        └── coditect-core-framework/
            └── .coditect -> ../../../.coditect   # SYMLINK
```

### Benefits

- **Single source of truth** - All framework development uses same agents
- **Consistent patterns** - Same commands and skills everywhere
- **Access to 50 specialized AI agents** - Full CODITECT capability
- **72 slash commands available** - Complete workflow automation
- **24 reusable skills** - Proven development patterns

### Learn More

- [WHAT-IS-CODITECT.md](https://github.com/coditect-ai/coditect-core/blob/main/WHAT-IS-CODITECT.md) - Architecture documentation
- [ADR-001: Distributed Brain Architecture](../coditect-core-architecture/docs/adrs/ADR-001-distributed-brain.md) - Decision rationale

---

## Integration with CODITECT Platform

### Dependencies

This repository will extract from:

| Repository | What It Provides |
|------------|------------------|
| [coditect-core](../coditect-core) | Source agents, skills, commands |
| [coditect-core-architecture](../coditect-core-architecture) | Architectural patterns and ADRs |

### Dependents

Once developed, this will be used by:

- **External developers** - Via pip/npm installation
- **Open source community** - Framework evaluators and contributors
- **Partner integrations** - Third-party tool vendors

### Relationship to coditect-core

| Aspect | coditect-core | coditect-core-framework |
|--------|-------------------------|-------------------------|
| **Purpose** | Full internal system | External distribution |
| **Audience** | AZ1.AI team | External developers |
| **Size** | Complete (50 agents, 72 commands) | Curated subset |
| **Dependencies** | Full ecosystem | Standalone |
| **Installation** | Git submodule + symlinks | pip/npm package |
| **Updates** | Pull submodule | Package manager |

---

## Development Guidelines

### Code Style

- Follow Python PEP 8 / TypeScript best practices
- Use black / prettier for formatting
- Maintain type annotations throughout
- Document all public APIs

### Commit Messages

Follow conventional commit format:
```
type(scope): description

feat: new feature
fix: bug fix
docs: documentation
refactor: code refactoring
test: adding tests
chore: maintenance
```

### Pull Requests

1. Create feature branch from `main`
2. Write tests for new functionality
3. Update documentation as needed
4. Request review from framework team

---

## Testing

### Planned Test Strategy

```bash
# Run all tests
pytest tests/ -v

# Run specific test category
pytest tests/agents/ -v

# Generate coverage report
pytest --cov=coditect_framework --cov-report=html
```

### Test Categories

- **Unit tests** - Individual agent, skill, command validation
- **Integration tests** - Multi-component workflows
- **End-to-end tests** - Full project initialization and usage
- **Compatibility tests** - Python/Node version matrix

---

## Documentation

- **[PROJECT-PLAN.md](PROJECT-PLAN.md)** - Development roadmap and milestones
- **[TASKLIST.md](TASKLIST.md)** - Task tracking with checkboxes
- **[Architecture Guide](../coditect-core-architecture/)** - CODITECT architectural decisions

### Planned Documentation

Once developed:

- **Quickstart Guide** - Get running in 5 minutes
- **Architecture Overview** - How the framework works
- **API Reference** - Complete agent/skill/command documentation
- **Migration Guide** - Upgrade to full CODITECT ecosystem
- **Examples** - Working project demonstrations

---

## Roadmap

### Phase 1: Foundation (Planned)

- [ ] Define core agent subset for distribution
- [ ] Design package structure (pip/npm)
- [ ] Create configuration templates
- [ ] Build installation scripts
- [ ] Write quickstart documentation

### Phase 2: Implementation (Planned)

- [ ] Extract agents from coditect-core
- [ ] Create skill distribution
- [ ] Build command package
- [ ] Implement project initialization
- [ ] Write comprehensive tests

### Phase 3: Distribution (Planned)

- [ ] Publish to PyPI
- [ ] Publish to npm
- [ ] Create documentation site
- [ ] Set up CI/CD for releases
- [ ] Launch marketing materials

---

## Related Resources

### CODITECT Repositories

- **Master Repository:** [coditect-rollout-master](https://github.com/coditect-ai/coditect-rollout-master)
- **Core Brain:** [coditect-core](https://github.com/coditect-ai/coditect-core)
- **Architecture:** [coditect-core-architecture](https://github.com/coditect-ai/coditect-core-architecture)
- **Documentation Site:** [docs.coditect.ai](https://docs.coditect.ai) (when available)

### External Resources

- **Claude Code Documentation:** [docs.anthropic.com/claude-code](https://docs.anthropic.com/claude-code)
- **CODITECT Training:** [Training System](https://github.com/coditect-ai/coditect-core/blob/main/user-training/README.md)

---

## Contributing

### Current State

This repository is not yet accepting contributions as it's in planning phase.

### Future Contributions

Once development begins:

1. Fork the repository
2. Create feature branch
3. Follow code style guidelines
4. Write tests
5. Submit pull request

For CODITECT-wide contribution guidelines, see the [master repository](https://github.com/coditect-ai/coditect-rollout-master).

---

## FAQ

### Q: When will this be available?

This framework is currently in planning phase. Development will begin after Phase 1 of the CODITECT rollout (Weeks 1-16).

### Q: Can I use coditect-core directly instead?

Yes, but it requires understanding the full ecosystem including git submodule management and symlink architecture. This framework will provide a simpler onboarding path.

### Q: Will this be open source?

The distribution model is still being determined. It may be freemium (core free, premium agents paid) or fully open source with commercial support.

### Q: How do I upgrade to full CODITECT?

Migration guides will be provided to transition from this lightweight framework to the complete `coditect-core` ecosystem.

---

## License

Copyright (C) 2025 AZ1.AI INC. All Rights Reserved.

**PROPRIETARY AND CONFIDENTIAL** - This repository contains AZ1.AI INC. trade secrets and confidential information. Unauthorized copying, transfer, or use is strictly prohibited.

---

*Built with Excellence by AZ1.AI CODITECT*
*Systematic Development. Continuous Context. Exceptional Results.*
