# Visual System

## Color tokens

Use these as starting tokens and adapt them to the existing design system.

| Token | Value | Purpose |
|---|---|---|
| `--bg` | `#050505` | Main canvas |
| `--surface-1` | `#0A0A0A` | Primary module surface |
| `--surface-2` | `#111111` | Elevated or active surface |
| `--surface-3` | `#161616` | Stronger module contrast |
| `--border` | `#252525` | Standard divider |
| `--border-strong` | `#383838` | Emphasis and active boundaries |
| `--text-primary` | `#F5F5F5` | Main content |
| `--text-secondary` | `#A0A0A0` | Supporting copy |
| `--text-muted` | `#686868` | Metadata; not for critical text |
| `--focus` | `#FFFFFF` | Keyboard focus outline |

Avoid using muted gray for essential information. Verify contrast in the actual rendered UI.

## Typography

- Prefer JetBrains Mono or IBM Plex Mono for numbers, timestamps, identifiers, labels, tables, and terminal output.
- Use a readable sans-serif for longer explanatory text if it improves scanning.
- Use tabular numerals for changing metrics and aligned ledgers.
- Use uppercase for short section labels, not all prose.
- Establish consistent scales for page title, module title, metric, body, and metadata.
- Avoid overly small text; operational density should not require squinting.

## Layout and spacing

- Establish a predictable grid and align module edges.
- Use consistent spacing tokens and compact but comfortable internal padding.
- Prefer square corners or subtle radii over large pill-shaped containers.
- Use dividers, inset rules, and negative space to distinguish regions.
- Keep the primary node module visually dominant without making it enormous.
- Make tables align numerically and keep units explicit.

## Borders and surfaces

- Use 1px borders with restrained contrast.
- Add subtle inset highlights or very low-opacity gradients only when they improve depth.
- Do not give every module a different visual treatment.
- Avoid strong drop shadows and heavy glass effects.
- Ensure texture never obscures labels, charts, or controls.

## Grid and scanlines

- Keep grids and scanlines at low opacity.
- Prefer CSS pseudo-elements or a single lightweight overlay rather than duplicating texture layers in every component.
- Ensure overlays do not intercept pointer events.
- Disable or reduce decorative texture on small screens or when it affects performance.
- Respect reduced-motion preferences.

## Bracket controls

Bracket styling can be used for technical actions, for example `[ CONNECT NODE ]`. Keep the accessible button name natural, such as “Connect node”; decorative brackets should not be announced unnecessarily. Provide hover, focus, pressed, disabled, and loading states.

## Icons

Use a consistent icon family and restrained sizes. Icons should clarify meaning. Avoid mixing unrelated icon styles or using symbols as a substitute for accessible labels.
