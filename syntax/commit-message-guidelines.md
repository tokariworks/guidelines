# Commit Message Guidelines

Consistent and clear commit messages improve project history readability and facilitate collaboration in Tokari Works projects. This document provides standards for writing effective commit messages.

## 1. Format

- Use the imperative mood in the subject line (e.g., “Add feature”, not “Added feature”).
- Keep the subject line concise (50 characters max).
- Separate subject and body with a blank line.
- Wrap the body at 72 characters.
- Use the body to explain *what* and *why*, not *how*.

### Example

Add player dialogue branching for chapter 3

Implemented conditional paths to reflect player choices regarding trust and suspicion. This improves narrative depth and replayability.

## 2. Subject Line

- Capitalize the first letter.
- Do not end with a period.
- Use present tense verbs.

## 3. Body

- Explain the motivation and context for the change.
- Reference relevant issues or tickets if applicable.
- Mention any side effects or considerations.

## 4. Common Prefixes (optional)

| Prefix      | Use case                                   |
| ----------- | ------------------------------------------|
| feat        | New feature                               |
| fix         | Bug fix                                  |
| docs        | Documentation updates                     |
| style       | Formatting, missing semi-colons, etc.    |
| refactor    | Code restructuring without behavior change|
| test        | Adding or fixing tests                    |
| chore       | Maintenance tasks                         |

## 5. Tips

- Make each commit focused and atomic.
- Avoid vague messages like “fix stuff” or “update”.
- Proofread for clarity before committing.
