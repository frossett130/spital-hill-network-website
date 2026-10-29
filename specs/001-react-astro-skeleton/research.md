# Research: React Astro Project Skeleton

## Runtime and project setup

**Decision**: Use the currently documented supported Node.js baseline of 22.23.4 or newer and
npm for package installation and scripts.

**Rationale**: Astro's installation guide lists this Node.js baseline and excludes odd-numbered
Node.js releases. Using the documented supported runtime avoids relying on an outdated local
default.

**Alternatives considered**: Use an older Astro-compatible Node.js release; rejected in favor of
the current installation guide's higher supported baseline.

**Sources**:

- [Astro installation and setup](https://docs.astro.build/en/install-and-setup/)
- [Upgrade to Astro 6](https://docs.astro.build/en/guides/upgrade-to/v6/)

## React integration and rendering

**Decision**: Configure the official `@astrojs/react` integration with `react` and `react-dom`.
Keep the initial page primarily Astro. React components render without client-side JavaScript
unless an explicit `client:*` directive requests hydration.

**Rationale**: This provides a React-capable Astro project while preserving static HTML output
and avoiding unnecessary client JavaScript for the informational starter page.

**Alternatives considered**: Build the whole page as a client-rendered React application; rejected
because it conflicts with the static-first requirement and provides no needed interaction.

**Sources**:

- [Astro React integration](https://docs.astro.build/en/guides/integrations-guide/react/)
- [Framework components](https://docs.astro.build/en/guides/framework-components/)
- [Islands architecture](https://docs.astro.build/en/concepts/islands/)

## Scripts and validation

**Decision**: Provide npm scripts for `dev`, `build`, `preview`, and `check`. Use the Astro CLI
for development and static building, and Astro's check command for Astro and TypeScript
diagnostics. Validate the build, generated-file ignore behavior, and responsive/keyboard
accessibility.

**Rationale**: These cover the contributor workflow in the specification without introducing
a separate test framework for an initial static page.

**Alternatives considered**: Add a full component/browser test stack immediately; deferred because
the initial page has no interactive React behavior and its required outcomes can be checked with
type diagnostics, a production build, and targeted manual review.

**Sources**:

- [Astro CLI reference](https://docs.astro.build/en/reference/cli-reference/)
- [Astro TypeScript guide](https://docs.astro.build/en/guides/typescript/)

## Static output and project scope

**Decision**: Use Astro's default static output in `dist/`; do not add an on-demand rendering
adapter, database, or external service.

**Rationale**: The feature is an informational starter site with no user-specific or persisted
data. Static output is the simplest option and meets the constitution's runtime constraints.

**Alternatives considered**: Server-rendered pages or an API-backed content store; rejected because
no requirement calls for request-time rendering or persistence.

**Source**:

- [Astro configuration reference](https://docs.astro.build/en/reference/configuration-reference/)
