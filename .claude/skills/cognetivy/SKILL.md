```markdown
# cognetivy Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `cognetivy` TypeScript codebase. It covers file organization, import/export styles, commit message habits, and testing patterns. By following these guidelines, contributors can write code that is consistent, maintainable, and easy to review.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example:  
    ```
    user-profile.ts
    data-fetcher.test.ts
    ```

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { fetchData } from './data-fetcher';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In user-profile.ts
    export function getUserProfile(id: string) { ... }

    // In another file
    import { getUserProfile } from './user-profile';
    ```

### Commit Messages
- Commit messages are **freeform** with no strict prefixes.
- Average commit message length is about 64 characters.
  - Example:
    ```
    Add error handling to user profile fetch logic
    ```

## Workflows

_No automated workflows detected in this repository._

## Testing Patterns

- Test files use the pattern: `*.test.*` (e.g., `user-profile.test.ts`)
- The specific testing framework is not detected, but standard TypeScript testing practices apply.
- Example test file:
  ```typescript
  // user-profile.test.ts
  import { getUserProfile } from './user-profile';

  describe('getUserProfile', () => {
    it('returns user data for a valid ID', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command | Purpose |
|---------|---------|
| /new-file | Create a new TypeScript file using kebab-case naming |
| /add-test | Add a new test file using the *.test.* pattern |
| /import-module | Import a module using relative import style |
| /export-named | Export functions or variables using named exports |
```