# Story: Filter Project Checklist IDs by Category

## Value Statement
As an engineer reviewing truss components, I need to narrow available Checklist IDs by Category when adding or editing a Component Review item so that I can find the correct issue faster.

## Details
Add a Category column to the project-facing Component Review Checklist grid.

When a user types or selects one or more Category values on a review item, the available Checklist ID choices for that item should be filtered to checklist issues that match those categories. Category values come from the Component Review Issues administration data. New categories are maintained in the Issues administration screen, not in this project view.

Multiple category terms should be supported as comma-delimited text, for example: `Design, Plating`. This should narrow the available Checklist IDs to entries matching any entered category term.

This is a project usage workflow, separate from administration-side category maintenance.

## Acceptance Criteria
- Project-facing Component Review Checklist grid includes a Category column.
- Category control allows the user to type and choose from existing Category values.
- Category control supports one or more comma-delimited category values.
- Checklist ID choices are filtered by the Category value or values on that row.
- If multiple category values are entered, Checklist ID choices include entries matching any entered category.
- Clearing Category shows all available Checklist IDs.
- Selecting a Checklist ID still populates the correct checklist description and note behavior.
- Category selection does not create new Category values.
- Existing project/review immutability behavior is preserved after the review item is saved or sent with a project.
