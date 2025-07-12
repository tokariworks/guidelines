# Event Triggers

Event triggers are the conditional mechanisms that activate narrative events, scene transitions, or gameplay changes based on player actions, states, or timing.

## 1. Types of Triggers

- **Flag-Based Triggers**  
  Activated when specific boolean variables change state (e.g., `met_character = true`).

- **Counter-Based Triggers**  
  Depend on numeric thresholds or counts (e.g., `friendship_points >= 10`).

- **Time-Based Triggers**  
  Trigger events after elapsed time or specific in-game dates.

- **Sequence Triggers**  
  Activate when a predefined sequence of actions or events occurs.

## 2. Implementation Guidelines

- Define clear trigger conditions to avoid ambiguous activations.  
- Keep triggers modular and reusable where possible.  
- Use descriptive names for triggers and linked events.

## 3. Trigger Hierarchies and Priority

- Establish priority rules when multiple triggers could activate simultaneously.  
- Prevent conflicting triggers by defining mutually exclusive conditions.

## 4. Debugging and Testing

- Log trigger activations during playtests for traceability.  
- Include test commands or cheat codes to manually activate triggers.  
- Monitor for unintended or missed activations.

## 5. Best Practices

- Document all triggers with purpose, conditions, and linked events.  
- Avoid over-reliance on complex nested conditions that reduce maintainability.  
- Coordinate trigger design closely with narrative and systems teams to align story flow.
