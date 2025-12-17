# GitHub Project Board Setup Checklist

This checklist helps repository administrators complete the setup of the project board integration.

## ✅ Completed (Already Done)

- [x] Issue templates created (Feature, Task, Bug)
- [x] GitHub Actions workflow created for auto-adding issues to project board
- [x] CONTRIBUTING.md updated with issue type documentation
- [x] Setup documentation created (WORKFLOW_SETUP.md)
- [x] Issue classification guide created for existing issues

## 📋 Required Actions for Repository Administrators

### 1. Create or Configure GitHub Project Board

**If you don't have a project board yet:**
1. Go to https://github.com/orgs/MechanicalGames/projects (or user projects if not using org)
2. Click "New project"
3. Choose "Board" or "Table" view
4. Name it (e.g., "Godot Online Subsystem Development")
5. Add status columns (suggested: Backlog, Ready, In Progress, In Review, Done)
6. Note the project URL (e.g., `https://github.com/orgs/MechanicalGames/projects/1`)

**If you already have a project board:**
- Note the project URL

### 2. Create Personal Access Token (PAT)

1. Go to https://github.com/settings/tokens
2. Click "Generate new token" → "Generate new token (classic)"
3. Name it: "Project Board Automation"
4. Set expiration (recommend: 90 days or 1 year, then renew)
5. Select scopes:
   - ✅ `repo` (Full control of private repositories)
   - ✅ `project` (Full control of projects)
   - ✅ `org:read` (if using organization project)
6. Click "Generate token"
7. **IMPORTANT**: Copy the token now (you won't be able to see it again!)

### 3. Configure Repository Secrets and Variables

**Add the PAT as a secret:**
1. Go to https://github.com/MechanicalGames/godot-online-subsystem/settings/secrets/actions
2. Click "New repository secret"
3. Name: `ADD_TO_PROJECT_PAT`
4. Value: Paste the PAT from step 2
5. Click "Add secret"

**Add the project URL as a variable:**
1. Go to https://github.com/MechanicalGames/godot-online-subsystem/settings/variables/actions
2. Click "New repository variable"
3. Name: `PROJECT_URL`
4. Value: Your project URL from step 1 (e.g., `https://github.com/orgs/MechanicalGames/projects/1`)
5. Click "Add variable"

### 4. Verify Workflow Permissions

1. Go to https://github.com/MechanicalGames/godot-online-subsystem/settings/actions
2. Under "Workflow permissions," ensure appropriate permissions are set
3. Recommended: "Read and write permissions"

### 5. Test the Integration

**Test with a new issue:**
1. Create a test issue using one of the templates
2. Check the Actions tab to see if the workflow runs
3. Verify the issue appears in your project board
4. Delete the test issue if successful

**If it doesn't work:**
- Check the Actions tab for error messages
- Verify the PAT hasn't expired
- Confirm the PROJECT_URL is correct
- Review the workflow logs in the Actions tab

### 6. Update Existing Issues (Optional but Recommended)

Use the [Issue Classification Guide](.github/ISSUE_CLASSIFICATION_GUIDE.md) to:
1. Add `feature` or `task` labels to existing issues
2. Manually add existing issues to the project board
3. Organize them by status

**Quick label guide:**
- Issues #1, 3, 4, 5, 6, 9 → `feature` (user-facing)
- Issues #2, 7 → `task` (development team-facing)

### 7. Configure Project Board Views (Optional)

Enhance your project board with:
- **Status field**: Track progress (Backlog → In Progress → Done)
- **Priority field**: High, Medium, Low
- **Type field**: Automatically populated from labels
- **Assignee field**: Track who's working on what
- **Iteration field**: For sprint/release planning

### 8. Set Up Notifications (Optional)

Configure notification preferences:
1. Project settings → Notifications
2. Choose how you want to be notified of changes

## 🔄 Maintenance Tasks

**Monthly:**
- Review and renew PAT if needed (before expiration)
- Audit project board organization
- Clean up closed/completed items

**Per Release:**
- Archive completed items from previous releases
- Update project board views for new release cycle

## 📚 Documentation References

- [WORKFLOW_SETUP.md](WORKFLOW_SETUP.md) - Detailed technical documentation
- [ISSUE_CLASSIFICATION_GUIDE.md](ISSUE_CLASSIFICATION_GUIDE.md) - Guide for classifying issues
- [CONTRIBUTING.md](../CONTRIBUTING.md) - Contributor guidelines including issue types

## ❓ Troubleshooting

**Workflow not running?**
→ Check PAT expiration and repository secret configuration

**Issues not appearing on board?**
→ Verify PROJECT_URL and manually add one issue to test permissions

**Need help?**
→ See [WORKFLOW_SETUP.md](WORKFLOW_SETUP.md) troubleshooting section

---

Once you complete steps 1-5, the automatic project board integration will be fully functional! 🎉
