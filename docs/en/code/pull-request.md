# Pull Request Creation Policy

This document summarizes the guidelines for creating Pull Requests (PRs).
The goals are to ensure smooth reviews and maintain code quality.

## Table of Contents

- [PR Granularity](#pr-granularity)
- [PR Structure (How to Write an Overview)](#pr-structure-how-to-write-an-overview)
  - [Title](#title)
  - [Body](#body)
- [Testing and Evidence](#testing-and-evidence)
- [Points to Note When Requesting Reviews](#points-to-note-when-requesting-reviews)

---

## PR Granularity

Keep PRs as small as possible.

- **1 PR = 1 Concern (e.g., 1 feature addition, 1 bug fix)**:
  - Including multiple fixes in one PR increases the reviewer's load and risks overlooking bugs.
- **Estimated Lines of Code**:
  - Reviews tend to become difficult when a PR exceeds 200–400 lines. Consider dividing the PR if the changes are extensive.
- **Handling Refactoring**:
  - Ideally, feature additions and refactoring should be in separate PRs.

## PR Structure (How to Write an Overview)

Explain "What," "Why," and "How" you changed the code so reviewers can understand the PR immediately.

### Title

- **Use Prefixes**: Use `feat:`, `fix:`, `refactor:`, `docs:`, etc., to clearly indicate the type of change.
- **Concise Summary**: Make it understandable at a glance (e.g., `feat: Implement login functionality`).
- **Linking IDs**: Include ticket numbers or task IDs if applicable (e.g., `[ISSUE-123] fix: Correct validation errors`).

### Body

Using the following template is recommended.

- **Changes/Purpose**:
  - Why is this change necessary? What is the background?
- **Key Changes**:
  - Specifically what was changed and how (include technical design decisions for major changes).
- **Scope of Impact**:
  - Are there other areas affected by this change?
- **Related Links (Primary Sources)**:
  - URLs for related tickets (Issues), documentation, and **primary sources consulted (official docs, technical specs, etc.)**.
  - Provide reliable sources to support the validity of the implementation, rather than just secondary sources (like technical blogs).

## Testing and Evidence

Provide test results to prove that the changes work correctly.

- **Test Details**:
  - Types of tests conducted (unit tests, manual tests, etc.) and the cases verified.
- **Attach Evidence**:
  - For UI changes, attach screenshots or videos of the "Before" and "After" states.
  - Pasting logs or execution results in text format is also effective.
- **Test Automation**:
  - If test code is included, ensure that all tests pass in CI.

## Points to Note When Requesting Reviews

Be mindful of the reviewer's experience so they can approve with minimal cost and maximum confidence.

- **Self-Review and Self-Comment**:
  - Before creating the PR, review the differences yourself to remove unnecessary code (e.g., `console.log`) and finalize naming.
  - **Add self-comments to explain areas where your intent might be unclear.** This reduces the time reviewers spend wondering "Why?".
- **Clarify Key Points**:
  - For large PRs, specify which files need the most focus or highlight the core logic.
- **Use Draft PRs**:
  - For work in progress, create a Draft PR and change it to "Ready for review" when you're ready for feedback.
- **Use Diagrams or Tables**:
  - If the logic is complex, adding sequence diagrams or architecture diagrams (using Markdown, etc.) is very helpful.

---

Related Documents:
- [Issue Creation Policy](./issue.md)
- [Code Review Perspectives](./review.md)
- [Commit Conventions](./commit.md)
