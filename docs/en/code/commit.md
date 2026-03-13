# Commit Conventions

This document outlines the guidelines for Git commit messages and commit granularity.
The goal is to improve history readability and make tracking changes easier.

## Commit Granularity

Commits should be divided into "meaningful minimum units."

- **Separate commits by scope**:
  - Do not mix multiple different changes (e.g., feature additions and refactoring) into a single commit.
  - Mixing changes makes it difficult to revert specific modifications.
- **Commit in a working state**:
  - Avoid committing in a state that causes compilation errors or test failures (except for WIP commits being pushed to a shared branch).

## Commit Message Structure

Write messages so that the changes are immediately understandable.

### Basic Format

```text
<type>: <summary>

<body> (optional)
```

### type (Change Types)

Use prefixes consistent with those used in GitHub Issues and Pull Requests.

- `feat:`: New feature
- `fix:`: Bug fix
- `docs:`: Documentation only changes
- `style:`: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc.)
- `refactor:`: A code change that neither fixes a bug nor adds a feature
- `perf:`: A code change that improves performance
- `test:`: Adding missing tests or correcting existing tests
- `chore:`: Changes to the build process or auxiliary tools and libraries such as documentation generation

### summary (Summary)

- **Concise and specific**: The first line should be about 50 characters, briefly describing the change.
- **Include Ticket ID**: If there is a related ticket, include it (e.g., `feat: [ISSUE-123] Implement login functionality`).

### body (Body)

- **Describe the "Why"**: Explain the reason for the change and any supplemental information on how it was fixed, separated from the summary by a blank line.
- **Use Bullet Points**: If multiple small changes are included, use bullet points for clarity.

## Example of a Good Commit Message

```text
feat: [ISSUE-45] Add validation for user registration

- Added check for duplicate email addresses
- Changed minimum password length to 8 characters
- Translated error messages into Japanese
```

---

Related Documents:
- [Issue Creation Policy](./issue.md)
- [Pull Request Creation Policy](./pull-request.md)
- [Code Review Perspectives](./review.md)
