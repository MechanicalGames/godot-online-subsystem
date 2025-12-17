# Project Board and Workflow Setup

This document explains how to configure and maintain the GitHub project board integration for the Godot Online Subsystem repository.

## Overview

The repository uses GitHub Projects (V2) for tracking work items. Issues are automatically added to the project board via GitHub Actions, maintaining a single source of truth for task tracking.

## Issue Types

We use different issue types to categorize work:

### Feature
**Purpose**: User-facing functionality for consumers of the GD Extension  
**Label**: `feature`  
**Use when**: Adding or modifying features that end users will directly interact with or benefit from.

**Examples**:
- Adding Steam authentication support
- Implementing matchmaking APIs
- Adding friend list functionality

### Task
**Purpose**: Development team-facing work (infrastructure, tooling, process improvements)  
**Label**: `task`  
**Use when**: Working on internal improvements that don't directly affect end users.

**Examples**:
- Setting up CI/CD pipelines
- Configuring project boards
- Improving build systems
- Documentation infrastructure

### Bug
**Purpose**: Reporting issues or defects  
**Label**: `bug`  
**Use when**: Something isn't working as expected.

## GitHub Actions Workflow

### Automatic Project Board Integration

The `.github/workflows/add-to-project.yml` workflow automatically adds new and reopened issues and pull requests to the project board.

#### Configuration Required

To enable this workflow, repository administrators need to:

1. **Create or identify a GitHub Project board**
   - Can be at the organization level or user level
   - Note the project URL (e.g., `https://github.com/orgs/MechanicalGames/projects/1`)

2. **Create a Personal Access Token (PAT)**
   - Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Generate a new token with the following scopes:
     - `repo` (Full control of private repositories)
     - `project` (Full control of projects)
     - `org:read` (if using an organization project)
   - Save the token securely

3. **Configure Repository Secrets and Variables**
   - Go to repository Settings → Secrets and variables → Actions
   - Add a new repository secret:
     - Name: `ADD_TO_PROJECT_PAT`
     - Value: The PAT created in step 2
   - Add a new repository variable:
     - Name: `PROJECT_URL`
     - Value: The full URL of your project (e.g., `https://github.com/orgs/MechanicalGames/projects/1`)

4. **Verify Workflow Permissions**
   - Go to repository Settings → Actions → General
   - Under "Workflow permissions," ensure the appropriate permissions are set

### Manual Workflow Triggers

If you need to manually add issues to the project board:

1. Navigate to the project board
2. Click the "+" button or "Add item"
3. Search for and select the issue or PR

## Project Board Best Practices

### Status Fields

We recommend using the following status fields in your project board:
- **Backlog**: Items not yet started
- **Ready**: Items ready to be worked on
- **In Progress**: Currently being worked on
- **In Review**: Under review or testing
- **Done**: Completed

### Custom Fields

Consider adding these custom fields:
- **Priority**: High, Medium, Low
- **Size**: Small, Medium, Large
- **Type**: Automatically set from issue labels (feature, task, bug)
- **Target Release**: For planning purposes

### Keeping Issues and Project Board in Sync

1. **Use issue templates**: They automatically apply the correct labels
2. **Update issue status**: When changing the status in the project board, add a comment to the issue
3. **Close completed issues**: This helps keep the board clean
4. **Link related issues**: Use keywords like "Closes #123" in PRs

## Workflow Maintenance

### Regular Reviews

- **Weekly**: Review open issues and ensure they're properly categorized
- **Monthly**: Clean up stale issues and update project board structure as needed
- **Per Release**: Update issues with target release information

### Updating Templates

Issue templates are located in `.github/ISSUE_TEMPLATE/`. To modify:

1. Edit the appropriate YAML file
2. Test the template by creating a draft issue
3. Commit and push changes

### Troubleshooting

**Workflow not running?**
- Check that the PAT hasn't expired
- Verify the `PROJECT_URL` variable is correct
- Check workflow permissions in repository settings

**Issues not appearing on the board?**
- Manually add one issue to verify permissions
- Check the Actions tab for workflow run logs
- Ensure the project board is not archived

## References

- [GitHub Projects Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
- [Automating Projects using Actions](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/automating-projects-using-actions)
- [actions/add-to-project](https://github.com/actions/add-to-project)
