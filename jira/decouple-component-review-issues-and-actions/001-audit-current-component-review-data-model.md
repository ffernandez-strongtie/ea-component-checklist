# Story: Audit Current Component Review Data Model

## Value Statement
As a developer, I need to understand the current Component Review tables, relationships, and generated outputs so that we can decouple issues and actions without losing existing behavior.

## Details
Review the current CSE persistence model for Component Review Issues, Actions, Changes, job notes, and customer-facing notes. Identify how actions are currently tied to issues or checklist IDs and where that relationship is used by the application.

Also identify where Component Review information is copied or attached to a project. Because this information supports engineering seal review, project-level records must be immutable after they are sent with a project.

The exact table names are unknown at story creation time. The implementation team should inspect the CSE database schema, data access layer, import/export logic, and any services that generate checklist or job-note output.

## Acceptance Criteria
- Current tables/entities that store Component Review Issues, Actions, Changes, and notes are documented.
- Current relationships between issues, actions, checklist IDs, and notes are documented.
- Current UI screens and code paths that read or write action data are identified.
- Current import/export/sync code paths that depend on the coupled model are identified.
- Code paths that copy or attach Component Review information to a project are identified.
- Any current project-level references back to mutable administration records are documented as risks.
- Risks and unknowns for migration are documented.
