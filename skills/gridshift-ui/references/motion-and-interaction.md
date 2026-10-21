# Motion and Interaction

## Motion philosophy

Motion should communicate arrival, state change, feedback, or data updates. It should not be a permanent distraction.

## Recommended motion patterns

### Initial reveal
- Reveal only a few important elements in a short stagger.
- Keep the duration brief and avoid delaying access to controls.
- Do not replay the entire entrance animation on every small state update.

### Typing or decryption
- Use for a short system greeting, selected status label, or initial terminal line.
- Keep important values and body copy immediately readable.
- Never make users wait for critical information to finish animating.
- Provide a reduced-motion fallback.

### Numeric transitions
- Animate from the previous confirmed value to the new value.
- Avoid rerunning the count-up on every render.
- Do not randomize values to simulate activity.
- Respect precision, units, negative changes, and large numbers.

### Status indicators
- A restrained pulse can indicate a real active state.
- Use distinct static states for disconnected, error, pending, and unknown.
- Never rely on motion or color alone to convey status.

### Hover and focus
- Use subtle border or surface changes.
- Keep focus indicators visible for keyboard users.
- Do not require hover to reveal essential information or controls.

### Charts and tables
- Animate transitions only when the underlying data or selected range changes.
- Keep axes, legends, units, and labels readable.
- Avoid motion that changes the interpretation of data.

## Performance

- Prefer CSS transforms and opacity for simple transitions.
- Avoid animating large areas with filters, blur, or expensive shadows.
- Avoid layout shifts and animations that trigger repeated reflow.
- Keep continuous animations limited to small indicators.
- Clean up timers, observers, and animation loops in component lifecycles.

## Reduced motion

Honor `prefers-reduced-motion`. Remove or shorten decorative animation while preserving the information conveyed by state changes. All functionality must remain available without motion.

## Interaction states

Every interactive component should consider:
- Default.
- Hover.
- Keyboard focus.
- Pressed.
- Disabled.
- Loading.
- Success.
- Error.

For destructive or consequential operations, provide appropriate confirmation and feedback. Do not show success before the operation actually succeeds.
