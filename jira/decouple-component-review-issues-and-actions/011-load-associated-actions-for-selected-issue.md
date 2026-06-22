# Story: Load Associated Actions for Selected Issue

## Value Statement
As a process engineer, I need to see only the actions associated with the issue I select so that I can quickly understand how that issue will behave during review.

## Details
Update the Issues administration page so selecting an issue loads the actions associated to that issue through the new association model.

This story assumes the Issues page layout has already been updated to include an Associated Actions grid.

## Acceptance Criteria
- Selecting an issue refreshes the associated actions grid.
- The associated actions grid displays only actions linked to the selected issue.
- The grid includes Action ID, Default, and Job Note fields.
- The grid does not display Checklist ID for actions.
- Selecting a different issue updates the grid without requiring a page reload.
- If the selected issue has no associated actions, the grid shows a clear note or empty-state message.
