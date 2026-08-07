# Human Interface Measurement — Kick Scooter Hand Brake

Version 0.1 · Status: **Not yet measured · deferred 2026-08-07**

> **Why this is here but not active.** A brake lever is the cheapest real
> instance of a human vehicle control: it has slop, no spec sheet, and cannot be
> modified. That made it the first candidate target. It was deferred, not
> rejected — the lever is a control without an operator position, and the
> direction now requires both. It returns when the operator question is settled.
> The measurement method below is unaffected by that decision.

## Why this exists

Interfaces built for humans ship without a spec sheet. This one is worse than
that: the lever is loosely built, so it does not hold a single stable value.

That is not a measurement problem. **The spread is the result.** A lever that
responds differently pull to pull generates mismatch for free, which is the
condition the program exists to study. Measure the spread, not the average.

Target interface: a child's kick scooter with a **hand brake lever** and no other
control surface. One degree of freedom, no confounds.

## Subject

| Field | Value |
| --- | --- |
| Scooter make / model | |
| Approximate age of unit | |
| Brake type (cable rim / cable disc / other) | |
| Lever material (steel / aluminum / plastic) | |
| Photo reference | |
| Measured by | |
| Date | |

## A. Geometry

Measure with a ruler. Photograph each measurement with the ruler in frame.

| ID | Quantity | Unit | Value |
| --- | --- | --- | --- |
| G1 | Handlebar grip diameter | mm | |
| G2 | Lever length (pivot to lever tip) | mm | |
| G3 | Pivot-to-grip vertical offset | mm | |
| G6 | Handlebar height from ground | mm | |

## B. Slop

This section exists because the lever is not precisely built. Anything here that
is large will dominate the experiment.

| ID | Quantity | Unit | Value | Notes |
| --- | --- | --- | --- | --- |
| B1 | Lateral play at lever tip (side to side, unloaded) | mm | | Decides whether a gripper can stay on it |
| B2 | Does the lever visibly bend under full pull? | yes/no | | If yes, some gripper force goes into bending, not braking |
| B3 | Does the pivot rattle or rock? | yes/no | | |
| B4 | Cable free play at rest | mm | | |
| B5 | Does the lever return to the same rest position each time? | yes/no | | Test 10 releases |

## C. Travel — as a band, not a point

Free travel is unlikely to be repeatable. Record the range across 10 slow pulls.

| ID | Quantity | Unit | Min | Max | Typical |
| --- | --- | --- | --- | --- | --- |
| G4 | Travel from rest to first wheel drag | mm | | | |
| G5 | Travel from rest to lockup or bar contact | mm | | | |

Was a crisp "first bite" point identifiable at all? yes / no: ______

If no, say so plainly here — an interface with no detectable bite point is a
finding, and it changes what the controller has to sense.

## D. Force — spread is the primary result

Measure at the **lever tip**. Force scales with grip position, so also take one
reading at mid-lever for comparison.

| ID | Quantity | Unit | Min | Max | Median | n |
| --- | --- | --- | --- | --- | --- | --- |
| F1 | Force at first wheel drag, lever tip | N | | | | |
| F2 | Force at lockup, lever tip | N | | | | |
| F3 | Force at lockup, mid-lever | N | | | | |
| F4 | Force to hold lockup for 10 s | N | | | | |

**F5 — spread ratio:** `F2(max) / F2(min)` = ______

F5 is the headline number of this sheet. It states how wrong a fixed-force
controller will be, and it is the reason this interface is worth studying.

### Method

For **single values**, no equipment is needed:

1. Hang a plastic bag from the lever tip with string.
2. Add water or coins until the wheel first drags → mass → F1.
3. Keep adding until the lever bottoms out → mass → F2.
4. Convert: **force (N) = mass (kg) × 9.81**.

For **spread**, the bag method is too slow to repeat 10 times. A luggage scale
(hook it to the lever tip, pull along the lever's arc, read peak) makes 10 pulls
trivial. Since spread is now the main result, the scale is worth buying.

Method used: ______________________  ·  n pulls: ______

## E. Mounting

The scooter must be held rigidly for any bench test. Record how.

| Field | Value |
| --- | --- |
| Fixture used | |
| Is the front wheel free to spin? | |
| Can the lever be reached without the fixture blocking it? | |

## F. Derived requirements

Fill in only after B, C, and D are complete. These numbers select the hardware.

| Requirement | Derived from | Value |
| --- | --- | --- |
| Minimum gripper closing force | F2 **max**, plus margin | |
| Minimum end-effector stroke | G5 max | |
| Minimum grip opening | G1 | |
| Gripper compliance needed | B1, B2 | |
| Minimum reach from mount point | G6, E | |

Size the actuator to **F2 max**, not the median. A gripper sized to the average
fails on roughly half the pulls.

## G. Kill conditions

Record the finding and stop **before purchasing anything** if either holds.

| ID | Condition | Value | Triggered? |
| --- | --- | --- | --- |
| K1 | F2 max exceeds what an affordable tabletop arm can deliver | | |
| K2 | B1 lateral play is large enough that a fixed gripper slips off the lever | | |

If K1 or K2 triggers, name the next candidate interface here: ______________

Note that a large F5 is **not** a kill condition. Variance is the subject, not an
obstacle.

## Evidence rule

This sheet is not a result until every value is filled and the photos exist. An
unfilled sheet is a plan, not evidence.
