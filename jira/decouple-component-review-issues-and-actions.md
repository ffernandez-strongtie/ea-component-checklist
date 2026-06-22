# Epic: Decouple Component Review Issues and Actions

## Value Statement
As a process engineer, I need Component Review issues and actions to be managed independently in CSE so that reusable standard actions can be associated or removed from issues without duplicating action records for every issue.

## Background
The current Component Review checklist administration model tightly couples issues, actions, and note text. When a new issue is added, standard actions must be recreated for that issue even when those actions already exist elsewhere. This creates duplicate data entry, increases the risk of inconsistent checklist behavior, and makes CSE harder to keep aligned with the other checklist sources.

The proposed mockup changes the administration experience by treating actions as reusable records and allowing administrators to manage issue-action associations from the Issues page. It also separates Issues, Actions, and Changes into distinct administration views.

Important domain constraint: Component Review information is used when reviewing truss components for engineering seal decisions. Once Component Review issues/actions are sent with a project, that project must keep an immutable copy of the review information. Project records must not depend on live action references that can change later.

## Goals
- Support reusable Component Review actions that are not owned by a single issue.
- Support issue-to-action associations so one issue can have many actions and one action can be reused by many issues.
- Provide an administration workflow to add or remove associated actions for a selected issue.
- Move reusable action creation and deletion to the Actions administration page.
- Preserve existing checklist behavior after migration.
- Preserve legal/audit integrity by copying Component Review information to projects when used, rather than referencing mutable administration records.
- Reduce unnecessary Checklist ID dependency from action-management views.
- Make Component Review Issues, Actions, and Changes easier to maintain as separate administrative concerns.

## Non-Goals
- Selecting or implementing the final source-of-truth system across all three checklist locations.
- Redesigning customer-facing note authoring beyond preserving current behavior unless covered by a future epic.
- Replacing import/export/sync mechanisms unless required to support the decoupled model.

## Scope
- Data model review and migration planning.
- New or updated persistence model for reusable actions and issue-action associations.
- Migration of existing duplicated issue/action data into reusable action records and association records.
- Administration UI updates for the Issues page.
- Administration UI updates for standalone Actions and Changes pages.
- Reusable action maintenance on the Actions page.
- Removal of Checklist ID from action-management displays where it no longer represents the action model.
- Regression checks to ensure generated review/checklist output remains correct.
- Verification that existing project/review records are not changed by later edits to reusable administration actions.

## Success Metrics
- A reusable standard action can be associated to multiple issues without duplicating the action record.
- A process engineer can add or remove actions from a selected issue through the CSE administration UI.
- Existing issue/action relationships remain available after migration.
- Existing generated notes/checklist outputs remain functionally equivalent after migration.
- Previously created project/review records do not change when reusable action text is edited later.
- Action-management views no longer require users to reason about Checklist ID as the owner of an action.

## Reference
- Mockup: https://ffernandez-strongtie.github.io/ea-component-checklist/administration.html
- Project checklist category filter mockup: https://ffernandez-strongtie.github.io/ea-component-checklist/project-component-review-category-filter.html
