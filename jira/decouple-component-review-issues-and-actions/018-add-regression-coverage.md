# Story: Add Regression Coverage for Decoupled Checklist Administration

## Value Statement
As a developer, I need regression coverage for the decoupled Component Review administration workflow so that future changes do not reintroduce duplicated or broken issue-action behavior.

## Details
Add automated or documented regression coverage appropriate for the CSE application stack. Coverage should focus on the new reusable action model, issue-action association management, and existing output behavior.

If full automation is not practical in one day, add targeted tests for the data-access or service layer and document the remaining manual regression checks.

## Acceptance Criteria
- Test coverage verifies an action can be associated to multiple issues.
- Test coverage verifies an issue can have multiple actions.
- Test coverage verifies removing an association does not delete the reusable action.
- Test coverage verifies associated actions load for a selected issue.
- Test coverage verifies generated output uses associations correctly.
- Test coverage verifies project-level Component Review data does not change after a reusable administration action is edited later.
- Manual test gaps, if any, are documented.
