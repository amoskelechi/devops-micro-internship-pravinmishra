---
description: Review staged changes and draft a PR title, description, and review notes
allowed-tools: Bash, Read, Grep
disable-model-invocation: true
---

Review the currently staged git changes (git diff --cached) and produce:

1. A PR-readiness report: any secret-like patterns, debug statements, oversized files,
   or mixed/unrelated changes you notice in the staged diff.
2. A suggested PR title.
3. A suggested PR description summarizing what changed and why, based only on the
   staged diff — do not invent context you don't have evidence for.
4. A short list of anything worth a human reviewer double-checking.

Do not run git add, git commit, git push, or open a PR. Only read and report.
