---
name: gridshift-ui
description: Design, review, and implement original, production-minded interfaces for technical products, data-heavy dashboards, Web3 and DePIN tools, infrastructure consoles, and modern web applications. Use when improving visual hierarchy, interaction design, responsive behavior, accessibility, or overall UI polish without copying a specific brand.
---

# Gridshift UI

## Purpose

Create distinctive, production-minded interfaces where visual character supports the product's real purpose. For technical dashboards, this may mean a precise monochrome system with restrained terminal-inspired details; for other products, adapt the visual language to the audience and existing brand.

The goal is **clear, credible, usable, responsive, and memorable**—not a generic SaaS template, fictional hacking interface, or collection of decorative cards.

Read only the reference documents relevant to the current task.

## Start Here

1. Inspect repository instructions, app structure, framework, design system, dependencies, routes, and data models before changing code.
2. Read `references/README.md` for the reference index.
3. Read `references/design-principles.md` and `references/product-and-information-architecture.md` for dashboard work.
4. Read `references/visual-system.md` for visual styling and `references/motion-and-interaction.md` for interactive or animated work.
5. Read `references/engineering-and-accessibility.md` before implementation and `references/quality-checklist.md` before declaring work complete.
6. Treat screenshots, URLs, and product references supplied by the user as evidence. Do not claim an uninspected reference has a specific layout or behavior.

## Core Principles

- **Product before decoration:** every visual decision should support a user goal, information hierarchy, or meaningful feedback.
- **Distinctive, not derivative:** develop an original visual system. Do not reproduce one reference product's exact screens, assets, copy, or branding.
- **Readable contrast:** use color, typography, spacing, and borders to establish hierarchy. Effects must never compromise legibility.
- **Purposeful density:** present useful information efficiently without crowding or overwhelming the user.
- **Honest data:** distinguish live, calculated, unavailable, and mock values. Never fabricate live activity or product capabilities.
- **Responsive by design:** define how layout, navigation, tables, charts, and actions behave at narrow and wide sizes.
- **Accessible interaction:** visible focus, keyboard support, meaningful labels, sufficient contrast, and reduced-motion support are part of implementation—not optional polish.

## Required Workflow

### 1. Discover

- Read relevant project and agent instructions first.
- Identify the primary user, workflow, and most important action.
- Identify which data is real, derived, unavailable, or mocked.
- Preserve the existing architecture and component conventions.
- Check whether the repository already has design tokens, reusable components, or utilities before creating new ones.
- Do not assume the product has wallets, tokens, referrals, reward claims, live APIs, or any other feature unless supported by the repository or user requirements.

### 2. Plan

- Define page hierarchy before styling.
- Choose the smallest set of modules that fulfills the workflow.
- Specify loading, empty, disconnected, error, success, and stale-data states where relevant.
- Plan responsive behavior and keyboard accessibility.
- Reuse existing components and dependencies when appropriate.
- If references are supplied, extract broad principles and translate them into an original solution.

### 3. Implement

- Build reusable primitives for recurring patterns such as metrics, status indicators, tables, timelines, charts, logs, and controls.
- Separate data fetching, business logic, formatting, and presentation where appropriate.
- Keep diffs small and avoid unrelated rewrites.
- Make every visible control functional or clearly disabled with an explanation.
- Use mock data only when necessary and isolate it from production data paths. Label demonstrations as mock/demo data.
- Avoid adding dependencies for effects that can be implemented simply with the current stack.

### 4. Verify

- Run available checks and relevant tests.
- Test primary workflows and important interaction states.
- Check desktop, tablet, and mobile widths.
- Check keyboard navigation, focus visibility, contrast, and reduced motion.
- Confirm animations do not cause layout shifts or block interaction.
- Report what was tested and any limitations honestly.

## Technical Dashboard Priorities

When building a network, infrastructure, or node dashboard, adapt this order to the actual requirements:

1. **Current state and primary action:** connected, disconnected, connecting, syncing, degraded, or error—only if those states apply.
2. **User contribution or core metrics:** show meaningful values, units, and time ranges.
3. **System or network health:** show verified status, activity, synchronization, and uptime where available.
4. **History and analysis:** charts, tables, contribution records, and comparisons.
5. **Event log:** useful timestamped events and warnings as supporting context.
6. **Secondary features:** referrals, rewards, achievements, or account details only if the product actually supports them.

Do not invent protocol mechanics, network statistics, token economics, reward guarantees, or security claims.

## Interaction Rules

- Use motion to communicate state changes, hierarchy, or feedback—not to animate every element.
- Animate only values that genuinely change; never randomize metrics to simulate live activity.
- Use clear labels and confirmation for consequential actions.
- Provide visible hover, focus, pressed, disabled, loading, and error states.
- Respect `prefers-reduced-motion`.
- Keep critical state understandable without color or animation.
- Prefer small, purposeful interactions over effects that delay the user's task.

## Reference Index

- `references/README.md` — reading order and design intent.
- `references/design-principles.md` — visual philosophy and anti-patterns.
- `references/visual-system.md` — palette, typography, borders, texture, and component styling.
- `references/product-and-information-architecture.md` — dashboard concepts, page hierarchy, and module guidance.
- `references/motion-and-interaction.md` — animation, state changes, and interaction patterns.
- `references/responsive-layouts.md` — desktop, tablet, and mobile rules.
- `references/engineering-and-accessibility.md` — implementation and accessibility standards.
- `references/reference-sources.md` — source inspection and verification guidance.
- `references/quality-checklist.md` — pre-delivery quality gate.

## Definition of Done

The result should have a clear purpose, credible information, strong hierarchy, deliberate interactions, responsive behavior, accessible controls, and an original visual identity. It should feel designed for the actual product—not generated from a generic dashboard template.
