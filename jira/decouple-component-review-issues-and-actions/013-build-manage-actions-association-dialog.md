# Story: Build Manage Actions Association Dialog

## Value Statement
As a process engineer, I need a dialog that shows available reusable actions and which ones are associated to the selected issue so that I can choose the correct actions without creating duplicates.

## Details
Build the Manage Actions dialog for the selected issue. The dialog should list all reusable actions with checkboxes indicating whether each action is currently associated to the selected issue.

The dialog should support searching by Action ID or note text. Checklist ID should not be shown in the dialog because actions are no longer managed as issue-owned checklist rows.

## Acceptance Criteria
- Dialog title identifies the selected issue.
- Dialog lists all reusable actions.
- Associated actions are checked when the dialog opens.
- Unassociated actions are unchecked when the dialog opens.
- User can check and uncheck actions in the dialog.
- Search filters by Action ID or note text.
- Dialog does not display Checklist ID for actions.
- Dialog includes Apply and Cancel actions.
