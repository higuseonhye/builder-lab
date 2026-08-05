# EXP-001 Target Shift

## Status

Planning

## Question

Can a small Physical AI system recover when the target changes after the system
has already committed to an action?

## Motivation

This experiment is the first Builder Lab translation of the After the Spill
program into hardware. The event is intentionally small: the target moves after
commitment. The goal is not to prove a broad theory, but to create a reproducible
setup where recovery behavior can be observed, logged, and compared.

## Minimal Setup

To be determined.

Candidates:

- Low-cost tabletop arm
- Camera or fixed overhead observation
- Simple movable target object
- ROS 2 logging
- Isaac Sim counterpart, if feasible

## Planned Conditions

| Condition | Description |
| --- | --- |
| Static target | Target remains where the policy expects it |
| Early shift | Target moves before action commitment |
| Mid shift | Target moves during approach |
| Late shift | Target moves near contact |

## Planned Measures

- Task completion
- Final distance to target
- Recovery latency
- Number of corrective actions
- Whether the system continues, replans, pauses, or requests intervention

## Evidence Rule

No claim is made until the protocol, run logs, and at least one reproducible
artifact exist.
