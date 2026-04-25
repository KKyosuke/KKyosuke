# AI Agent Instruction List

This directory (`docs/en/agent/`) manages instruction documents (prompts) and output templates intended for AI agents (such as GitHub Copilot).

## 1. Instructions (`instruction/`)

- [**`instruction/pull-request.md`**](./instruction/pull-request.md)
  - **Purpose**: A prompt used to have an AI automatically execute a code review for a Pull Request.
  - **Overview**: Diagnoses and evaluates whether the implementation and documentation have been done appropriately, using the PR creation policy described in `docs/en/code/pull-request.md` as the evaluation criteria.

## 2. Templates (`template/`)

- [**`template/pull-request.md`**](./template/pull-request.md)
  - **Purpose**: A format used to output the PR review results mentioned above.
  - **Overview**: Includes an overall score, a general summary, and a detailed list of review points (in a table format: Reason / Priority / Overview).
