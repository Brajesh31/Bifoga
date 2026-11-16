# ADR 0003: Accessible interactive controls

- **Status:** Accepted
- **Date:** 2026-11-17

## Context

The website contains navigation and a JavaScript helper intended to switch visible menu panels. Visual state changes alone are insufficient for keyboard and assistive-technology users.

## Decision

Use native links and buttons where possible. Any tab-like interaction must have an explicit control-to-panel relationship, keyboard support, visible focus, and programmatically exposed selected state. Do not claim accessibility conformance without testing.

## Consequences

- Markup and JavaScript changes must be reviewed together.
- Interaction documentation must match actual IDs and behavior.
- Keyboard and screen-reader checks belong in the verification process.
- Accessibility regressions are treated as functional defects.

## Revisit when

The interaction pattern changes substantially or a component framework is introduced.
