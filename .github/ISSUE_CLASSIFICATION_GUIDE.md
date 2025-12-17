# Issue Classification Guide

This guide helps maintainers classify existing and new issues according to the project's issue type system.

## Classification Rules

### Feature (User-Facing)
**Label**: `feature`  
**Criteria**: Work that directly impacts users of the GD Extension

**Examples from existing issues**:
- Issue #3: "Implement SteamWorks provider" - User-facing functionality ✓
- Issue #4: "Implement C#-friendly bindings" - User-facing API ✓
- Issue #6: "Define core subsystem interfaces" - User-facing API ✓
- Issue #1: "Add Null provider" - User-facing testing feature ✓
- Issue #5: "Implement provider selection logic" - User-facing functionality ✓
- Issue #9: "Set up demos and sample projects" - User-facing examples ✓

### Task (Development Team-Facing)
**Label**: `task`  
**Criteria**: Internal improvements, infrastructure, or process work

**Examples from existing issues**:
- Issue #2: "Integrate with project board/GitHub issues" - Internal process ✓
- Issue #7: "Create initial repository structure" - Infrastructure ✓

### Bug
**Label**: `bug`  
**Criteria**: Something is broken or not working as expected

## Quick Reference Table

| Issue # | Title | Type | Reasoning |
|---------|-------|------|-----------|
| #1 | Add Null provider | Feature | User-facing testing capability |
| #2 | Integrate with project board | Task | Internal process/infrastructure |
| #3 | Implement SteamWorks provider | Feature | User-facing platform integration |
| #4 | Implement C#-friendly bindings | Feature | User-facing API surface |
| #5 | Implement provider selection logic | Feature | User-facing functionality |
| #6 | Define core subsystem interfaces | Feature | User-facing API design |
| #7 | Create repository structure | Task | Internal infrastructure |
| #9 | Set up demos and sample projects | Feature | User-facing examples |

## Label Migration

For existing issues without proper labels, maintainers should:

1. Review each issue using this guide
2. Add the appropriate `feature` or `task` label
3. Remove or update any conflicting labels
4. Add additional context labels as needed (e.g., `API`, `backend`, `demo`)

## Label Guidelines Going Forward

When reviewing new issues:
- Check that the appropriate template was used
- Verify the correct label was auto-applied
- Add additional context labels for better organization
- Consider priority labels (to be defined) for critical items
