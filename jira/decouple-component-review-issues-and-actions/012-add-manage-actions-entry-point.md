# Story: Add Manage Actions Entry Point on Issues Page

## Value Statement
As a process engineer, I need a clear way to manage actions for the selected issue so that I can create or remove issue-action associations from the Issues page.

## Details
Add a Manage Actions command to the Component Review Issues administration page. The command should be available when an issue is selected and disabled or unavailable when no issue is selected.

This command replaces the existing Add Action and Delete Action ribbon commands for the Issues page. Since actions are now reusable records, the Issues page should manage associations only. Creating or deleting reusable action records belongs on the standalone Actions administration page.

This story assumes the Issues page has already been reorganized and has an Associated Actions grid. This story only adds the entry point and state behavior. The dialog content and persistence are covered by separate stories.

## Acceptance Criteria
- Manage Actions command is visible on the Issues administration page.
- Existing Add Action and Delete Action ribbon commands are removed from the Issues page or replaced by Manage Actions.
- Manage Actions is disabled or unavailable when no issue is selected.
- Manage Actions becomes enabled when an issue is selected.
- Clicking Manage Actions opens the association-management experience or placeholder hook.
- UI state remains correct when changing selected issues.
