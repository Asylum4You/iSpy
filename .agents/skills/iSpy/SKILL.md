# iSpy Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the iSpy TypeScript codebase. You'll learn about file naming, import/export styles, commit message patterns, and how to write and run tests. This guide will help you contribute code that matches the project's established style and workflows.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dataFetcher.ts`

### Import Style
- Use **relative imports** for referencing local modules.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In userProfile.ts
    export function getUserProfile(id: string) { ... }
    ```

### Commit Messages
- Freeform, no strict prefix required.
- Average commit message length: ~35 characters.
  - Example:  
    ```
    Add support for multiple user sessions
    ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new feature.
**Command:** `/add-feature`

1. Create a new file using camelCase naming.
2. Use relative imports to include dependencies.
3. Export your functions or classes using named exports.
4. Write or update corresponding test files (`*.test.*`).
5. Commit your changes with a clear, concise message.

### Fixing a Bug
**Trigger:** When resolving a bug or issue.
**Command:** `/fix-bug`

1. Locate the relevant code file(s).
2. Apply your fix, following coding conventions.
3. Update or add tests to cover the bug fix.
4. Commit with a descriptive message about the fix.

### Writing Tests
**Trigger:** When adding or updating tests.
**Command:** `/write-test`

1. Create or update a test file matching the pattern `*.test.*`.
2. Use TypeScript for test files.
3. Ensure tests cover the intended functionality or bug fix.
4. Run tests using the project's test runner (framework unknown—consult project docs or package.json).

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `userProfile.test.ts`).
- The specific testing framework is not detected; check project documentation or dependencies for details.
- Place tests close to the code they test, using TypeScript.

  Example:
  ```typescript
  // userProfile.test.ts
  import { getUserProfile } from './userProfile';

  describe('getUserProfile', () => {
    it('returns user data for valid id', () => {
      // test implementation
    });
  });
  ```

## Commands

| Command       | Purpose                                 |
|---------------|-----------------------------------------|
| /add-feature  | Scaffold and implement a new feature    |
| /fix-bug      | Apply a bug fix and update tests        |
| /write-test   | Create or update a test file            |
