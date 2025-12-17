# GitHub Issue Automation: Type and Status Fields

This document describes how to programmatically manage the **Type** and **Status** fields on issues using the GitHub REST API. These are special fields utilized in repositories that support GitHub's enhanced issue types and project status integration.

## 1. Updating the Type Field on Issues

You can set the type of an issue (e.g., Bug, Task, Feature) using the PATCH API for issues:

### Example API Call
```bash
gh api --method PATCH repos/MechanicalGames/godot-online-subsystem/issues/<issue_number> -f type=<TypeName>
```
**Where**:
- `<issue_number>` is the number of the issue you are updating.
- `<TypeName>` is one of the allowed type names for this repo (see below).

### Allowed Values for the `type` Field
| Type Name | Description                               |
|-----------|-------------------------------------------|
| Bug       | An unexpected problem or behavior         |
| Task      | A specific piece of work                  |
| Feature   | A request, idea, or new functionality     |

### Example Sequence
```bash
gh api --method PATCH repos/MechanicalGames/godot-online-subsystem/issues/7 -f type=Bug
# Changes the type of issue #7 to "Bug"
gh api --method PATCH repos/MechanicalGames/godot-online-subsystem/issues/7 -f type=Task
# Changes the type of issue #7 to "Task"
gh api --method PATCH repos/MechanicalGames/godot-online-subsystem/issues/7 -f type=Feature
# Changes the type of issue #7 to "Feature"
```

A successful update modifies the `type` JSON object in the issue response. Example type object:
```json
"type": {
    "id": <int>,
    "node_id": <string>,
    "name": "Feature", // or "Task", "Bug"
    ...
}
```

## 2. Status Field: Todo, In Progress, Done

Some issues in project boards, or issues enhanced to support status, can be updated with a corresponding status value.

### Example API Call
```bash
gh api --method PATCH repos/MechanicalGames/godot-online-subsystem/issues/<issue_number> -f status="Todo"
gh api --method PATCH repos/MechanicalGames/godot-online-subsystem/issues/<issue_number> -f status="In Progress"
gh api --method PATCH repos/MechanicalGames/godot-online-subsystem/issues/<issue_number> -f status="Done"
```

### Allowed Values for `status`
| Status Value | Meaning         |
|--------------|----------------|
| Todo         | Not yet started|
| In Progress  | Work started   |
| Done         | Work complete  |

### Findings
- Setting type and status updates the special fields in the API response JSON for the issue.
- If an invalid value is provided, the API returns an error.
- These fields are supported only in repos/projects that have them enabled.

---

For more details, see:
- [GitHub Issues API docs](https://docs.github.com/en/rest/issues/issues?apiVersion=2022-11-28#update-an-issue)