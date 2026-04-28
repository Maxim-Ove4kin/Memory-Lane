# Architecture Overview

## Project Summary

Memory Lane is a client-side `Vite` application for preserving the shared history of private groups. The application currently works as a lightweight SPA with screen switching in the browser, local persistence through `localStorage`, and a mobile-first interface.

The current product scope is additionally anchored in `PRD.md`, while this file remains the canonical source of the high-level architecture.

## Main Directories

| Path | Purpose |
| --- | --- |
| `index.html` | Single entry point and screen markup |
| `js/app.js` | UI logic, navigation, modal handling, rendering |
| `js/data.js` | Data model, demo data, import/export, local persistence |
| `css/styles.css` | Full visual system, responsive layout, themes |
| `docs` | High-level architecture documentation |
| `memory_bank` | Operational project memory and progress tracking |

## Runtime Architecture

| Area | Current State |
| --- | --- |
| Entry point | `index.html` |
| Routing | no framework router; screens are switched in the DOM |
| State | in-memory UI state plus persistence in `localStorage` |
| Data | groups, events, members, badges, and settings are managed on the client |
| Map | Leaflet is loaded from CDN |
| Styling | custom CSS with light and dark theme support |

## Current Feature Scope

1. Groups list screen with search.
2. Timeline screen inside a selected group.
3. Members board, memory map, and badges screens.
4. Modal creation flow for groups and events.
5. Import and export of project data as JSON.
6. Theme toggle and mobile bottom navigation.

## Product Scope Notes

1. `PRD.md` confirms the same active product scope as the current SPA: groups, timeline, members, map, badges, JSON transfer, themes, and local browser storage.
2. AI-assisted text editing remains planned but is not implemented in the current codebase.
3. PWA positioning is already part of the product story, but the implementation is still partial because offline caching is not yet backed by a `service worker`.

## Known Architectural Gaps

1. No backend or multi-user synchronization.
2. No real AI integration yet.
3. PWA support is partial: manifest exists, but service worker is not implemented.

## Related Documents

1. `README.md`
2. `PRD.md`
3. `memory_bank/projectbrief.md`
