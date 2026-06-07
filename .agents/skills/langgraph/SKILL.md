```markdown
# langgraph Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `langgraph` TypeScript codebase. You'll learn about file naming, import/export styles, commit message conventions, and how to work with and write tests in this repository. This guide will help you contribute code that matches the project's established style and workflows.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.ts`, `langGraphUtils.ts`

### Import Style
- Use **relative imports** for referencing other modules within the project.
  - Example:
    ```typescript
    import { myFunction } from './myModule';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In myModule.ts
    export function myFunction() { ... }

    // In another file
    import { myFunction } from './myModule';
    ```

### Commit Messages
- Follow **conventional commit** style.
- Use the `chore` prefix for maintenance or non-feature commits.
- Keep commit messages concise (average 58 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features, fixing bugs, or making improvements  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Write your code following the coding conventions above.
3. Add or update tests as needed (see Testing Patterns).
4. Commit your changes using the conventional commit format.
5. Push your branch and open a pull request.

### Running Tests
**Trigger:** When verifying code correctness or before submitting a PR  
**Command:** `/run-tests`

1. Identify test files (pattern: `*.test.*`).
2. Use the project's test runner (framework unspecified; check project docs or package.json for details).
3. Run all tests and ensure they pass.
4. Address any failing tests before committing.

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `myModule.test.ts`).
- The specific testing framework is not specified; check the repository for more details.
- Place tests alongside the modules they test or in a dedicated `tests` directory.
- Example test file:
  ```typescript
  // myModule.test.ts
  import { myFunction } from './myModule';

  describe('myFunction', () => {
    it('should return true for valid input', () => {
      expect(myFunction('valid')).toBe(true);
    });
  });
  ```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /contribute    | Start the code contribution workflow         |
| /run-tests     | Run all tests in the repository              |
```