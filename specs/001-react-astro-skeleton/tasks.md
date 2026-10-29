# Tasks: React Astro Project Skeleton

**Input**: Design documents from `/specs/001-react-astro-skeleton/`

**Prerequisites**: plan.md, spec.md, research.md, data-model.md, quickstart.md

**Tests**: No automated test tasks were requested. Build, ignore, and accessibility verification
are included as implementation validation.

**Organization**: Tasks are grouped by user story so each story can be implemented and checked
independently after shared project setup.

## Phase 1: Setup

**Purpose**: Declare the project dependencies and supported npm scripts.

- [ ] T001 Define Astro, React, React DOM, TypeScript, and Astro check dependencies plus `dev`, `build`, `preview`, and `check` scripts in `package.json`
- [ ] T002 Install the declared dependencies and generate `package-lock.json`

---

## Phase 2: Foundational

**Purpose**: Configure the static Astro project before implementing individual stories.

- [ ] T003 Configure Astro to use the React integration and static output in `astro.config.mjs`
- [ ] T004 Add strict Astro TypeScript defaults in `tsconfig.json`

**Checkpoint**: Dependencies are installed, Astro is configured for static output, and all user
story work can begin.

---

## Phase 3: User Story 1 - Start development from a ready project (Priority: P1) 🎯 MVP

**Goal**: Provide a runnable, responsive starter site with neutral placeholders and the configured
React integration.

**Independent Test**: Run the local development command and production build. Confirm the page
shows clearly marked placeholders, remains readable from 320 px to 1920 px, and introduces no
horizontal scrolling or content overlap.

### Implementation for User Story 1

- [ ] T005 [P] [US1] Create a semantic shared page shell with viewport metadata in `src/layouts/SiteLayout.astro`
- [ ] T006 [P] [US1] Add responsive base styles and visible keyboard focus styles in `src/styles/global.css`
- [ ] T007 [US1] Build the neutral placeholder home page using the shared layout and stylesheet in `src/pages/index.astro`
- [ ] T008 [US1] Run `npm run check` and `npm run build`; review the generated page at 320 px, 768 px, and 1920 px and verify keyboard reading order

**Checkpoint**: A new contributor can run the static starter page with no unapproved charity
claims, visitor data collection, or unnecessary client-side hydration.

---

## Phase 4: User Story 2 - Understand and maintain the project (Priority: P2)

**Goal**: Document the project and local contributor workflow without hosting or server guidance.

**Independent Test**: Follow the README prerequisites and commands; verify they match the project
scripts and that the README describes no production hosting or server configuration.

### Implementation for User Story 2

- [ ] T009 [US2] Update `README.md` with project purpose, Astro and React stack, prerequisites, and local install, development, check, and build commands; remove deployment, hosting, and server-configuration information and add no server configuration files anywhere in `.`

**Checkpoint**: Contributors can set up and build the project from the README alone.

---

## Phase 5: User Story 3 - Keep generated files out of version control (Priority: P2)

**Goal**: Keep installed dependencies, framework caches, and static build output out of source control.

**Independent Test**: After dependency installation and a successful build, verify the generated
dependency, cache, and output directories are ignored by Git.

### Implementation for User Story 3

- [ ] T010 [US3] Add ignore rules for installed dependencies, Astro caches, and generated static build output in `.gitignore`
- [ ] T011 [US3] Verify generated files are ignored with `git check-ignore` and confirm no generated paths appear as untracked files in `git status --short`

**Checkpoint**: Installing and building the project does not add generated files to repository status.

---

## Phase 6: Polish & Cross-Cutting Concerns

**Purpose**: Validate the complete contributor workflow and ensure documentation matches the project.

- [ ] T012 Run the complete validation flow in `specs/001-react-astro-skeleton/quickstart.md` and confirm all documented npm commands exist in `package.json`

---

## Dependencies & Execution Order

### Phase Dependencies

- **Setup (Phase 1)**: No dependencies; complete T001 before T002.
- **Foundational (Phase 2)**: Depends on the project dependencies declared in T001; complete
  T003 and T004 before the user story phases.
- **User Story 1 (Phase 3)**: Depends on the shared setup and Astro configuration; T005 and T006
  can run in parallel, and T007 follows them.
- **User Story 2 (Phase 4)**: Depends on T001 so README commands can match the declared scripts.
  It is independent of page implementation after setup.
- **User Story 3 (Phase 5)**: Independent after setup; ignore rules can be added alongside page
  and README work.
- **Polish (Phase 6)**: Depends on all desired stories being complete.

### User Story Dependencies

- **US1 (P1)**: Depends on setup and foundation only; provides the MVP.
- **US2 (P2)**: Depends on the declared package scripts in US1 setup, but not on the page content.
- **US3 (P2)**: Depends on the generated paths described by setup and plan; independent of US1
  content and US2 documentation.

### Parallel Opportunities

- T005 and T006 can be implemented in parallel because they create separate files.
- After shared setup, US2's README work and US3's `.gitignore` work can proceed in parallel
  with US1 page work.
- Run story-specific validation after its implementation tasks; run T012 after all stories.

## Implementation Strategy

1. Complete setup and foundational configuration.
2. Deliver **US1 as the MVP** and verify its local server and static build workflows.
3. Add README guidance (US2) and ignore rules (US3) independently.
4. Run the end-to-end quickstart and repository cleanliness checks.
