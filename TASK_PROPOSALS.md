# Codebase Issue Triage and Proposed Tasks

## 1) Typo Fix Task
- **Issue found:** The phrase "i can be reached when found" is grammatically unclear and has inconsistent capitalization.
- **Proposed task:** Update the line to: "I can be reached through GitHub messages."
- **Where:** `AboutMOI` contact bullet.

## 2) Bug Fix Task
- **Issue found:** The opening self-introduction line has an unmatched parenthesis in `(@ndu0323`, which causes malformed Markdown text and can render oddly in profile viewers.
- **Proposed task:** Correct the handle formatting to `(@ndu0323)`.
- **Where:** `AboutMOI` first bullet.

## 3) Documentation/Comment Discrepancy Task
- **Issue found:** The HTML comment says this is a special repository because `README.md` appears on the GitHub profile, but the tracked file is named `AboutMOI`.
- **Proposed task:** Either rename `AboutMOI` to `README.md` or update the comment to reflect the actual file name and intended usage.
- **Where:** trailing HTML comment block in `AboutMOI`.

## 4) Test Improvement Task
- **Issue found:** There are no automated checks validating Markdown quality or profile-file conventions.
- **Proposed task:** Add a CI workflow that runs markdown linting and a lightweight content check script to catch malformed handles/parentheses and missing expected profile file names.
- **Suggested acceptance criteria:**
  - CI runs on pull requests.
  - Fails when Markdown has unmatched parentheses in key identity lines.
  - Fails when profile repository lacks a `README.md` (if that is the intended standard).
