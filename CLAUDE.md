# CODITECT Core Framework - Claude Code Configuration

## Project Overview

**CODITECT Core Framework** is the distributable package of the CODITECT AI development framework, designed for external projects and organizations to integrate CODITECT capabilities into their workflows. This is the extraction and packaging layer that makes CODITECT accessible beyond the internal ecosystem.

### Purpose

- **Framework Distribution:** Package and distribute CODITECT's AI agents, skills, and commands for external use
- **External Integration:** Enable third-party projects to leverage CODITECT's distributed intelligence architecture
- **Standardized API:** Provide a clean, documented interface for framework capabilities
- **Version Management:** Control versioned releases of framework components for stability
- **Onboarding Simplification:** Reduce complexity for new adopters with packaged, tested components

### Development Status

**Status:** Stub (Early Development)

This repository is currently in planning phase with placeholder documentation. The core functionality is maintained in `coditect-core` and will be extracted and packaged here for distribution.

---

## Ecosystem Role

### Position in CODITECT Architecture

```
coditect-core (THE BRAIN)
         |
         v
coditect-core-framework (DISTRIBUTION PACKAGE)
         |
         v
External Projects / Third-Party Users
```

### Dependencies

**Depends On:**
- `coditect-core` - Source of all framework components

**Used By:**
- External projects adopting CODITECT
- Third-party integrations
- Enterprise customers (planned)

---

## Technology Stack

### Planned Technologies

| Component | Technology | Purpose |
|-----------|------------|---------|
| Package Format | Python Package (pip) | Standard distribution |
| Configuration | YAML/JSON | Framework configuration |
| Documentation | Sphinx | API documentation |
| Testing | pytest | Package validation |
| Versioning | Semantic Versioning | Release management |

### Future Components

- **CLI Tools:** Command-line interface for framework management
- **Configuration Validators:** Schema validation for framework configs
- **Migration Scripts:** Upgrade tools between versions
- **Integration Templates:** Starter templates for common use cases

---

## Key Features

- **Packaged AI Agents:** Pre-configured specialized agents for common development tasks
- **Reusable Skills Library:** Modular skills that can be composed into workflows
- **Command Catalog:** Ready-to-use slash commands for Claude Code integration
- **Configuration Templates:** Standard configurations for rapid project setup
- **Documentation Bundle:** Comprehensive guides for framework adoption

---

## Directory Structure

```
coditect-core-framework/
├── .coditect -> ../../../.coditect   # Distributed intelligence symlink
├── .claude -> .coditect               # Claude Code compatibility
├── PROJECT-PLAN.md                    # Development roadmap
├── README.md                          # User-facing documentation
├── TASKLIST.md                        # Progress tracking
├── CLAUDE.md                          # This file - AI agent configuration
│
├── src/                               # (Planned) Package source
│   ├── agents/                        # Packaged agents
│   ├── skills/                        # Packaged skills
│   ├── commands/                      # Packaged commands
│   └── templates/                     # Configuration templates
│
├── docs/                              # (Planned) Documentation
│   ├── getting-started/               # Quick start guides
│   ├── api-reference/                 # API documentation
│   └── examples/                      # Usage examples
│
├── tests/                             # (Planned) Package tests
└── setup.py                           # (Planned) Package configuration
```

---

## Distributed Intelligence

### Symlink Architecture

This repository participates in CODITECT's distributed intelligence system:

```
.coditect -> ../../../.coditect
```

This symlink provides:
- Access to 50+ specialized AI agents
- 72 slash commands for workflow automation
- 24 reusable skills
- Shared context and memory systems

### Why This Matters

Even as a distribution package, the repository benefits from the shared brain, enabling:
- Consistent AI assistance during development
- Access to orchestration capabilities
- Automated documentation and testing agents

---

## Development Guidelines

### Code Standards

- Follow Python packaging best practices (PEP 517/518)
- Maintain backward compatibility within major versions
- Document all public APIs with docstrings and examples
- Include type hints for all function signatures

### Documentation Standards

- Every public function must have docstring documentation
- Include usage examples for all major features
- Maintain changelog for version tracking
- Provide migration guides between versions

### Package Development

When building this package:
1. Extract components from `coditect-core`
2. Add proper packaging metadata
3. Create comprehensive tests
4. Generate API documentation
5. Validate against real-world use cases

---

## Quick Start

### Prerequisites

- Python 3.9+
- Git
- pip or poetry

### Installation (Planned)

```bash
# Install from PyPI (planned)
pip install coditect-framework

# Install from source
git clone https://github.com/coditect-ai/coditect-core-framework.git
cd coditect-core-framework
pip install -e .
```

### Basic Usage (Planned)

```python
from coditect import Framework

# Initialize framework
framework = Framework()

# Load agents
framework.load_agents(['code-architect', 'test-engineer'])

# Execute workflow
result = framework.execute_workflow('code-review')
```

### Development Setup

```bash
# Clone the repository
git clone https://github.com/coditect-ai/coditect-core-framework.git
cd coditect-core-framework

# Install development dependencies (planned)
pip install -e ".[dev]"

# Run tests (planned)
pytest
```

---

## Testing Approach

### Test Categories

1. **Unit Tests:** Individual component validation
2. **Integration Tests:** Component interaction testing
3. **Package Tests:** Distribution package validation
4. **Compatibility Tests:** Cross-version compatibility

### Test Execution (Planned)

```bash
# Run all tests
pytest

# Run specific test category
pytest tests/unit/
pytest tests/integration/

# Run with coverage
pytest --cov=coditect_framework
```

---

## AI Agent Guidelines

### When Working in This Repository

1. **Understand Package Purpose**
   - This is a distribution package, not the source of truth
   - Changes should align with packaging and distribution goals
   - Coordinate major changes with `coditect-core`

2. **Focus on Packaging Excellence**
   - Ensure clean API boundaries
   - Write comprehensive documentation
   - Create helpful error messages
   - Build thorough test coverage

3. **Maintain Compatibility**
   - Document breaking changes clearly
   - Provide migration paths
   - Test against multiple Python versions
   - Validate packaging metadata

4. **Documentation Priority**
   - This is an external-facing package
   - Documentation quality is paramount
   - Include examples for all features
   - Write clear getting-started guides

### Recommended Reading Order

1. `README.md` - Understand the user-facing documentation
2. `PROJECT-PLAN.md` - Review development roadmap
3. `TASKLIST.md` - Check current progress
4. `coditect-core` documentation - Understand the source

---

## Common Tasks

### Extract Agent for Packaging

```python
# Copy agent from dotclaude to framework
# 1. Read agent definition
# 2. Adapt for standalone use
# 3. Add packaging metadata
# 4. Create tests
# 5. Document API
```

### Create New Template

```bash
# 1. Identify common use case
# 2. Create template configuration
# 3. Add to templates directory
# 4. Document usage
# 5. Add to tests
```

### Version Release

```bash
# 1. Update version in setup.py
# 2. Update CHANGELOG.md
# 3. Run full test suite
# 4. Build distribution
# 5. Tag release
# 6. Publish to PyPI
```

---

## Integration Points

### With coditect-core

- Extract and package components
- Sync updates from source
- Maintain version mapping

### With External Projects

- Provide installation scripts
- Support configuration migration
- Enable feature detection

---

## Future Enhancements

### Short-term (1-3 months)

- [ ] Define package structure
- [ ] Extract core agents
- [ ] Create initial documentation
- [ ] Build test framework

### Medium-term (3-6 months)

- [ ] PyPI publication
- [ ] Plugin system
- [ ] Configuration GUI
- [ ] Integration templates

### Long-term (6-12 months)

- [ ] Enterprise features
- [ ] Custom agent marketplace
- [ ] Training/certification integration
- [ ] Multi-language support

---

## Support & Resources

### Documentation

- **README.md** - User-facing overview
- **PROJECT-PLAN.md** - Development roadmap
- **TASKLIST.md** - Current progress

### Related Repositories

- **coditect-core** - Source framework
- **coditect-core-architecture** - Architectural standards
- **coditect-docs-main** - Documentation site

### Contact

- **Repository:** https://github.com/coditect-ai/coditect-core-framework
- **Owner:** AZ1.AI INC
- **License:** Proprietary - AZ1.AI INC

---

**Last Updated:** November 20, 2025
**Status:** Stub (Early Development)
**Next Milestone:** Package Structure Definition
**Owner:** AZ1.AI INC
