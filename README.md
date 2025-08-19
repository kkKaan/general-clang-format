# Common Formatter Configurations

This repository contains formatter and linter configurations for multiple programming languages. Each configuration is designed to promote consistent, readable code across different projects while following established style guides and best practices.

## Languages Supported

### C++ (`/cpp`)
- **clang-format**: Comprehensive code formatting based on Google and LLVM style guides
- **clang-tidy**: Static analysis with focus on naming conventions and code quality

### Python (`/python`)
- **Ruff**: Modern, fast linter and formatter with extensive rule set
- **YAPF**: Google-style code formatter with detailed configuration options

## Repository Structure

```
common-formatters/
├── cpp/
│   ├── .clang-format     # C++ code formatting rules
│   ├── .clang-tidy       # C++ static analysis rules
│   └── README.md         # C++ specific documentation
├── python/
│   ├── ruff.toml         # Ruff configuration
│   ├── .style.yapf       # YAPF configuration
│   └── README.md         # Python specific documentation
└── README.md             
```

## Quick Start

### For C++ Projects
1. Copy the files from `/cpp` directory to your project root
2. Your editor/IDE will automatically detect and use the configurations, if you have clang working on your machine.
3. See [cpp/README.md](cpp/README.md) for detailed usage instructions

### For Python Projects
1. Copy the configuration files from `/python` directory to your project root
2. Install the formatter of your choice: `pip install ruff` or `pip install yapf`
3. See [python/README.md](python/README.md) for detailed usage instructions

## Contributing

Contributions are welcome! If you have improvements or configurations for additional languages:

1. Fork the repository
2. Create a new directory for the language (if needed)
3. Add configuration files with comprehensive comments, when not self-explanatory
4. Include a detailed README for the language-specific directory
5. Update this main README
6. Submit a pull request

## Acknowledgments

These configurations are built upon the guides:
- [Google Style Guides](https://google.github.io/styleguide/)
- [LLVM Coding Standards](https://llvm.org/docs/CodingStandards.html)
- [PEP 8 -- Style Guide for Python Code](https://peps.python.org/pep-0008/)
- The documentations of the formatters.

