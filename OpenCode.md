# Build/Lint/Test Commands

- **Lint:** `task lint`
- **Lint and Fix:** `task lint-fix`
- **Run all tests:** `task test`
- **Run a single test:** `go test <path_to_package> -run <TestName>` (e.g., `go test ./internal/config -run TestLoad`)
- **Format:** `task fmt`

# Code Style Guidelines (Go)

- **Imports:** Group imports by standard library and then by third-party packages.
- **Formatting:** Use `gofumpt` for consistent code formatting.
- **Naming Conventions:** Follow Go's official naming conventions (e.g., `CamelCase` for exported names, `camelCase` for unexported names, `ID` instead of `Id`).
- **Error Handling:** Return errors explicitly; do not use panics for recoverable errors. Handle errors immediately.
- **Variable Declaration:** Prefer `:=` for short variable declarations when possible.
- **Structure:** Organize code into small, focused functions.
