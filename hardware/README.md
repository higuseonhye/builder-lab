# Hardware

Status: Planning

This directory will track hardware options, constraints, purchase decisions,
setup notes, and reproducibility requirements for Builder Lab.

## Selection Criteria

- Affordable enough for personal lab iteration
- Safe for tabletop experiments
- ROS 2 compatible or bridgeable
- Simple to reset between runs
- Good enough sensing for target-shift experiments
- Reproducible by another small lab or individual builder

## Exclusion Rule

Added 2026-08-07, after a day of ideation drifted from the starting question to
an unrelated endpoint through a sequence of individually reasonable steps.

> The machine must already exist in the world, must have been built for a human
> operator, and must be used **without modification**.

This rule excludes purpose-built robot platforms even when they are cheaper,
safer, and better documented. A 1/10 scale autonomous car has no operator
position; scaling a vehicle down to fit a small robot stops it being a human
asset. Both were considered and both fail this line.

## Current Decision

**No hardware has been selected, and none is purchased.**

The exclusion rule was defined today. No candidate has been checked against it
yet, so there is nothing to select from.

Costs have been surveyed so that any future comparison starts from real numbers.
Surveying a price is not a decision to spend.

### Under consideration

A written justification as a purchase gate — why the operator position
specifically, why an existing machine, why now, and what this is not. Proposed
2026-08-07, not adopted.

### Recorded constraint

A force-feedback racing wheel (G29/G920 class) peaks at 2.1–2.3 Nm on a 280 mm
rim, about **15 N** at the grip. A low-cost arm in the SO-101 class carries
about **5 N**. Any candidate pairing has to clear this kind of check before
purchase, not after.

Because force feedback strength is adjustable in software, reaction force can be
swept as an experimental variable rather than fought as a limitation.

## Deferred

- [`scooter_brake_interface_measurement_v0.1.md`](scooter_brake_interface_measurement_v0.1.md)
  — measurement sheet for a kid's kick scooter hand brake. A real control with
  real slop, but no operator position. Held, not discarded.
