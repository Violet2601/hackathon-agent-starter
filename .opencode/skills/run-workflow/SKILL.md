---

name: run-workflow
description: Use when the user wants to execute a previously saved workflow by referencing its keyword.
-------------------------------------------------------------------------------------------------------

# Run Workflow

## When to use this

Use when the user:

* Runs a workflow.
* References a workflow keyword.
* Requests execution of a saved command sequence.

Examples:

```text
run workflow react
run workflow deploy
run workflow docker
```

## Procedure

1. Extract the workflow keyword.

Example:

```text
react
```

2. Read `.opencode/workflows.yaml` and find the matching keyword.

3. If found, retrieve the associated description, variables, and commands.

4. If not found, report: "No workflow found for keyword `<keyword>`." and stop.

5. Resolve any variables by asking the user for values.

Example:

```text
project=myapp
```

becomes:

```bash
npm create vite@latest myapp -- --template react
```

6. Before execution display:

* Workflow name
* Workflow description
* Commands to be executed

7. If Beginner Mode:

Provide a short explanation below every command.

8. Request confirmation.

9. Execute only after confirmation.

10. Report success, failure, or errors.