# Builder Lab

Build. Break. Learn. Repeat.

An open laboratory for building small, reproducible Physical AI systems.

Repository description:

> Public execution lab for small, reproducible Physical AI experiments connected
> to the After the Spill research program.

## Current Status

**Planning** as of 2026-08-05.

Builder Lab is in Day 0 setup. No hardware result, robot demo, or experimental
claim is published yet.

## Mission

Builder Lab turns research questions into runnable physical experiments.

Research OS manages the question. Builder Lab runs the experiment. Papers record
the evidence.

```text
Idea -> Experiment -> Evidence
```

The first goal is simple:

> Build one small, reproducible Physical AI system that actually moves.

## What This Repository Is

- A public execution log for tabletop Physical AI experiments.
- A place for reproducible hardware, ROS 2, Isaac Sim, and robot-diff workflows.
- A bridge between the After the Spill research program and physical systems.

## What This Repository Is Not

- Not a claim that hardware experiments are already running.
- Not a private lab notebook.
- Not a product or clinical system.
- Not a place to create new research claims before evidence exists.

## Initial Tracks

| Track | Purpose | Status |
| --- | --- | --- |
| Hardware | Select the first affordable tabletop robot setup | Planning |
| EXP-001 Target Shift | Test recovery after a target moves unexpectedly | Planning |
| ROS 2 | Prepare a minimal control and logging stack | Planning |
| Isaac Bridge | Keep simulation and physical experiments comparable | Planning |
| Robot Diff | Compare rollouts and expose behavior differences | Planning |

## Experiments

Experiments are numbered and kept small.

| ID | Name | Question | Status |
| --- | --- | --- | --- |
| EXP-001 | Target Shift | Can the system recover when the target changes after commitment? | Planning |
| EXP-002 | Occlusion | What changes when part of the scene becomes hidden? | Backlog |
| EXP-003 | Human Intervention | When should a human interruption become evidence? | Backlog |
| EXP-004 | Recovery Timing | How late is too late to intervene? | Backlog |

## Repository Layout

```text
builder-lab/
|-- README.md
|-- ROADMAP.md
|-- hardware/
|-- experiments/
|   `-- EXP-001-target-shift/
|-- ros2/
|-- isaac/
|-- robot-diff/
|-- media/
`-- docs/
```

## Public Boundary

This repository should publish only reproducible plans, configs, logs, results,
and media that are safe to share. Private credentials, unreleased partner data,
private lab assets, and unpublished paper claims stay out.

## Related Workspaces

- Research program: [After the Spill / Research OS](https://github.com/higuseonhye/research-os)
- Public portfolio: [higuseonhye.github.io/research-os](https://higuseonhye.github.io/research-os/)
- Product-facing exploration: Mismatch Lab

## License

MIT License. See [LICENSE](LICENSE).
