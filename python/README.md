# Python Formatter Configurations

This directory contains formatter and linter configurations for Python projects.

## Files

- **`ruff.toml`**: Modern Python linter and formatter configuration (Ruff)
- **`.style.yapf`**: Code formatting configuration for YAPF (Yet Another Python Formatter)

## About the Configurations

### ruff.toml
Ruff is a fast Python linter and formatter written in Rust. This configuration provides:
- **Line length**: 110 characters
- **Quote style**: Double quotes (Google style)
- **Indentation**: 4 spaces
- **Import sorting**: Combined imports with trailing comma splitting
- **Linting rules**: Includes pycodestyle, pyflakes, isort, pyupgrade, and more
- **Docstring convention**: Google style

**Selected lint rules:**
- `E`, `F`: pycodestyle errors and pyflakes
- `I`: isort import sorting
- `UP`: pyupgrade modernization
- `B`: flake8-bugbear bug detection
- `C4`: flake8-comprehensions
- `SIM`: flake8-simplify
- `PIE`: flake8-pie
- `TC`: flake8-type-checking
- `PERF`: performance optimizations
- `RUF100`: Ruff-specific rules

### .style.yapf
YAPF (Yet Another Python Formatter) configuration based on Google style:
- **Line length**: 110 characters
- **Indentation**: 4 spaces, no tabs
- **Style base**: Google Python style guide
- **Bracket handling**: Custom alignment and splitting rules
- **Comment spacing**: 3 spaces before comments

## Usage

### Ruff
```bash
# Install ruff
pip install ruff

# Format code
ruff format .

# Run linter
ruff check .

# Fix auto-fixable issues
ruff check --fix .
```

### YAPF
```bash
# Install yapf
pip install yapf

# Format a file
yapf -i file.py

# Format entire directory
yapf -ir .

# Check formatting (dry run)
yapf -d -r .
```

## IDE Integration

### VS Code
- **Ruff**: Install "Ruff" extension by Astral Software
- **YAPF**: Install "Python" extension and configure YAPF as formatter

### PyCharm/IntelliJ
- **Ruff**: Install "Ruff" plugin
- **YAPF**: Configure in Settings → Tools → External Tools

### Vim/Neovim
- Use plugins like `ruff-lsp` or `yapf.vim`

## Project Setup

### Using Ruff (Recommended)
1. Place `ruff.toml` in your project root
2. Install ruff: `pip install ruff`
3. Add to your CI/CD pipeline or pre-commit hooks

### Using YAPF
1. Place `.style.yapf` in your project root
2. Install yapf: `pip install yapf`
3. Configure your editor to use YAPF

## Pre-commit Integration

Add to your `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.1.0
    hooks:
      - id: ruff
        args: [--fix]
      - id: ruff-format

  # Or for YAPF:
  - repo: https://github.com/pre-commit/mirrors-yapf
    rev: v0.32.0
    hooks:
      - id: yapf
```

## Compatibility

Both configurations are designed to work well together and maintain consistency with:
- Google Python Style Guide
- PEP 8 standards
- Modern Python best practices
