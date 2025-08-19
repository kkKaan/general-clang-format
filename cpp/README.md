# C++ Formatter Configurations

This directory contains formatter and static analysis configurations for C++ projects.

## Files

- **`.clang-format`**: Code formatting configuration for clang-format
- **`.clang-tidy`**: Static analysis configuration for clang-tidy

## About the Configurations

### .clang-format
The `.clang-format` file provides comprehensive formatting rules for C++ code, based on a mixture of:
- [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)
- [LLVM Coding Standards](https://llvm.org/docs/CodingStandards.html)

**Key features:**
- 4-space indentation
- Custom brace wrapping style
- 150 character column limit
- Comprehensive spacing and alignment rules
- Detailed commenting of available options

### .clang-tidy
The `.clang-tidy` file focuses on code quality and naming conventions:
- Enforces `readability-identifier-naming` checks
- Comprehensive naming rules for classes, functions, variables, etc.
- Uses CamelCase for types and functions, camelBack for variables
- Interface classes prefixed with 'I'

## Usage

### clang-format
1. Place `.clang-format` in your project's root directory
2. Run: `clang-format -i <file>` to format a specific file
3. Or integrate with your IDE/editor for automatic formatting

### clang-tidy
1. Place `.clang-tidy` in your project's root directory
2. Run: `clang-tidy <file> -- <compile_flags>` to check a file
3. Or integrate with your build system

## IDE Integration

Most modern IDEs and editors support these configurations automatically:
- **VS Code**: Install C/C++ extension
- **CLion**: Built-in support
- **Vim/Neovim**: Use plugins like `vim-clang-format`
- **Emacs**: Use `clang-format.el`

## Customization

The configurations include commented alternatives for most settings. Uncomment and modify as needed for your project's specific requirements.

For more information, see the official documentation:
- [Clang-Format Documentation](https://clang.llvm.org/docs/ClangFormatStyleOptions.html)
- [Clang-Tidy Documentation](https://clang.llvm.org/extra/clang-tidy/)
