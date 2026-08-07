# Builder Lab Roadmap

## Day 0

- [x] Create repository skeleton
- [x] Define mission and public boundary
- [x] Mark current status as Planning
- [x] Add initial experiment sequence
- [x] Add license and gitignore

## Next 7 Days

- [x] Freeze Paper 003 claims separately from Builder Lab
- [x] Define the exclusion rule for hardware selection
- [ ] **Write `Why Human Drivers?` — the purchase gate**
- [ ] Draft EXP-001 target-shift protocol
- [ ] Define minimum telemetry schema for physical runs
- [ ] Decide ROS 2 setup path
- [ ] Decide Isaac-to-hardware comparison boundary

"Choose first tabletop hardware target" was removed on 2026-08-07. Choosing
hardware before the justification exists is how the previous week's direction
drifted — the constraint picked the target instead of the question.

## Next 30 Days

- [ ] Acquire or assemble first hardware setup **(blocked on the purchase gate)**
- [ ] Run first motor/control smoke test
- [ ] Record first reproducible movement artifact
- [ ] Publish EXP-001 protocol before the first real run
- [ ] Add run logs and media only after the system actually moves

## Next 90 Days

- [ ] Complete EXP-001 Target Shift
- [ ] Add EXP-002 Occlusion design
- [ ] Add a minimal Robot Diff comparison for two rollouts
- [ ] Document failures and setup constraints
- [ ] Connect lessons back to the After the Spill program

## Backlog

| ID | Experiment | One-line aim |
| --- | --- | --- |
| EXP-001 | Target Shift | Recover after an unexpectedly moved target |
| EXP-002 | Occlusion | Detect and respond when scene evidence is hidden |
| EXP-003 | Human Intervention | Treat interruption as evidence, not just noise |
| EXP-004 | Recovery Timing | Find when intervention is still useful |
| EXP-005 | Slip / Grasp Loss | Recover after contact state changes |
| EXP-006 | Sensor Delay | Separate latency from true model inadequacy |

## Release Rule

Do not announce Builder Lab broadly until EXP-001 is running. The first public
story should be an experiment in motion, not a repository announcement.
