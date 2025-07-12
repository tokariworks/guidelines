# Version Control Best Practices

Effective version control is essential for collaborative development, traceability, and managing changes in Tokari Works visual novel projects. This document outlines recommended workflows and practices.

## 1. Repository Structure

- Use a single Git repository per project or for shared tools/assets.
- Keep repository size manageable by avoiding large binaries; use Git LFS if needed.
- Use `.gitignore` to exclude build artifacts, temporary files, and user-specific settings.

## 2. Branching Strategy

- Adopt **feature branching**:
  - `main` or `master` branch is always stable and deployable.
  - Create branches named descriptively for features, fixes, or experiments (e.g., `feature/dialogue-system`, `fix/menu-bug`).
- Use pull requests (PRs) or merge requests for code review before merging to main.

## 3. Commit Guidelines

- Write clear, concise commit messages starting with a verb, e.g., "Add", "Fix", "Refactor".
- Group related changes in a single commit.
- Avoid committing incomplete or broken code to shared branches.

## 4. Collaboration

- Regularly pull from the main branch to keep branches up to date.
- Resolve merge conflicts promptly and communicate with the team.
- Review pull requests thoroughly, focusing on functionality, style, and adherence to guidelines.

## 5. Tags and Releases

- Use semantic versioning tags (e.g., `v1.0.0`) for marking stable releases.
- Include changelogs to document features, fixes, and breaking changes.

## 6. Backup and Security

- Host repositories on reliable platforms (GitHub, GitLab, etc.).
- Manage access permissions carefully.
- Regularly back up critical repositories.
