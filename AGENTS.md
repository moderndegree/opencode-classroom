# OpenSpec Classroom - Agent Guidelines

## Build & Development Commands

```bash
# Development server
npm run dev

# Production build
npm run build

# Start production server
npm run start

# Linting
npm run lint
```

**Note**: No test framework is currently configured. Tests should be added as needed.

## Code Style Guidelines

### TypeScript & React
- Use TypeScript with strict mode enabled
- Use React 19 with Next.js 16 App Router
- Files: `.ts`, `.tsx`, `.mts`
- Use `Readonly<{ children: React.ReactNode }>` for props in layouts
- Export components as `default function ComponentName()`
- Use `import type` for type-only imports

### Imports & Module Resolution
- Use path aliases: `@/*` maps to `.*/*`
- Import order: React → External → Internal → Types
- Use default imports for default exports
- Use named imports for named exports

### Formatting
- Use 2-space indentation
- Use single quotes for strings
- Use semicolons consistently
- Use PascalCase for component names
- Use camelCase for functions, variables, and hooks
- Use kebab-case for CSS classes and file names

### Styling
- Use Tailwind CSS v4 with `@tailwindcss/postcss`
- Use CSS variables for theme colors (`--background`, `--foreground`)
- Use semantic color names from theme
- Follow existing class naming patterns

### Error Handling
- Use try-catch for async operations
- Return early on invalid inputs
- Use TypeScript non-null assertion (`!`) only when guaranteed
- Add fallback values for optional props

### Naming Conventions
- Components: PascalCase (e.g., `UserProfile`)
- Hooks: `use` prefix (e.g., `useAuth`)
- Constants: UPPER_SNAKE_CASE (e.g., `MAX_RETRIES`)
- Boolean variables: `is`, `has`, `should` prefix (e.g., `isLoading`)

### File Structure
- Pages: `app/<route>/page.tsx`
- Layouts: `app/layout.tsx`
- Components: `app/components/<Component>.tsx`
- Utilities: `lib/<utility>.ts`

## OpenSpec Workflow

This project uses OpenSpec for change management:

```bash
# Propose a new change
/opsx-propose <change-name-or-description>

# Apply a change
/opsx-apply <change-name>

# Explore ideas
/opsx-explore <topic>

# Archive a completed change
/opsx-archive <change-name>
```

See `.opencode/command/` for full documentation.

## Linting & Type Checking

- ESLint with Next.js core web vitals rules
- TypeScript strict mode enabled
- Run `npm run lint` before committing
- Fix all type errors before submitting code

## Git Workflow

- Commit messages should be concise and descriptive
- Use present tense: "Add feature" not "Added feature"
- Reference issue/PR numbers when applicable
