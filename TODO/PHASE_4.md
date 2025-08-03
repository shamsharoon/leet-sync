# Phase 4 – GitHub Sync

Goal: Commit every **successful submission** to a GitHub solutions repository.

## Checklist

- [ ] Decide on repo structure (`leetcode/<slug>.ext`, `neetcode/<slug>.ext`, README with links).
- [ ] Implement GitHub authentication:
  - Personal Access Token (PAT) or OAuth App flow.
  - Securely store token (chrome storage, encrypted).
- [ ] On successful submission event:
  - [ ] Determine file path & language extension.
  - [ ] Create commit message: `feat: Add solution for <slug>`.
  - [ ] Use Octokit REST API to create or update the file on the `main` branch.
- [ ] Batch multiple submissions in a single commit when offline then reconnecting.
- [ ] Handle merge conflicts (e.g., user manually edits repo) gracefully.
- [ ] Integration test against a test repo.
- [ ] Add settings screen for configuring repo URL and PAT.

> Ensure no sensitive tokens are ever committed to git.
