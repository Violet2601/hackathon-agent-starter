---

name: save-workflow
description: Use when the user wants to create, update, or store a reusable terminal workflow that can later be executed using a workflow keyword.
--------------------------------------------------------------------------------------------------------------------------------------------------

# Save Workflow

## When to use this

Use when the user:

* Wants to save a sequence of terminal commands.
* Wants to create a reusable workflow.
* Wants to associate commands with a keyword.
* Wants to update an existing workflow.

Examples:

* "Save this as a workflow."
* "Create a workflow called react."
* "Remember these commands."
* "Store this deployment workflow."

## Procedure

1. Determine the workflow keyword.

Example:

```text
react
```

2. Collect the commands associated with the keyword.

Example:

```bash
npm create vite@latest {project} -- --template react
cd {project}
npm install
npm run dev
```

Ask for any variables (e.g. `{project}`).

3. Read the file `.opencode/workflows.yaml`.

4. Add or update the entry:

```yaml
<keyword>:
  description: <user-provided description>
  variables: [<var1>, <var2>]
  commands:
    - "<command1>"
    - "<command2>"
```

5. If the keyword already exists:

   * Show the existing workflow.
   * Ask whether it should be replaced.
   * Never overwrite without confirmation.

6. Write the updated YAML back to `.opencode/workflows.yaml`.

7. Confirm the workflow was saved.