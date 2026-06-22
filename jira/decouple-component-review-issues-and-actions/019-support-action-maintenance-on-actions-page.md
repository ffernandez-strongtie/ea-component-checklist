# Story: Support Action Maintenance on Actions Page

## Value Statement
As a process engineer, I need to add, edit, and delete reusable actions from the Actions page so that action records are maintained in one place instead of through issue-specific grids.

## Details
Move reusable action maintenance behavior to the standalone Component Review Actions page.

The Issues page should manage only associations between issues and actions. It should not be the place where reusable action records are created or deleted.

This story should reuse existing Add Action and Delete Action behavior where possible, but retarget it to the reusable Actions page and the new action model.

Reusable actions cannot be deleted while they are associated to one or more issues. If deletion is blocked, the user should be shown which issues currently use the action.

## Acceptance Criteria
- Actions page supports adding a reusable action.
- Actions page supports editing action-level fields.
- Actions page allows deleting a reusable action only when it is not associated to any issue.
- If a reusable action is associated to one or more issues, delete is blocked and the UI shows which issues currently use it.
- Issues page does not create or delete reusable action records directly.
- Existing Add Action and Delete Action ribbon behavior is either moved to the Actions page or explicitly replaced there.
