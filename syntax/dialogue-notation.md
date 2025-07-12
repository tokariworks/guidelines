# Dialogue Notation

Clear and consistent dialogue notation is essential for managing large branching narratives, ensuring accurate voice acting scripts, and supporting localization, pacing, and readability. This guide outlines Tokari Works' standards for writing and formatting dialogue within visual novel scripts.

## 1. Dialogue Blocks

* Each line of dialogue should begin with a speaker tag followed by the text.
* Use quotation marks **only** inside the line, never around the full line.
* Maintain one speaker per line.

```renpy
    sakura "This place feels different at night."
    p "Yeah... it’s quieter."
```

Use an assigned narrator character or dedicated tag (e.g., `narrator`, `inner`) for thoughts or description:

```renpy
    narrator "The sky shimmered with artificial stars."
    inner "I can’t let her know how nervous I am."
```

## 2. Emphasis and Pacing

* Use **ellipses (`...`)** to show hesitation or trailing thoughts.
* Use **em dashes (`—`)** for interruptions or sudden shifts.
* Use **line breaks** (split into multiple strings) to reflect tempo or pauses.

```renpy
    sakura "I— I didn’t mean to say that..."
    p "You don’t have to explain."
```

Avoid excessive punctuation; let structure communicate rhythm.

## 3. Internal Monologue and Narration

* Use `inner` or another dedicated tag for thoughts.
* Avoid quotation marks in inner monologue unless quoting another character.

```renpy
    inner "This can’t be happening."
    inner "He said, \"I’ll be back before sunset.\" But he never came."
```

## 4. Multiline Dialogue

For lines that are too long or carry multiple narrative beats:

* Break them manually with natural punctuation.
* Keep lines concise, preferably under 100 characters each.

```renpy
    narrator "They stood in silence, their shadows stretching across the pavement."
    narrator "Neither of them moved. Neither of them spoke."
```

## 5. Text Styling and Tags

When using markup tags (e.g., bold, italics, ruby text), follow engine-specific syntax:

* **Do not hard-code styling unless required by the engine.**
* Keep logic and formatting separate whenever possible.

Example (Ren'Py-compatible):

```renpy
    sakura "{i}You promised.{/i}"
    p "I didn’t forget. I just... needed more time."
```

## 6. Special Considerations

* Use inline expressions (e.g., `"You have [points] points."`) sparingly and only when narratively justified.
* For localization, avoid culturally specific idioms unless intentional.
* Use clear variable names in templated strings to maintain translatability.

## 7. Best Practices

* Prioritize clarity and emotional tone over verbosity.
* Avoid excessive wordplay, complex metaphors, or references unless character-appropriate.
* Keep punctuation grammatically correct unless a character’s voice demands otherwise.
* Maintain consistent formatting across all routes.
