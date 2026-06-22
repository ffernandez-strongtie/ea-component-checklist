# Story: Add Issue Category Editing

## Value Statement
As a process engineer, I need to categorize Component Review issues so that large checklists are easier to organize and maintain.

## Details
Add a free-text Category field to Component Review Issues and allow administrators to edit the category values for each issue.

An issue can belong to one or more categories. Multiple categories should be entered as comma-delimited text, for example: `Design, Loading`.

The exact database column should follow the CSE data model conventions. If a category field already exists, reuse it. If not, add one with appropriate migration/default behavior.

## Acceptance Criteria
- Issues include a Category field that supports one or more categories.
- Category is visible on the Issues administration page.
- User can edit the category for an issue.
- Category is free text and supports comma-delimited values.
- Category is optional.
- Whitespace around comma-delimited category values is ignored.
- Saved category values persist after leaving and reopening the page.
- Blank category values are supported.
- Category changes do not affect issue-action associations.
