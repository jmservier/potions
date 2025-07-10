# AGENT RULES FOR NEXT.JS & REACT

## 1. CONTEXT

- Always read `README.md`.
- Check `docs/` for up-to-date project documentation.
- Check data schema definitions in `docs/` or TypeScript types.
- Understand Next.js routing (`/pages`, `app/`) and React component structure.

## 2. DOCUMENTATION

- Store all documentation in the `docs/` folder, as Markdown (`.md`).
- Update documentation for each significant change.
- Document every new feature near its implementation (README, `/docs/`, code comments).
- API documentation must be clear for non-code readers (Swagger/OpenAPI, TSDoc).
- Do not update `README.md` for minor fixes.
- When moving `.md` files, update all internal and external links.
- Avoid duplicate information. Prefer a single source of truth.
- Use TypeScript types for prop and context documentation.

## 3. DEVELOPMENT PRACTICES

- Use TypeScript everywhere.
- Add TSDoc/JSDoc comments for all public functions, hooks, and components.
- Apply atomic design or feature-based structure for React components.
- Prefer `async/await` for async operations.
- Use React hooks (`useEffect`, `useMemo`, `useCallback`, custom hooks) for logic reuse.
- Write tests for all critical components and API routes.
- Use Jest and React Testing Library.
- Add logs before and after major operations.
- Use meaningful error messages (never just "500 Internal Server Error").
- Handle missing data with explicit UI (`<EmptyState />`, messages).
- Do not swallow exceptions; always log and handle properly.
- Refactor files >500 lines into smaller modules.

## 4. TESTS & CI

- Use GitHub Actions for CI.
- Keep CI configuration up-to-date.
- Run `make precommit` before every commit.
- Check and improve test coverage (Codecov or equivalent).
- Add tests for every bug fix.
- Integration tests for key Next.js API routes and pages.

## 5. CODE STYLE & CONVENTIONS

- Respect Next.js folder structure: `/pages`, `/app`, `/components`, `/lib`, `/hooks`, `/api`.
- Use Prettier for formatting and ESLint for linting.
- Do not mix tabs and spaces.
- Add empty lines between logical code blocks.
- Use clear and consistent naming (`useFetchUser` not `useFU`).
- Add TSDoc/JSDoc for components and functions.
- Do not break code indentation.
- Refactor large files.

## 6. DATA & STATE MANAGEMENT

- Use Context API, Redux, Zustand, or Recoil for state.
- Document and type all Next.js API endpoints.
- Use Prisma or Drizzle for database migrations (if applicable).
- Use validators (zod, yup) for data validation.

## 7. PULL REQUEST PROCESS

- Use Conventional Commits (`feat(agent): add x`, `fix(agent): bugfix`).
- Branch names follow ticket or convention.
- PR descriptions must include context, ticket refs, screenshots.
- Always update and check documentation in PR.
- All tests and CI must pass before merge.

## 8. NEXT.JS/REACT SPECIFIC TABLE

| Aspect               | Next.js/React         |
|----------------------|----------------------|
| Doc props/hooks      | TSDoc/JSDoc          |
| Routing              | `/pages`, `app/`     |
| Testing              | Jest, RTL            |
| Logging              | Browser, custom logs |
| Typing               | TypeScript           |
| DB migrations        | Prisma, Drizzle      |
| UI state             | Context, Redux, ...  |
| Error handling       | ErrorBoundary, Sentry|

## 9. REFERENCES

- https://nextjs.org/docs
- https://react.dev
- https://www.typescriptlang.org/docs/handbook/intro.html
- https://testing-library.com/docs/react-testing-library/intro/

## 10. CONTINUOUS IMPROVEMENT

- Track issues, ideas, and improvements in `docs/todo.md`.
- Each significant change must be documented and tested.
- Always prioritize developer and user experience.

