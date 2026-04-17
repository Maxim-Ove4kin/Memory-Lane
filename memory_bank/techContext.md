# Tech Context

## Stack
| Area | Current Choice |
| --- | --- |
| Framework | Next.js 15 |
| Language | TypeScript |
| UI | React 19 |
| Styling | Tailwind CSS v4 plus custom global CSS |
| Components | shadcn-style UI primitives |
| Package Manager Policy | `AGENTS.md` requires Bun for agent-run package commands |
| Linting | ESLint is configured in `package.json`; Biome is not currently configured in the repository |

## Constraints
- Development server must not be started, stopped, or checked by the agent.
- Markdown files should not be passed through Biome.
- Supabase is planned in requirements but not yet wired into the codebase.

## Verification Notes
- Repository contains no Biome configuration or Biome dependency at this time.
- For this task, only Markdown documentation files were added.
