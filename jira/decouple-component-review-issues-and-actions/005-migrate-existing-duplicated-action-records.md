# Story: Migrate Existing Duplicated Action Records

## Value Statement
As a process engineer, I need existing Component Review action data migrated into the new reusable model so that current checklist content remains available without requiring manual re-entry.

## Details
Implement and run the migration that converts existing duplicated action rows into reusable action records and issue-action association records.

This story depends on the approved migration mapping. It should include validation output that lets the team confirm record counts and association counts before and after migration.

Exact duplicate action rows should be consolidated into one reusable action record. Rows with any differing relevant column should remain separate action records.

## Acceptance Criteria
- Existing action data is migrated into reusable action records.
- Exact duplicate action rows are consolidated into a single reusable action record.
- Action rows with any relevant column difference remain separate reusable action records.
- Existing issue-action relationships are migrated into association records.
- No existing active issue loses its associated actions.
- Migration produces a validation summary with before/after counts.
- Migration can be tested in a non-production environment.
- Migration failure behavior is documented.
