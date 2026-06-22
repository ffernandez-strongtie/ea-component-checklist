# Story: Create Migration Mapping for Existing Issue-Action Data

## Value Statement
As a developer, I need a clear mapping from the current duplicated issue-action data into the new reusable action model so that existing checklist behavior is preserved after migration.

## Details
Create a migration mapping that explains how current rows will be transformed into reusable action records and issue-action association records.

The mapping should consolidate exact duplicate actions into one reusable action record. If all relevant action columns are the same, the rows should map to one action. If any relevant column is different, even slightly, they should remain separate action records.

## Acceptance Criteria
- Migration rules define how to identify reusable action candidates.
- Migration rules consolidate action rows only when all relevant action columns match.
- Migration rules keep action rows separate when any relevant action column differs.
- Migration rules define how issue-action associations will be created.
- Edge cases and records requiring manual review are documented.
