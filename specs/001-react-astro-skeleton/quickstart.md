# Quickstart: React Astro Project Skeleton

## Prerequisites

- Node.js 22.23.4 or newer, using an even-numbered release.
- npm.

## Set up and run locally

From the repository root:

```sh
npm ci
npm run dev
```

Open the local address printed by the development command. Confirm that the starter page displays
neutral, clearly marked placeholders rather than unapproved charity details.

## Validate

```sh
npm run check
npm run build
```

Expected results:

- The check command completes without Astro or TypeScript diagnostics.
- The production build completes and writes static output to `dist/`.
- Generated dependency, cache, and build-output files do not appear as untracked files.

## Review responsive and keyboard behavior

At viewport widths of 320 px, 768 px, and 1920 px:

- Confirm essential content does not overlap or require horizontal scrolling.
- Navigate any interactive elements using only the keyboard and confirm focus is visible.
- Confirm placeholder content remains readable when images are unavailable.

The starter page may have no interactive elements; if so, record that keyboard activation is not
applicable and confirm semantic reading order.
