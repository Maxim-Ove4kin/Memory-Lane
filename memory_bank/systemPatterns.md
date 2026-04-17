# System Patterns

## Architecture Summary
The project currently follows a simple App Router frontend architecture.

## Main Patterns
| Pattern | Usage |
| --- | --- |
| App Router pages | `src/app/page.tsx` and `src/app/results/page.tsx` define public routes |
| Client components | Both pages run on the client and use React hooks for interactivity |
| Local browser persistence | The search query is stored in `localStorage` before navigation |
| UI primitive composition | `Button`, `Input`, and `Card` primitives are reused from `src/components/ui` |
| Global visual utilities | Sketch borders, shadows, rotation helpers, and color utilities live in `src/app/globals.css` |

## Route Map
| Route | Source File | Responsibility |
| --- | --- | --- |
| `/` | `src/app/page.tsx` | Search entrypoint with mode toggle |
| `/results` | `src/app/results/page.tsx` | Mocked search results list and loading state |

## Known Architectural Gaps
- No server data layer or API routes are implemented.
- No recipe detail route is implemented, even though product docs require it.
- No authentication or Supabase integration is present.
- Search state transfer depends on `localStorage`, which is a temporary prototype approach.
