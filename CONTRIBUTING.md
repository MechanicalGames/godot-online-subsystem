# Contributing to Godot Online Subsystem by Mechanical Games

Thank you for your interest in contributing to the Godot Online Subsystem by Mechanical Games! We welcome contributions from the community.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Issue Types](#issue-types)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Features](#suggesting-features)
  - [Creating Tasks](#creating-tasks)
  - [Pull Requests](#pull-requests)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Project Board and Workflow](#project-board-and-workflow)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Issue Types

We categorize issues into three main types. Please use the appropriate issue template when creating a new issue:

#### Feature (User-Facing)
Use the **Feature Request** template for functionality that will be used by consumers of the GD Extension. This includes:
- New APIs or interfaces for game developers
- Player-facing features (authentication, matchmaking, etc.)
- New platform integrations
- Enhancements to existing user-facing functionality

#### Task (Development Team-Facing)
Use the **Task** template for development team-facing work. This includes:
- Infrastructure improvements
- Build system updates
- CI/CD pipeline work
- Documentation infrastructure
- Repository management and tooling
- Internal process improvements

#### Bug
Use the **Bug Report** template for reporting issues or defects in existing functionality.

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. Use the **Bug Report** issue template, which will guide you through providing:

- **Clear and descriptive title**
- **Steps to reproduce the problem**
- **Expected vs. actual behavior**
- **Environment information**: Godot version, OS, extension version
- **Screenshots or logs** if relevant

### Suggesting Features

Use the **Feature Request** template for user-facing enhancements. The template will guide you through:

- **Clear description** of the feature
- **Use case** explaining why it would be useful
- **Alternative solutions** you've considered
- **Additional context** like examples or mockups

### Creating Tasks

Use the **Task** template for development team-facing work items. The template will guide you through:

- **Task description** and objectives
- **Acceptance criteria** for completion
- **Additional context** and references

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
- Make use of [GitMoji](https://gitmoji.dev/) and [GitMoji CLI](https://github.com/carloscuesta/gitmoji-cli) to define the type

### Commit Message Format

```
<type> <subject>

<body>

<footer>
```

**Types:**
- `✨ :sparkles:`: A new feature
- `🐛 :memo:`: A bug fix
- `📝 :memo:`: Documentation only changes
- `🎨 :art:`: Code style changes (formatting, missing semicolons, etc.)
- `♻️ :recycle:`: Code change that neither fixes a bug nor adds a feature
- `🧪 :test_tube:`: Add a failing test
- `✅ :white_check_mark:`: Add, update, or pass tests
- `👷 :construction_worker:`: Changes to build process or auxiliary tools

**Example:**
```
✨ Add Steam authentication support

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

## Project Board and Workflow

### Automated Issue Tracking

All issues and pull requests are automatically added to our GitHub Project board through automated workflows. This ensures:
- Single source of truth for task tracking
- Visibility into project progress
- Clear prioritization and status tracking

### Issue Labels

Issues are automatically labeled based on their type:
- `feature` - User-facing functionality
- `task` - Development team-facing work
- `bug` - Defects and issues

Additional labels may be added to provide more context about:
- Priority (high-priority, etc.)
- Status (in-progress, blocked, etc.)
- Platform or component (steam, eos, core, etc.)

### Workflow Setup

For repository maintainers, see [`.github/WORKFLOW_SETUP.md`](.github/WORKFLOW_SETUP.md) for detailed instructions on configuring the project board integration.

## Questions?

Feel free to open an issue with your question or reach out to the maintainers. For general questions and community discussions, check if [GitHub Discussions](https://github.com/MechanicalGames/godot-online-subsystem/discussions) is enabled for this repository.

Thank you for contributing! 🎮
