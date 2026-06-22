# Story: Persist Manage Actions Changes

## Value Statement
As a process engineer, I need changes made in Manage Actions to be saved so that the selected issue uses the updated action associations in future review workflows.

## Details
Wire the Manage Actions dialog to the new association table and queries. Applying changes should add newly checked associations and remove unchecked associations for the selected issue.

Canceling should close the dialog without changing persisted associations.

Removing an action from an issue must only remove the issue-action association. It must not delete the reusable action record from the Actions page.

## Acceptance Criteria
- Applying the dialog saves checked actions as associations for the selected issue.
- Applying the dialog removes associations for actions that were unchecked.
- Removing an association does not delete the reusable action record.
- Canceling the dialog does not save changes.
- Associated actions grid refreshes after successful apply.
- Reopening the dialog reflects the saved association state.
- Errors during save are shown to the user and do not leave the UI in a misleading state.
