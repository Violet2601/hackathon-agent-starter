name: command-generator
description: Convert natural language descriptions into terminal commands.
metadata:
difficulty: beginner

# Command Generator

Convert a user's description into the most appropriate terminal command.

## Inputs

User provides:
- Task description
- Optional operating system
- Optional mode (normal or beginner)

## Procedure

1. Determine operating system.
2. Identify the user's goal.
3. Generate the simplest working command.
4. Verify flags are valid.
5. Return output according to selected mode.

## Beginner Mode

Include:
- Command
- Flag explanations
- Example usage
- Example output
- Common mistakes

## Normal Mode

Include:
- Command
- Short explanation

## Examples

User: Show all files including hidden ones

Output:
ls -la

User: Find every PDF in my home directory

Output:
find ~ -type f -name "*.pdf"