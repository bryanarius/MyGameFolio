# MyGameFolio

An AI-powered game discovery and portfolio app built with **React**, **TypeScript**, **Node.js**, **Express**, the **IGDB API**, and an **LLM with tool calling and streaming**.

> 🚧 **Status:** Phase 0, planning and design. The client is set up with Vite, React, TypeScript, and Vitest. See the [roadmap](#roadmap).

---

# Overview

MyGameFolio lets users build a collection of the games they've played, rate them, see what their ratings say about their taste, and get game recommendations grounded in their own collection.

The project is a portfolio application that shows modern full-stack and AI application engineering:

- React + TypeScript component architecture
- Immutable state updates and derived state
- An Express backend that proxies a third-party API
- IGDB integration with server-side credentials
- Async data fetching with loading states, error handling, and cancellation
- LLM recommendations grounded in the user's data
- Tool calling and streamed responses
- Automated testing from the first milestone
- Production deployment

---

# Screenshots

_Coming once the first screens are built._

<!-- ## Collection
![MyGameFolio Collection](docs/screenshots/collection.png) -->

---

# Core Features

## Game Collection (M1)

- View your game collection
- Filter the collection
- Rate games

## Preference Analytics (M2)

- Stats derived from your collection and ratings
- Sorting

## Game Search (M3)

- Search IGDB through the Express API
- Add search results to your collection

## AI Recommendations (M4)

- Recommendations based on your collection and ratings
- Recommended games checked against IGDB data

## Tool Calling And Streaming (M5)

- Recommendations stream in as they're generated
- Status updates while the AI uses tools (for example, "Searching IGDB…")
- Cancel a response while it's streaming

---

# Security

- IGDB (Twitch) credentials and the LLM API key are stored only on the server and never reach the browser
- The browser talks only to the Express API, never to IGDB or the LLM provider directly

---

# Automated Testing

- **Vitest:** unit tests for data and stat functions
- **React Testing Library:** component tests that interact with the UI the way a user would

Tests are written alongside each feature, starting at M1.

---

# Design & Architecture Process

MyGameFolio is being planned and designed before development.

## Project Outline

The [project outline](docs/planning/project-outline.md) defines the project's goals, users, scope, screens, and data.

## User Flow

_In progress._

<!-- ![MyGameFolio User Flow](docs/design/user-flow.png) -->

## Low-Fidelity Wireframes

_In progress._

## High-Fidelity Mockups

_In progress._

## Architecture

_Planned for M3, when the client, server, and IGDB are connected._

## From Concept to Production

```text
Project Outline
    ↓
User Flow
    ↓
Low-Fidelity Wireframes
    ↓
High-Fidelity Mockups
    ↓
Implementation (M1–M5)
    ↓
Automated Testing
    ↓
Production Deployment
```

---

# Tech Stack

| Layer              | Technology                                   |
| ------------------ | -------------------------------------------- |
| Frontend           | React, TypeScript, Vite                      |
| Backend            | Node.js, Express, TypeScript (planned)       |
| External API       | IGDB (planned)                               |
| AI                 | LLM with tool calling and streaming (planned) |
| Testing            | Vitest, React Testing Library                |
| Linting            | ESLint, typescript-eslint                    |
| Package Management | npm                                          |
| Version Control    | Git & GitHub                                 |

---

# Project Structure

```text
MyGameFolio/
├── client/          # React + TypeScript app (Vite)
│   └── src/
│       └── test/    # Test setup and tests
├── server/          # Express API (planned, M3)
└── docs/
    ├── planning/    # Project outline and roadmap
    ├── design/      # User flow and wireframes
    └── architecture/
```

---

# Roadmap

The full step-by-step checklist is in [docs/planning/roadmap.md](docs/planning/roadmap.md).

## 🚧 Phase 0: Planning and Design

- [x] Client scaffold (Vite, React, TypeScript, Vitest)
- [ ] Project outline
- [ ] User flow
- [ ] Low-fidelity wireframes
- [ ] High-fidelity mockups

## M1: Game Collection

- [ ] Collection list from static data
- [ ] Filtering
- [ ] Rating with immutable state updates

## M2: Preference Analytics

- [ ] Derived stats, grouping, and sorting

## M3: Express API + IGDB

- [ ] Backend proxy for IGDB
- [ ] Search with loading, error, and cancellation handling

## M4: LLM Recommendations

- [ ] Recommendations grounded in the user's collection

## M5: Tool Calling + Streaming

- [ ] Streamed responses, tool status UI, and cancel

## M6: Testing, Deployment, Architecture

- [ ] End-to-end tests, deployment, and architecture docs

---

# Installation

## Requirements

- Node.js 22+
- npm

## 1. Clone the Repository

```bash
git clone https://github.com/bryanarius/MyGameFolio.git
cd MyGameFolio
```

## 2. Install Client Dependencies

```bash
cd client
npm install
```

## 3. Start the Development Server

```bash
npm run dev
```

---

# Running Tests

```bash
cd client
npm test
```

---

# Lessons Learned

_Added as the project progresses._

---

# Acknowledgements

Game data will be provided by **IGDB**.

https://www.igdb.com/

MyGameFolio is an educational portfolio project and is not affiliated with or endorsed by IGDB, Twitch, or any game publisher.
