# Conditional Syntax

A robust conditional system allows branching narratives to respond meaningfully to player input and internal state. This guide defines best practices for writing and structuring conditionals in Tokari Works visual novel scripts.

## 1. Purpose of Conditionals

Conditionals allow scripts to:

* Change dialogue or scenes based on player choices
* Track and reference emotional states, relationships, or variables
* Gate access to specific branches of the story
* Control events through logic-based flags or computed values

A well-written conditional enhances the sense of agency and emotional coherence.

## 2. Syntax and Structure

Use clear, properly indented structures:

```renpy
if has_key_item:
    p "I found it!"
elif knows_secret:
    p "I think I understand now."
else:
    p "I'm still missing something."
```

* Use `if`, `elif`, and `else` blocks to express mutually exclusive paths.
* Always indent the logic inside a conditional by one level (4 spaces).
* Conditionals can precede dialogue, scene transitions, function calls, or menu declarations.

## 3. Boolean Expressions

Write conditions based on boolean logic, flags, or comparisons:

* Boolean flags: `if is_trusted:`
* Variable comparison: `if affection_score > 7:`
* Combined logic: `if has_ring and not has_confessed:`

Use parentheses to group conditions and ensure logical clarity:

```renpy
if (has_letter and not has_opened_it) or knows_secret:
    p "Something doesn't add up."
```

Avoid chaining too many conditions in a single line; break into helper flags or functions when necessary.

## 4. Nested Conditionals

Prefer flat structures. Only nest when absolutely necessary:

```renpy
if has_sword:
    if is_night:
        p "This will be dangerous... but I'm ready."
```

Too much nesting reduces readability. Instead, collapse logic into combined checks:

```renpy
if has_sword and is_night:
    p "This will be dangerous... but I'm ready."
```

## 5. Menu Integration

Conditionals often wrap or gate menu options:

```renpy
menu:
    "Ask about her past" if is_trusted:
        sakura "It’s not something I talk about easily."

    "Stay silent":
        sakura "...Thanks for not pushing."
```

Avoid hiding too many choices at once — this can disorient the player.

## 6. Best Practices

* Use descriptive variable and flag names (e.g., `has_confessed`, `knows_truth`).
* Avoid repeating conditions unnecessarily.
* Document the intent of complex logic with comments.
* Reuse flags for consistency across chapters/scenes.
* Keep logic consistent with the narrative tone and emotional state.

## 7. Common Pitfalls

| Issue                     | Example                              | Recommendation                                     |
| ------------------------- | ------------------------------------ | -------------------------------------------------- |
| Over-nesting              | `if A: if B: if C:`                  | Flatten logic or split into named flags            |
| Vague conditions          | `if value == 1:`                     | Use meaningful flags (e.g., `if is_final_choice:`) |
| Logic inversion confusion | `if not not is_true:`                | Simplify with clear expression                     |
| Duplicate conditions      | `if has_key: ...` in multiple places | Centralize via shared flag or function             |
