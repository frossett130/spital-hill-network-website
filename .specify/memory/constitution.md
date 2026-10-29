<!--
Sync Impact Report
Version change: not established -> 1.0.0
Modified principles: None; this is the initial constitution.
Added sections: Technical Constraints; Delivery and Review Standards.
Populated template sections: Core Principles; Governance.
Removed sections: None.
Follow-up TODO: Confirm the original ratification date.
-->

# Spital Hill Network Website Constitution

## Core Principles

### I. Public Information Must Be Approved and Clear
The website MUST identify the charity by its approved public name and explain its purpose and
activities using information approved by the organization. Published information MUST identify
the organization as its source and state when it was last reviewed. Unconfirmed details MUST NOT
be presented as facts. This keeps public information accurate and trustworthy.

### II. Accessibility and Responsive Use Are Requirements
The website MUST keep essential content readable and usable across phone, tablet, and desktop
sizes, including without horizontal page scrolling or overlapping content. Every interactive
element MUST be keyboard-operable and show a visible focus indicator. Meaningful images MUST
have text alternatives, and essential information MUST remain available as text. These requirements
make the site usable by people with different devices and access needs.

### III. Collect and Publish Only What the Scope Requires
The initial release MUST remain informational and MUST NOT require accounts or collect visitor
personal information. Donations, payments, contact forms that collect personal information, and
other transactional features MUST NOT be added without an explicitly approved scope change. This
limits privacy risks and keeps the initial service focused.

### IV. Generated Documents Must Use Available Sources
Generated project documents MUST NOT identify, link to, or otherwise disclose ignored or excluded
repository paths. They MUST rely on approved information and sources available to project
collaborators. This prevents deliverables from depending on material that is absent from the
shared repository.

### V. Prefer a Simple, Static Website
The website MUST deliver its informational content as static output without requiring a running
application server or database. Interactive client-side functionality MUST be added only when
needed to meet an approved requirement. This keeps the initial site simple and reliable to host.

## Technical Constraints

The site MUST use Astro to generate static website output. React MAY be used for interactive
components where needed, but the informational site MUST NOT require a React application in the
visitor's browser. The expected deployment builds the output with npm and serves generated files
with Apache. Server hardening and deployment automation are deployment concerns, not requirements
for the website runtime.

## Delivery and Review Standards

Before release, reviewers MUST confirm that the public name, purpose, activities, contact route,
and any published media are approved. Internal navigation and published contact links MUST be
checked. Reviews MUST assess keyboard operation, visible focus, meaningful image alternatives,
and layouts at narrow and desktop widths. Any unavailable external destination MUST be corrected,
removed, or clearly identified before release.

Changes MUST include validation appropriate to their behavior and affected screen sizes. A
release MUST preserve the informational site if an external link is unavailable.

## Governance

This constitution governs project decisions and MUST be considered during planning, implementation,
and review. Amendments MUST document their rationale and impact and receive review and approval
from repository maintainers before adoption.

Constitution versions use semantic versioning: MAJOR for backward-incompatible governance changes,
MINOR for new principles or materially expanded requirements, and PATCH for clarifications and
non-semantic wording changes. Reviews MUST check proposed work and releases for compliance with
these principles; any exception MUST be explicitly approved and recorded with its rationale.

**Version**: 1.0.0 | **Ratified**: TODO(RATIFICATION_DATE): original adoption date unknown | **Last Amended**: 2026-10-29
