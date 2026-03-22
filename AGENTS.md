# AGENTS.md

This repository contains the opencode-classroom project.

## Build/Lint/Test Commands

Since this repository is currently empty, no build/lint/test commands are configured.

When adding code, common commands for different languages:

**TypeScript/JavaScript:**
- `npm run lint` - Run linter
- `npm run test` - Run all tests
- `npm run test -- --testNamePattern="pattern"` - Run single test
- `npm run build` - Build project

**Python:**
- `ruff check .` - Lint
- `pytest` - Run all tests
- `pytest -k "test_name"` - Run single test
- `mypy .` - Type check

**Go:**
- `golangci-lint run` - Lint
- `go test ./...` - Run all tests
- `go test -run TestName` - Run single test

## Code Style Guidelines

### General
- Follow language-specific conventions (PEP 8 for Python, ESLint for JS/TS, etc.)
- Use meaningful names for variables, functions, and classes
- Write clear, concise comments explaining *why* not *what*

### TypeScript/JavaScript
- Use TypeScript for new code
- Import order: stdlib → external → internal
- Use camelCase for functions/variables, PascalCase for types/classes
- Prefer `const`/`let` over `var`
- Use optional chaining (`?.`) and nullish coalescing (`??`)
- Handle errors with try/catch or proper error types

### Python
- Use PEP 8 style guide
- Import order: stdlib → third-party → local
- Use snake_case for functions/variables, PascalCase for classes
- Type hints required for all function signatures
- Use context managers for resource handling

### Error Handling
- Use specific error types when possible
- Provide meaningful error messages
- Don't swallow errors silently
- Log errors appropriately

## Cursor/Copilot Rules

No Cursor or Copilot rules configured.

## Project Structure

Expected structure:
```
opencode-classroom/
├── src/              # Source code
├── tests/            # Test files
├── docs/             # Documentation
├── examples/         # Example code
└── README.md
```
