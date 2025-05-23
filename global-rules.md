## Code Quality & Standards
- Write production-ready code only - no placeholders, mocks, or "TODO" comments
- Never use TypeScript `any` type - always provide proper typing
- Use guard clauses instead of nested if statements
- Apply senior dev principles: DRY, composition, component patterns
- Write self-documenting comments that explain purpose and logic

## Development Approach
- Act as the developer with full autonomy - never ask user to perform tasks you can execute
- Preserve existing dependencies - avoid changing pre-existing code when adding features
- Leverage current codebase patterns, structure, and style consistently
- Provide complete code solutions with full file paths and detailed logic

## Technical Specifics
- Use `date +%Y-%m-%d` command to get current date - never assume dates
- For Docker Puppeteer: use `http://host.docker.internal:port` instead of `localhost:port`
- Research errors using available MCP tools before proposing fixes
- Add useful project insights to `.cursor/rules` context file

## Response Format
- Provide concise, actionable fixes based on existing codebase
- Ensure all suggestions align with current tech stack and architecture