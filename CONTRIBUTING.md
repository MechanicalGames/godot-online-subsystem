# Contributing to Godot Online Subsystem

Thank you for your interest in contributing to the Godot Online Subsystem! We welcome contributions from the community.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** to demonstrate the steps
- **Describe the behavior you observed** and what you expected to see
- **Include screenshots or animated GIFs** if relevant
- **Note your environment**: Godot version, OS, etc.

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- **Use a clear and descriptive title**
- **Provide a detailed description** of the suggested enhancement
- **Explain why this enhancement would be useful** to most users
- **List any alternatives** you've considered

### Pull Requests

We actively welcome your pull requests:

1. Fork the repo and create your branch from `main`
2. Make your changes following our coding standards
3. Test your changes thoroughly
4. Update documentation as needed
5. Submit your pull request

## Development Setup

### Prerequisites

- Godot Engine (version TBD)
- Git
- A C++ compiler (if working with GDExtension/native code)

### Building

```bash
# Clone the repository
git clone https://github.com/MechanicalGames/godot-online-subsystem.git
cd godot-online-subsystem

# Follow build instructions (TBD based on project structure)
```

### Testing

```bash
# Run tests (TBD based on project structure)
```

## Coding Standards

### General Guidelines

- Write clear, readable code
- Comment complex logic and algorithms
- Keep functions focused and modular
- Follow the DRY (Don't Repeat Yourself) principle
- Write self-documenting code with meaningful names

### GDScript Style

If contributing GDScript code:

- Use **snake_case** for variables and functions
- Use **PascalCase** for classes
- Use **UPPER_CASE** for constants
- Indent with **tabs** (Godot standard)
- Follow the [official GDScript style guide](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_styleguide.html)

### C++ Style (if applicable)

If contributing C++ code:

- Follow modern C++ best practices (C++17 or later)
- Use meaningful variable names
- Keep lines under 120 characters when reasonable
- Use smart pointers where appropriate
- Document public APIs with comments

### Documentation

- Update README.md if you change functionality
- Add inline comments for complex logic
- Update API documentation for public interfaces
- Include code examples in documentation where helpful

## Commit Guidelines

### Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

### Commit Message Format

```
<type>: <subject>

<body>

<footer>
```

**Types:**
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Code style changes (formatting, missing semicolons, etc.)
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `test`: Adding or updating tests
- `chore`: Changes to build process or auxiliary tools

**Example:**
```
feat: Add Steam authentication support

Implement Steam authentication provider for the online subsystem.
This allows games to authenticate users through Steam.

Closes #123
```

## Pull Request Process

1. **Update documentation** with details of changes to the interface, new environment variables, exposed ports, useful file locations, etc.

2. **Follow the coding standards** outlined in this document

3. **Ensure all tests pass** before submitting

4. **Update the README.md** with details of changes if applicable

5. **Request review** from maintainers

6. **Address feedback** promptly and professionally

7. Your PR will be merged once:
   - It has been approved by at least one maintainer
   - All tests pass
   - All conversations are resolved

## Questions?

Feel free to open an issue with your question or reach out to the maintainers.

Thank you for contributing! 🎮
