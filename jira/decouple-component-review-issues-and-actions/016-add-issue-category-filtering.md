# Story: Add Issue Category Filtering

## Value Statement
As a process engineer, I need to filter Component Review issues by category so that I can focus on a smaller set of checklist items during maintenance.

## Details
Add category filtering to the Issues administration page using the same filtering behavior already provided by the existing grid control for other filterable columns. Do not build a custom filtering workflow unless the current grid control cannot support the Category column.

Filtering should not change stored issue-action associations. If the selected issue is filtered out, the UI should handle selection state cleanly.

## Acceptance Criteria
- Category column uses the existing grid-control filtering pattern used by other columns.
- Category filter options are populated from existing issue categories.
- Applying a category filter limits the Issues grid to matching issues.
- Clearing the filter restores all issues.
- Associated actions grid updates correctly when the selected issue changes due to filtering.
- Filter state is visible to the user.
