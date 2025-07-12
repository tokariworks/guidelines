# Naming Conventions

Consistent and clear naming conventions improve code readability, maintainability, and collaboration in narrative-driven projects.

## 1. General Principles

- Use `lowercase_with_underscores` for variables and flags.
- Use `CamelCase` for function names, structures, and custom types.
- Be descriptive but concise — names should reflect purpose, not implementation.
- Avoid ambiguous, overly generic names (e.g., `temp`, `data`, `stuff`).

## 2. Variables and Flags

- Prefix boolean flags with `is_`, `has_`, or `can_`
  - ✅ `is_locked`, `has_permission`, `can_proceed`
- Use noun-based names for descriptive clarity
  - ✅ `inventory_count`, `player_mood`, `dialogue_branch`
- For temporary scoped values, indicate purpose explicitly
  - ✅ `temp_score`, `debug_output`, `choice_buffer`

## 3. Labels and Scene Identifiers

- Use `snake_case` for labels and script jump points:
  - ✅ `intro_scene`, `chapter_1_start`, `ending_a`
- Prefix with content type if needed:
  - ✅ `scene_library`, `menu_settings`, `choice_love_route`
- Use numeric or mnemonic suffixes for clarity:
  - ✅ `day_01`, `route_sakura_good`, `scene_rival_confrontation`

## 4. Constants and Enums

- Write constants in `ALL_CAPS_WITH_UNDERSCORES`:
  - ✅ `MAX_HEARTS`, `DEFAULT_VOLUME`, `CHOICE_ACCEPT`
- Group related constants or enums into documented blocks.
- Prefer named values over raw numbers or strings in logic conditions.

## 5. Functions and Methods

- Use action-oriented names: `verb_object` or `action_target`
  - ✅ `load_scene()`, `calculate_affinity()`, `save_state()`
- Be explicit if the function causes side effects:
  - ✅ `update_inventory()` vs. `get_inventory()`  
- Avoid prefixing with module/class redundancies unless required.

## 6. File Naming

- Use `kebab-case.md` for markdown files (e.g., `state-management.md`).
- Use `snake_case` for script files or config (e.g., `scene_03_home.rpy`).
- Use descriptive prefixes for content type:
  - ✅ `char_sakura.json`, `bg_school.png`, `ui_options_menu.psd`

## 7. Avoid

- Reserved keywords from the scripting engine or language (e.g., `true`, `label`, `if`)
- Inconsistent casing or style mixing (`SceneIntro`, `scene_intro`, `sceneIntro`)
- Abbreviations unless widely understood (`cfg`, `id`, `npc` are acceptable; avoid `cnfg`, `dbst`, etc.)
