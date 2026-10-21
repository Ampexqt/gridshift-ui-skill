# Engineering and Accessibility

## Repository-first implementation

1. Read project instructions and agent skill files.
2. Inspect package scripts, dependencies, routes, existing components, and styling conventions.
3. Locate API clients, schemas, types, state management, and current mock data.
4. Identify the smallest coherent implementation plan.
5. Reuse existing patterns and avoid unrelated refactors.

Do not introduce a new framework, component library, animation library, or charting dependency without a clear need.

## Component boundaries

Consider reusable components for:
- Node status and primary action.
- Metric/value display.
- Connection or event status badge.
- Contribution ledger row.
- Leaderboard table.
- Uptime/activity chart.
- Terminal event row.
- Loading, empty, and error states.

Keep data access and business logic separate from presentation when the existing architecture supports it. Use explicit types and avoid unnecessary abstraction.

## Data integrity and failure handling

- Handle loading, empty, stale, error, and success states.
- Do not silently turn API errors into plausible-looking numbers.
- Do not represent mock values as live.
- Format timestamps with a clear timezone policy.
- Include units and time windows for metrics.
- Avoid optimistic success messages for operations that have not completed.
- Keep secrets and API keys out of client-side source code.

## Accessibility

- Use semantic landmarks, headings, buttons, links, and tables.
- Ensure all controls work with a keyboard.
- Provide visible focus states.
- Give icon-only controls accessible names.
- Do not rely on color, glow, or motion alone to communicate state.
- Use meaningful chart labels or an accessible text summary.
- Maintain adequate text and control contrast.
- Avoid overly small text for essential information.
- Respect reduced-motion preferences.
- Make bracket decorations presentational when possible.

## Verification

Use the project's existing lint, typecheck, test, and build scripts where available. Test the key workflow manually or with existing browser tests. Report commands run and any checks that could not be performed. Do not claim tests passed if they were not run.
