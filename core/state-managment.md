# State Management

State management is fundamental to dynamic and coherent visual novel experiences. It involves tracking and manipulating narrative variables, flags, and conditions to ensure continuity and player agency.

## 1. Types of State

- **Global State**  
  Variables persisting throughout the entire playthrough (e.g., player attributes, major plot flags).

- **Scene State**  
  Temporary variables scoped to a specific scene or chapter, reset or discarded after the scene concludes.

- **Character State**  
  Emotional or relationship parameters tied to individual characters, influencing dialogue and event availability.

## 2. State Representation

- Use clear, descriptive variable names adhering to naming conventions (see `syntax/naming-conventions.md`).  
- Organize variables into logical groups or namespaces to avoid collisions and improve maintainability.

## 3. State Mutations

- Prefer atomic, isolated state changes to minimize unintended side effects.  
- Use setter functions or controlled interfaces to update state, encapsulating validation logic.  
- Avoid direct manipulation of state from multiple sources; centralize control when possible.

## 4. State Persistence and Serialization

- Persist global and critical state between sessions using engine-supported save/load systems.  
- Ensure all variables critical to narrative branching are serialized correctly to prevent inconsistencies.

## 5. Common Patterns

- **Flagging**: Boolean variables marking if a player has seen a scene, made a choice, or triggered an event.  
- **Counters**: Numerical variables tracking player progress or repeated actions.  
- **State Machines**: Represent complex conditions as states with defined transitions (e.g., character moods).

## 6. Best Practices

- Document all variables with purpose, scope, and allowed values.  
- Minimize use of “magic numbers” or ambiguous flags.  
- Use constants or enumerations for fixed value sets.  
- Regularly audit state usage to detect dead or redundant variables.
