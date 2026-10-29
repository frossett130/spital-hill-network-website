# Spital Hill Network Website

An informational website starter for the charity. It uses Astro to generate a static site and
includes React integration for interactive components if they are needed.

## Project status

The project is a working starter. The homepage contains clearly marked placeholders; replace them
only with content approved by the organization. No visitor accounts or personal-data collection
are included.

## Requirements

- Node.js 22.23.4 or newer, using an even-numbered release
- npm

## Getting started

Install dependencies and start the local development site:

```sh
npm ci
npm run dev
```

Open the local address printed in the terminal.

## Available commands

| Command | Purpose |
|---------|---------|
| `npm run dev` | Start the local development site |
| `npm run check` | Check Astro and TypeScript diagnostics |
| `npm run build` | Generate the static site |
| `npm run preview` | Preview the generated site locally |

Run the check and build before sharing changes:

```sh
npm run check
npm run build
```

## Project structure

- `src/pages/` contains the site's pages.
- `src/layouts/` contains shared page layouts.
- `src/styles/` contains global styles.
- `src/components/` is available for reusable components.
- `public/` is for static assets.

The initial page is built with Astro and does not require client-side React. Add React components
only when an approved requirement calls for them.

## Content and accessibility

Do not present unapproved charity details as facts. Before publication, confirm the public name,
purpose, activities, contact route, and review date with the organization. Keep content readable
on small and large screens and ensure interactive elements can be reached by keyboard with visible
focus.
