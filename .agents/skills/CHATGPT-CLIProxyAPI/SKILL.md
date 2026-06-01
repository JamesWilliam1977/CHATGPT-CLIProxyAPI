```markdown
# CHATGPT-CLIProxyAPI Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the development conventions and workflows used in the `CHATGPT-CLIProxyAPI` Go repository. You'll learn about file naming, import/export styles, commit message patterns, and how to structure and run tests. This guide is ideal for contributors looking to maintain consistency and productivity in this codebase.

## Coding Conventions

### File Naming
- Use **snake_case** for all file names.
  - Example: `api_handler.go`, `user_service.go`

### Import Style
- Use **relative imports** within the project.
  - Example:
    ```go
    import "./utils"
    ```

### Export Style
- Use **named exports** for functions, types, and variables.
  - Example:
    ```go
    // In user_service.go
    func GetUser(id string) (*User, error) {
        // ...
    }
    ```

### Commit Messages
- Follow **conventional commit** patterns.
- Use prefixes such as `feat` for new features and `test` for test-related changes.
  - Example:
    ```
    feat: add support for user authentication
    test: add tests for token validation
    ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new capability or endpoint  
**Command:** `/add-feature`

1. Create a new file using snake_case (e.g., `feature_name.go`).
2. Write your code, exporting functions/types as needed.
3. Use relative imports for internal dependencies.
4. Add or update tests in a corresponding `*.test.*` file.
5. Commit with a message starting with `feat:`.
6. Open a pull request for review.

### Writing and Running Tests
**Trigger:** When adding or updating tests  
**Command:** `/run-tests`

1. Create or update test files matching the pattern `*.test.*`.
2. Write test cases for your code.
3. Run tests using Go's testing tools (e.g., `go test ./...`).
4. Commit with a message starting with `test:`.
5. Review test results and fix any failures.

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `api_handler.test.go`).
- The testing framework is not explicitly specified; use Go's standard `testing` package unless otherwise noted.
- Example test file:
  ```go
  // api_handler.test.go
  package main

  import "testing"

  func TestGetUser(t *testing.T) {
      // test logic here
  }
  ```

## Commands
| Command        | Purpose                                   |
|----------------|-------------------------------------------|
| /add-feature   | Start workflow for adding a new feature   |
| /run-tests     | Run all tests in the repository           |
```
