# Product Manager Task Conventions

These rules define how tasks are created, named, stored, and moved in the workspace.

---

## 1. Task File Location
- All new tasks start in `/workspace/backlog/`.
- Active work moves to `/workspace/doing/`.
- Completed work moves to `/workspace/done/`.
- No work item should exist in more than one folder at a time.

## 2. File Naming
- File name must match the task `id` field.
- Example: `T-20250215-ab12cd.json`
- Lowercase file extension `.json` only.

## 3. Task ID Format
- Format: `T-YYYYMMDD-<6-char-random>`
- `YYYYMMDD` = creation date.
- Random segment may be alphanumeric.

## 4. Status Field
- Must be one of: `backlog`, `doing`, `done`, `blocked`.
- Folder location and `status` field must always match.
  - Example: If file is in `/doing/`, `status` must be `"doing"`.

## 5. Dates
- `created_at` = ISO-8601 UTC timestamp of when task was first created.
- `updated_at` = ISO-8601 UTC timestamp of last modification.

## 6. Priority
- Must be one of: `low`, `med`, `high`.
- Chosen based on business importance, not difficulty.

## 7. Acceptance Criteria
- Each criterion should be:
  1. Machine-checkable.
  2. Linked to a `tasks` subtask or `test_plan` step.

## 8. Test Plan
- Each step should describe exactly how to verify acceptance criteria.
- Steps should be reproducible without prior project context.

## 9. Labels
- Optional list for categorization.
- Examples: `"feature"`, `"bug"`, `"infra"`, `"blocked:waiting-for-api"`.

---
