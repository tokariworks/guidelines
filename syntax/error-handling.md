# Error Handling and Debugging

Error handling is critical for maintaining the robustness and reliability of Tokari Works visual novels. This document describes conventions and best practices for identifying, managing, and debugging errors within narrative scripts and supporting code.

## 1. Error Prevention

- Validate all variables and flags before use.  
- Use safe defaults when data may be missing or undefined.  
- Employ early conditional checks to avoid runtime failures.

## 2. Logging and Reporting

- Use in-engine debug logs or console output when available.  
- Include descriptive messages when logging errors, indicating context and expected vs. actual state.  
- Capture stack traces or script references to help pinpoint error locations.

## 3. Script Fail-Safes

- Provide fallback dialogue or alternative scenes if critical flags or data are missing.  
- Avoid script crashes by anticipating null or undefined values and handling them gracefully.  
- Gracefully degrade complex features or effects if dependent systems fail.

## 4. Debugging Workflow

- Use version control tools (e.g., git) for rollback, branching, and comparing changes.  
- Integrate linting and static analysis tools to catch syntax and style issues early.  
- Conduct iterative playtesting focusing on branching paths and variable states.  
- Maintain detailed bug reports with reproduction steps.

## 5. Best Practices

- Document complex logic and potential failure points in comments.  
- Isolate error-prone code into modular, testable functions or scripts.  
- Collaborate closely with QA and team members to reproduce and resolve bugs quickly.
