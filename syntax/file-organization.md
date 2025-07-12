# File Organization and Project Structure

A well-organized file and folder structure is crucial for scalability, collaboration, and maintainability of Tokari Works visual novel projects. This document outlines the recommended conventions and best practices for structuring scripts, assets, and resources.

## 1. Root Directory Layout

- Separate major categories into top-level folders:
  - `scripts/` — All Ren'Py or engine scripts, organized by scenes or chapters.
  - `assets/` — Visual and audio assets, subdivided logically.
  - `docs/` — Documentation, design docs, guidelines.
  - `tools/` — Utility scripts, build tools, automation.
  - `tests/` — Automated or manual test scripts.

## 2. Scripts Folder

- Organize scripts by narrative segments, such as:
  - `scripts/chapter_01/`
  - `scripts/characters/`
  - `scripts/common/` for shared scenes or UI logic.

- Use descriptive filenames with lowercase and underscores:
  - `chapter_01_intro.rpy`
  - `sakura_confrontation.rpy`

- Avoid overly large script files; modularize by scene or function.

## 3. Assets Folder

- Divide by asset type and usage:
  - `assets/images/characters/`
  - `assets/images/backgrounds/`
  - `assets/audio/music/`
  - `assets/audio/sfx/`

- Use consistent naming conventions reflecting usage and versioning:
  - `sakura_happy_v01.png`
  - `bg_school_hallway_day.png`

## 4. Documentation

- Store all project design documents and guidelines under `docs/`.
- Include `README.md` files in major folders explaining purpose and structure.

## 5. Tools and Automation

- Place build scripts, converters, or asset processors in `tools/`.
- Include clear instructions for running and updating tools.

## 6. Tests

- Store test scripts or playtest configurations in `tests/`.
- Organize by feature or narrative module.

## 7. Naming and Consistency

- Use lowercase with underscores for all files and folders.
- Avoid spaces or special characters.
- Maintain consistency across the project for ease of navigation and scripting.
