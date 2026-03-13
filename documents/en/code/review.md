# Code Review Perspectives

This document summarizes the guidelines and checklists for conducting code reviews.

## PR Description

Ensure that the title and content are described according to the following perspectives.

### Title

- Does the title alone clearly explain what was changed?
- Is the corresponding ticket number or feature ID listed?
- Are the details described in text as well as using identifiers?

### Content

- **Scope of Work**:
  - What kind of changes did you make?
  - What is the background or reason for these changes?
- **Modified Areas**:
  - Specifically, what modifications were made?
  - What were the technical considerations and decisions?
- **Additional Information**:
  - If a package was added, include a link to its documentation.
  - Include any other information necessary as prerequisite knowledge.
- **Testing**:
  - What kind of tests were conducted?
  - Is evidence (screenshots, logs, etc.) attached?
- **Related Pages**:
  - Are related documents or PRs listed?

## Prefix for Comments

To clarify the intent of review comments, use the following prefixes.

- **must**: Required change.
- **want**: Suggested change (if possible).
- **nits**: Minor point (at the author's discretion).
- **Q**: Question or confirmation of intent.

## Code Review Checklist

Focus on the following items.

- [Confirmation of Input and Output](#confirmation-of-input-and-output)
- [Logic Confirmation](#logic-confirmation)
- [Test Coverage](#test-coverage)
- [Style Consistency](#style-consistency)
- [Naming Conventions](#naming-conventions)
- [Granularity of Classes and Functions](#granularity-of-classes-and-functions)
- [Appropriateness of Comments](#appropriateness-of-comments)
- [Prohibited Items and Anti-patterns](#prohibited-items-and-anti-patterns)

### Confirmation of Input and Output

Verify that the input and output of the implemented code match the design (I/F, etc.).

- **UI/Screens**: Verify the validity of calling parameters.
- **APIs**: Verify the validity of requests and responses.

### Logic Confirmation

Verify the correctness of the implementation based on the following.

- Are the conditions for SQL queries correct?
- Are the parameters for create, update, and delete correct?
- Are there any issues with conditional branching?
- Is error handling performed appropriately?

### Test Coverage

Verify that testing is sufficient.

- **If test code exists**:
  - Is the writing style correct?
  - Are all necessary patterns covered?
  - Does it negatively impact test execution speed?
- **If test code does not exist**:
  - Is there a description of how the code was tested?
  - Is the execution result (evidence) provided?
  - Are all necessary patterns covered?

### Style Consistency

Verify compliance with project standards.

- Is the implementation flow consistent (e.g., controller → transaction → service → repository)?
- Is there consistency in naming conventions?
- Is there consistency in the granularity of file separation?

### Naming Conventions

Verify that naming clearly conveys intent.

- **Entities (Classes, Fields, etc.)**:
  - Does the name clearly represent the entity?
  - Can the values stored in fields be inferred?
- **Actions (Functions, Methods, etc.)**:
  - Does the name start with a verb?
  - Does the name briefly represent the internal processing?
  - Can the return value be inferred from the name?

### Granularity of Classes and Functions

Keep the logic within functions as simple as possible.
Insufficient separation leads to decreased readability and bugs caused by misunderstandings when others reuse the code.
If a function name and its logic do not match, the granularity may be an issue; consider further separation.

### Appropriateness of Comments

Ideally, intent should be conveyed by naming alone, but comments are recommended for complex logic or special processing.

- Supplement complex specifications with background and intent in comments.
- Note: The language of comments should follow project policy.

### Prohibited Items and Anti-patterns

Ensure the following items are not present.

- **Direct Use of Magic Numbers**:
  - Define meaningful numbers or strings as constants.
- **Bloated Functions or Classes**:
  - Consider separation if a function exceeds 100 lines or if a class has too many responsibilities (violating the Single Responsibility Principle).
- **Inclusion of Debug Code**:
  - Ensure `console.log`, temporary comments, or unused variables are not left behind.
- **Emotional Reviews**:
  - Reviews are for the "code," not the person. Avoid language that could be seen as a personal attack.
  - Avoid aggressive language and provide constructive feedback.

---

Related Documents:
- [Issue Creation Policy](./issue.md)
- [Pull Request Creation Policy](./pull-request.md)
- [Commit Conventions](./commit.md)

