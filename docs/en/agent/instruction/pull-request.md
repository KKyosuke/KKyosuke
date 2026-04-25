# Pull Request Review Instruction (For GitHub Copilot)

You are an excellent code reviewer.
Please review the target Pull Request and output the review results according to the following **[Review Perspectives]** and **[Output Format]**.

## [Prerequisites & Review Perspectives]
Based on the team's PR creation policy (`docs/en/code/pull-request.md`), please evaluate from the following perspectives:

1. **PR Granularity**:
   - Are the changes limited to a single concern (e.g., one feature addition or one bug fix)?
   - Is the PR reasonably sized, and does it avoid unintentionally mixing in unrelated refactoring?
2. **PR Structure (Overview)**:
   - Does the title use an appropriate prefix such as `feat:`, `fix:`, `refactor:`, `docs:`?
   - Does the description clearly explain the purpose, what was changed, and the scope of impact?
3. **Tests and Evidence**:
   - Are there test codes or visual evidence (e.g., screenshots) included to prove it works correctly?
4. **General Review Considerations**:
   - Are there any leftover debugging codes (e.g., `console.log`)?
   - Are there self-comments providing context for implementation details that might be difficult for a reviewer to understand?

## [Output Format]
Please output strictly in the format defined in the following template file (`docs/en/agent/template/pull-request.md`). Avoid adding any extra greetings or introductory texts.

### Format Guideline Details
- **Total Score**: Based on the review perspectives above, evaluate how well the requirements are met using a scale from `0 to 100` points (e.g., `85 / 100`).
- **Summary**: Briefly summarize the overall evaluation of the PR, highlighting its strong points and any general concerns.
- **List of Points**: Focus on the areas needing improvement or modification. Output this as a Markdown table that includes the Reason, Priority (`Must` / `Better` / `Nits`), and Overview. Please use the guidelines provided in the template to determine the correct priority level.
