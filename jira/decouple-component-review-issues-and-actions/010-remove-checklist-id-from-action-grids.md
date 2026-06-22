# Story: Remove Checklist ID from Action Grids

## Value Statement
As a process engineer, I need action grids to focus on reusable action information so that I do not confuse actions with issue-specific checklist rows.

## Details
Update Component Review action-management grids to remove Checklist ID where the grid is displaying actions. The issue grid may still display Checklist ID because that identifies the issue/checklist item itself.

This should include the associated actions grid on the Issues page, the Manage Actions dialog, and the standalone Actions administration page.

## Acceptance Criteria
- Associated actions grid on the Issues page does not show Checklist ID.
- Manage Actions dialog does not show Checklist ID.
- Standalone Actions administration page does not show Checklist ID.
- Main Issues grid still shows Checklist ID for issues.
- Removed columns do not leave layout or sorting artifacts.
- Any export/import implications are documented for follow-up if not changed in this story.

