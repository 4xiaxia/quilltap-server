```markdown
# quilltap-server Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `quilltap-server` repository, a TypeScript backend built with Next.js. It covers file organization, code style, commit messaging, and testing practices to ensure consistency and maintainability across the codebase.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example: `user-service.ts`, `api-handler.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { getUser } from './user-service';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // user-service.ts
    export function getUser(id: string) { ... }
    ```

### Commit Messages
- Follow **Conventional Commits** format.
- Use prefixes such as `chore`.
- Keep commit messages concise (average 76 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Code Commit Workflow
**Trigger:** When making any code changes  
**Command:** `/commit`

1. Make your code changes following the coding conventions.
2. Stage your changes:  
   ```
   git add .
   ```
3. Write a conventional commit message, e.g.:  
   ```
   git commit -m "chore: fix API response formatting"
   ```
4. Push your changes to the repository:  
   ```
   git push
   ```

### Testing Workflow
**Trigger:** When adding or updating features or bug fixes  
**Command:** `/test`

1. Write or update test files using the `*.test.*` pattern (e.g., `user-service.test.ts`).
2. Run your test suite (testing framework is unspecified; use your project's test runner).
3. Ensure all tests pass before committing code.

## Testing Patterns

- Test files are named using the `*.test.*` pattern.
  - Example: `user-service.test.ts`
- Place test files alongside the modules they test or in a dedicated test directory.
- Testing framework is not specified; follow your team's standard.
- Example test (using Jest syntax as a placeholder):
  ```typescript
  import { getUser } from './user-service';

  test('should fetch user by ID', () => {
    expect(getUser('123')).toEqual({ id: '123', name: 'Alice' });
  });
  ```

## Commands
| Command   | Purpose                                   |
|-----------|-------------------------------------------|
| /commit   | Guide for making conventional commits     |
| /test     | Steps for writing and running tests       |
```