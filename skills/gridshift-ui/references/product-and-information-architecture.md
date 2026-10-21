# Product and Information Architecture

## Core principle

Build the dashboard around the user's actual job to be done. For a node-contribution product, the user generally needs to understand: Is my node working? Is it contributing? What have I earned or recorded? How is the wider network performing?

Confirm these concepts against the real product requirements before implementing them.

## Suggested information hierarchy

### 1. Global header

Possible contents:
- Product identity and network/environment label.
- Navigation to dashboard, node, activity, leaderboard, and settings when those routes exist.
- Connection or synchronization status.
- Account controls if authentication exists.

Keep the header compact. Do not invent wallet connection, account login, or network switching if unsupported.

### 2. Node control center

Potential data:
- Node status: connected, disconnected, connecting, syncing, degraded, or error.
- Node identifier or display name.
- Last heartbeat or last successful sync.
- Session duration and uptime window.
- Supported resource or contribution indicators.
- Primary node action.

Rules:
- Status must come from application state or be labeled as a demo.
- Confirm consequential actions when appropriate.
- Show the reason and next step for errors where possible.
- Distinguish current session duration from historical uptime.

### 3. Personal contribution ledger

Potential data:
- Current points or work-unit balance.
- Contribution during a defined period.
- Activity entries with timestamp, event, amount, and status.
- Historical chart with labeled range and units.

Rules:
- Define what each metric means.
- Do not imply points are monetary value or guaranteed rewards.
- Do not add claim/withdraw buttons unless supported by the product.
- Explain pending or unavailable values.

### 4. Network overview

Potential data:
- Active nodes or validators.
- Network activity and throughput if provided.
- Uptime or availability over a labeled time range.
- Last network update and data freshness.

Rules:
- Identify whether a metric is global, local, estimated, or derived.
- Do not compare numbers with incompatible time windows.
- Show empty or unavailable states rather than inventing values.

### 5. Leaderboard

Potential columns:
- Rank.
- User or node identifier.
- Contribution score.
- Change from a previous period, if historical data exists.

Use a compact table, readable numeric alignment, sensible sorting, and pagination or virtualization when the dataset requires it. Make the current user easy to find without over-highlighting.

### 6. System event terminal

Useful entries include actual connection changes, synchronization outcomes, contribution records, and application warnings.

Each entry should include an understandable timestamp, severity or event type, and concise message. Use a bounded, scrollable region when logs are long. Do not let terminal content dominate the entire page.

### 7. Secondary features

Tasks, achievements, referrals, reward claims, device details, or account settings are optional. Include them only when confirmed by the product specification, API, or existing codebase.

## Page layout suggestion

Desktop:
- Compact header across the top.
- Main node status/control module near the top.
- Personal metrics grouped nearby.
- Network history and contribution ledger in the main content area.
- Leaderboard and event terminal as supporting modules.

Mobile:
- Node state and primary action first.
- Personal contribution and points next.
- Historical charts and tables after the essential summary.
- Logs and secondary details in collapsible sections where useful.

## Data integrity

For each displayed value, determine:
1. Source: API, database, local calculation, user input, or mock.
2. Unit and time range.
3. Refresh/update behavior.
4. Loading and stale-data behavior.
5. Empty and error behavior.

Do not label a static value as live. Keep demo data visibly identified in development or demo experiences.
