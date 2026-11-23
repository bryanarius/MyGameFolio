# MyGameFolio Roadmap

Small steps, each about one 30–60 minute session. The phases are an order, not a schedule.
Check off a box when its commit is done.

## Phase 0: Planning and Design
- [ ] Fill in the project outline, sections 1–7 (overview, users, goals, features, scope, stories, screens)
- [ ] Fill in the project outline, sections 8–10 (data, tech stack, risks)
- [ ] Decide on persistence: where is the collection saved? (browser storage / PostgreSQL / later)
- [ ] User flow in Excalidraw (`docs/design/user-flow.excalidraw` + PNG)
- [ ] Low-fi wireframes for each screen in the flow (`docs/design/low-fi/`)
- [ ] High-fi wireframes for each screen (`docs/design/high-fi/`)
- [ ] Update the README with the overview, stack, and a link to the docs

## M1: Game Collection
- [ ] `Game` type and static collection data
- [ ] Render the collection as a list
- [ ] Component test: the list renders every game
- [ ] Filter the collection (by a field chosen in the outline)
- [ ] Rate a game with an immutable state update
- [ ] Tests for filtering and rating

## M2: Preference Analytics
- [ ] Derive stats from the collection (counts, averages, top rated)
- [ ] Unit tests for the stat functions
- [ ] Analytics view that shows the stats
- [ ] Sort the collection

## M3: Express API + IGDB
- [ ] Scaffold `server/` (Express + TypeScript + Vitest)
- [ ] Keep the Twitch credentials in env vars and fetch an IGDB access token
- [ ] Game search route that proxies IGDB
- [ ] Error handling for the route (bad input, IGDB down, rate limits)
- [ ] Search UI with loading and error states
- [ ] Cancel stale searches with AbortController
- [ ] Add a search result to the collection
- [ ] Architecture diagram: client ↔ server ↔ IGDB (`docs/architecture/`)

## M4: LLM Recommendations
- [ ] Recommendations route on the server (API key stays server-side)
- [ ] Build the prompt from the user's collection
- [ ] Recommendations UI with loading and error states
- [ ] Check the recommended games against IGDB
- [ ] Tests for the prompt builder

## M5: Tool Calling + Streaming
- [ ] Stream the LLM response to the client
- [ ] Give the model a tool (for example, IGDB search)
- [ ] Tool status UI ("Searching IGDB…")
- [ ] Cancel a response while it's streaming

## M6: Testing, Deployment, Architecture
- [ ] Fill test gaps across the client and server
- [ ] End-to-end test of the main user flow
- [ ] Deploy the client and server
- [ ] Final architecture diagram and README with screenshots
