# Issue Creation Policy

This document summarizes the guidelines for creating Issues.
The goals are to ensure smooth development and progress management, and to improve information transparency.

## Table of Contents

- [Issue Granularity](#issue-granularity)
- [Issue Structure](#issue-structure)
  - [Title](#title)
  - [Body](#body)
- [Reference Examples of Issue Structure](#reference-examples-of-issue-structure)
- [Operational Rules](#operational-rules)

---

## Issue Granularity

Issues should be defined as the smallest unit of work.

- **1 Issue = 1 Specific Goal (task/bug fix/feature proposal)**:
  - If multiple different tasks are included, use a checklist or divide them into multiple Issues.
- **Definition of Done (DoD) should be clear**:
  - Specify exactly what needs to be achieved for the Issue to be considered "Complete."

## Issue Structure

Organize information clearly so that anyone can understand the content.

### Title

- **Concise and specific**: Make it understandable at a glance (e.g., `Fix validation bug in login screen`).
- **Use Prefixes**: If possible, clearly specify the category.
  - `feat:`: New feature
  - `fix:`: Bug fix
  - `docs:`: Documentation
  - `chore:`: Tasks, environment setup, etc.

### Body

Include the following information.

- **Background/Purpose**: Why is this task necessary?
- **Scope of Work**: Specifically what should be done (task list format recommended).
- **Completion Criteria**: The criteria for determining that the work is finished.
- **Reference Information**: Related documents, screenshots, reference URLs, related PRs, etc.

## Reference Examples of Issue Structure

Refer to the following structures when providing information in an Issue.

### 【For Bug Reports】

```markdown
## Overview
(Brief explanation of the bug)

## Reproduction Steps
1. 
2. 
3. 

## Expected Behavior
(What should happen)

## Actual Behavior
(What is actually happening)

## Environment
- OS/Browser: 
- Version: 

## Others
(Screenshots, logs, etc.)
```

### 【For Features, Improvements, or Tasks】

```markdown
## Overview/Purpose
(Why and what is being done)

## Scope of Work
- [ ] 
- [ ] 

## Completion Criteria
- [ ] 

## Reference Information
- 
```

## Operational Rules

- **Assignment**: Assign yourself when starting work to clarify the status.
- **Linking with PRs**: When creating a PR, include `Closes #123` to link the Issue and PR.
- **Discussion in Comments**: Record design decisions or concerns in the comments of the Issue to keep track of the history.

---

Related Documents:
- [Pull Request Creation Policy](./pull-request.md)
- [Code Review Perspectives](./review.md)
- [Commit Conventions](./commit.md)
