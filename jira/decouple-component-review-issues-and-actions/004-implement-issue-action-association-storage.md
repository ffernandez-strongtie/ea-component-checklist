# Story: Add Issue-Action Association Table and Queries

## Value Statement
As a developer, I need a database relationship between Component Review Issues and reusable Actions so that CSE can link existing actions to issues without duplicating action rows.

## Details
Add the database schema change needed to represent issue-action associations. This should be a join/association table or equivalent structure that references the existing issue record and the reusable action record.

Do not migrate production data in this story. The goal is to create the schema and application queries needed by later UI and migration work.

Removing an action from an issue is association-only behavior. It must remove the link between the issue and action, not delete the reusable action record.

Actual table, entity, and key names should follow the existing CSE conventions after the current schema is inspected.

## Acceptance Criteria
- A schema change exists for an issue-action association table or equivalent join structure.
- The association structure references an issue identifier and an action identifier.
- The association structure prevents duplicate links for the same issue/action pair.
- Application code can query all actions associated to a given issue.
- Application code can add an association between an issue and an action.
- Application code can remove an association without deleting the reusable action.
- Application code can determine which issues are associated to a reusable action.
- The change is covered by a basic database migration or schema update test.
- Existing issue and action records remain readable after the schema change.
