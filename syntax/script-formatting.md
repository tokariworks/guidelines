# Script Formatting

A consistent scripting style is essential for collaboration, scalability, and maintainability in narrative-driven development. This document outlines Tokari Works' standards for formatting visual novel scripts across all projects.

These conventions are designed to support writers, developers, editors, and QA engineers in working within a shared ecosystem, reducing ambiguity and enforcing clarity throughout complex branching structures.

## 1. Indentation and Structure

- Use **4 spaces** per indentation level.
- Do **not** use tabs — tabs render inconsistently across platforms and version control diffs.
- All nested structures (dialogue blocks, menus, conditionals, scene transitions) must follow strict indentation hierarchy.

### Example

```renpy
label station_arrival:

    narrator "The air smells of metal and electricity."

    sakura "Did you ever think we’d come back here?"

    menu:
        "Answer honestly":
            p "Not in a million years."
        "Deflect the question":
            p "Let’s focus on the mission."
```

## 2. Line Spacing and Logical Grouping

- Use **one blank line** between major narrative blocks (e.g., between `label` declarations, between `menu` and its parent dialogue).
- Avoid more than one consecutive blank line, unless separating *sections* within a scene.
- Keep related blocks (conditionals + resulting dialogue, menus + outcomes) visually grouped.

## 3. Commenting Guidelines

- Begin all comments with `#`.  
- Place comments directly **above** the logic or narrative element being explained.
- Use comments to describe **intent, logic, or special conditions** — never restate what is already clear.

### Example

```renpy
# Branch appears only if player previously encountered Sakura
if has_met_sakura:
    sakura "Back so soon? I thought you were done with this place."
```

- Use uppercase comment headers to denote **section titles** within long scenes.

```renpy
# : MIDGAME — DIALOGUE WITH THE RIVAL :
```

- Avoid excessive commenting. Well-written code should be self-evident.

## 4. Dialogue Formatting

- Dialogue lines must begin on their own line, preceded by a clear speaker tag.
- Do not group multiple lines under a single character line.
- Internal thoughts or narration should use either the `narrator` tag or another designated character (e.g., `inner`).

### Example

```renpy
    sakura "You don’t know what it’s like to be erased."

    inner "But I do. I just can’t admit it yet."

    narrator "A gust of wind carries silence between you both."
```

- Use **ellipses (...)**, **em dashes (—)**, or **line breaks** for pacing and tone control.
- Avoid overusing punctuation for dramatic effect. Let structure and context carry weight.

## 5. Menu & Choice Structures

- All menu choices must be indented under the `menu:` declaration.
- Keep the structure consistent:
  - Choice text is quoted on one line.
  - The resulting block is indented to the next level.

### Example

```renpy
menu:
    "Step forward":
        p "I’m ready. Let’s begin."

    "Stay silent":
        p "..."
```

- For longer choice sequences, group them using preceding comments or separate them by a single blank line.
- Avoid redundant choices (e.g., "Say yes" and "Agree"). Each option should have **clear tone and narrative value**.

## 6. Conditional Logic Blocks

- `if`, `elif`, and `else` must each begin on a new line and be followed by an indented block.
- Avoid nesting more than two levels deep.
- Place all conditionals **before** the affected dialogue or event.

### Example

```renpy
if has_confessed and affection_score > 7:
    sakura "I knew you felt the same way."

elif has_confessed:
    sakura "I just... need time."

else:
    sakura "Let’s not pretend something’s happening here."
```

- Use comments if logic becomes non-trivial or relies on earlier states.
- Prefer named flags or functions over repeated logical expressions.

## 7. Maximum Line Length

- Limit each line (dialogue, code, comment) to **100 characters** max.  
- If dialogue must be longer, break it at punctuation points.

```renpy
    narrator "As the train pulled away, everything that had held you here vanished into steam and steel."
```

✅ Good:

```renpy
    narrator "The wind blew harder now, rattling the lanterns—"
    narrator "—as if the night itself were trying to speak."
```

## 8. Label and Scene Declarations

- All `label` declarations must be lowercase and use `snake_case`.
- Use descriptive names for reusability and clarity.

```renpy
label chapter_3_decision_point:
```

- Avoid vague names like `scene1`, `ending`, or `label_a`.

## 9. Sectioning Large Files

- Use structured comment headers to break long scenes into parts:

```renpy
# : ACT I — INTRODUCTION :

# : ACT II — CONSEQUENCES :
```

- Each file should contain only logically related scenes. Consider modularizing long narratives into separate files.

## 10. Code Hygiene and Review

- Remove dead code, commented-out blocks, or placeholder lines before staging.
- Avoid mixing data logic and narrative presentation in the same block.
- Run format linting (if integrated) before commits.
