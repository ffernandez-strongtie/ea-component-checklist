# Story: Define Reusable Action and Issue-Action Association Model

## Value Statement
As a process engineer, I need actions to be reusable across multiple issues so that standard actions do not need to be recreated every time a new issue is added.

## Details
Define the target persistence model that separates Component Review Issues from reusable Component Review Actions. The model should support one issue having many actions and one action being associated to many issues.

Reusable actions may be edited over time in administration. That is acceptable for future use, but any Component Review information already sent with a project must remain unchanged. The model/design must preserve that snapshot behavior.

The implementation should identify the required new or modified tables/entities at a high level, such as a reusable action entity and an issue-action association entity. Actual names should follow CSE conventions.

## Acceptance Criteria
- Target model supports reusable action records independent of a single issue.
- Target model supports many-to-many issue-action associations.
- Target model preserves action fields required by existing behavior, including action ID, default flag, and job note text.
- Target model includes enough metadata to migrate existing records safely.
- Target model or related project workflow preserves immutable project-level copies of Component Review information after it is sent with a project.
- Proposed model is reviewed with a technical lead or data owner before implementation begins.
