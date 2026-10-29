# Spital Hill Network Website

A planned public-facing website for the charity. Its purpose is to help members of the public understand the organization, learn about its activities, and find an approved way to get in touch.

## Project status

The project is in the specification stage. The charity's public name, approved content, and contact details have not yet been confirmed. This repository does not yet contain the website implementation.

## Initial release

The first release is intended to be a small, primarily informational website. It should:

- Explain the charity's purpose and summarize its approved activities.
- Clearly identify the organization as the source of the information and indicate when it was last reviewed.
- Provide clear navigation and an approved contact route.
- Work on phone, tablet, and desktop screens, and support keyboard navigation with visible focus.
- Make essential information available as text, with appropriate alternatives for meaningful images.
- Avoid requiring visitor accounts or collecting personal information.

Online donations, accounts, contact forms that collect personal information, event booking, and a news publishing system are outside the initial scope.

## Planned technology and deployment

The site is planned to use [Astro](https://astro.build/) to generate static files. React may be used for interactive components if needed, but the informational site should not require a client-side React application, a running application server, or a database.

The expected deployment is to build the static output with npm and serve the generated files using Apache. Apache configuration and deployment automation have not yet been specified.

## Content and release readiness

Before publication, the organization needs to approve:

- Its public name, purpose, service area (if applicable), and activity descriptions.
- The contact method and details to publish.
- Any images and any additional first-release information, such as opening hours, location, accessibility information, or social links.

Unapproved or unavailable information should not be presented as confirmed. Published links should be checked before release.
