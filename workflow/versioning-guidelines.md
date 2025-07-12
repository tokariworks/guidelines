# Versioning Guidelines

Proper versioning ensures organized development, clear history, and controlled releases.

## 1. Branch Structure

- **`main`**: Stable production-ready code.  
- **`develop`**: Integration branch for completed features.  
- **`feature/`**: Branches for new scenes, systems, or fixes (e.g., `feature/write/scene_x`).  
- **`hotfix/`**: Urgent fixes on `main`.

## 2. Commit Messages

- Use imperative mood, concise and descriptive.  
- Prefix messages with context tags:  
  - `draft:` for initial writing  
  - `review:` for revisions  
  - `finalize:` for final changes  
  - `fix:` for bug fixes

Example: `draft: add opening dialogue for scene_05`

## 3. Tagging & Releases

- Use semantic versioning tags (`v1.0.0`, `v1.1.0-beta`).  
- Annotate releases with changelogs summarizing narrative and system changes.

## 4. Merge Protocols

- Require at least two approvals for merges into `develop` and `main`.  
- Use pull requests to review and discuss changes.
