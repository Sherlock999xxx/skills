```markdown
# skills Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches best practices for developing TypeScript projects without a framework, focusing on consistent code style, file organization, and testing patterns. It is based on the analysis of the `skills` repository, which emphasizes clarity, maintainability, and modularity in code.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example: `user-profile.ts`, `data-service.test.ts`

### Import Style
- Use **relative imports** for module references.
  - Example:
    ```typescript
    import { fetchData } from './data-service';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In user-profile.ts
    export function getUserProfile(id: string) { ... }
    ```

### Commit Messages
- Commit messages are **freeform** and do not follow a strict prefix convention.
- Average commit message length is about 38 characters.

## Workflows

### Creating a New Module
**Trigger:** When adding new functionality
**Command:** `/create-module`

1. Create a new `.ts` file using kebab-case (e.g., `feature-name.ts`).
2. Implement the functionality using named exports.
3. Use relative imports for any dependencies.
4. Write corresponding test files as `feature-name.test.ts`.

### Writing Tests
**Trigger:** When verifying module correctness
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.ts` in the same directory as the module.
2. Use your preferred testing framework (not specified in the repo).
3. Import the module using a relative path.
4. Write tests for all exported functions.
   - Example:
     ```typescript
     import { getUserProfile } from './user-profile';

     describe('getUserProfile', () => {
       it('returns the correct profile', () => {
         // test implementation
       });
     });
     ```

### Refactoring Code
**Trigger:** When improving or updating existing code
**Command:** `/refactor`

1. Update the relevant `.ts` files, maintaining kebab-case naming.
2. Ensure all imports remain relative.
3. Use named exports for any new or updated functions.
4. Update or add tests as needed.

## Testing Patterns

- Test files follow the `*.test.ts` naming convention.
- Tests are placed alongside the modules they test.
- The specific testing framework is not specified; choose one that fits your project (e.g., Jest, Mocha).
- Example test file:
  ```typescript
  import { fetchData } from './data-service';

  describe('fetchData', () => {
    it('should return data for valid input', () => {
      // test logic
    });
  });
  ```

## Commands

| Command         | Purpose                                   |
|-----------------|-------------------------------------------|
| /create-module  | Scaffold a new module with conventions    |
| /write-test     | Create a test file for a module           |
| /refactor       | Refactor code while following conventions |
```
