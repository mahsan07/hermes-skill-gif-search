# Gif Search

> Search and download GIFs from Tenor through a controlled command-line workflow.

This repository packages one focused Hermes skill as a public, documentation-first capability. The blueprint below explains the actual operating surfaces, control points, failure paths, and evidence expected from a trustworthy run.

![Detailed systems blueprint for Gif Search](assets/system-blueprint.png)

## The problem it solves

Research is hard to trust when source collection, interpretation, and conclusions are not visibly connected.

## System components

- **Search phrase**
- **Tenor search endpoint**
- **Relevance and content filter**
- **Preview candidates**
- **Downloaded GIF**

## Execution walkthrough

1. **Convert intent into concise search terms**
2. **Query Tenor with a bounded result count**
3. **Inspect previews dimensions and source links**
4. **Filter irrelevant or unsafe results**
5. **Download only the selected asset**
6. **Report attribution and local path**

## Example request

> For a narrow, non-sensitive research question, search and download GIFs from Tenor through a controlled command-line workflow. Return the result, the evidence used to verify it, and any limitations or actions that still require approval.

## Evidence contract

- `request.json` — captures request.
- `inspection.json` — captures inspection.
- `preview.json` — captures preview.
- `execution.json` — captures execution.
- `verification.json` — captures verification.
- `receipt.json` — captures receipt.

A run is complete only when the final artifact can be reopened or re-read and compared with the requested acceptance criteria. An attempted command or successful API response alone is not sufficient proof.

## Safety boundaries

- Confirm the exact target, owner, environment, and authority before acting.
- Preview consequential changes and pause at the approval gate.
- Keep credentials, personal data, and private endpoints out of logs and examples.
- Preserve user work and avoid unrelated changes.
- Report verification failures as incomplete work.

Read [SAFETY.md](SAFETY.md), [SECURITY.md](SECURITY.md), and the detailed [How it works](docs/HOW-IT-WORKS.md) guide before connecting this workflow to a real service or production environment.

## Repository contents

| Path | Purpose |
| --- | --- |
| `SKILL.md` | Trigger conditions and concise agent workflow. |
| `assets/system-blueprint.png` | High-resolution technical architecture poster. |
| `docs/HOW-IT-WORKS.md` | Component and execution-stage details. |
| `docs/EXAMPLES.md` | Safe, review-only, and failure scenarios. |
| `docs/PRODUCT.md` | Audience, problem statement, and maturity. |
| `SAFETY.md` / `SECURITY.md` | Operational and disclosure boundaries. |
| `tests/README.md` | Contract and package validation guidance. |

## Maturity

This is a public reference workflow extracted from a larger private workbench. It does not include a hosted runtime, credentials, or private infrastructure. Adopters must connect compatible tools and validate behavior in their own environment.

## Contributing

Contributions should improve capability accuracy, safe defaults, reproducible examples, or verification evidence without broadening the skill beyond its stated purpose. See [CONTRIBUTING.md](CONTRIBUTING.md).

<!-- JIT-HARNESS:START -->
## Executable harness contract

This repository now includes a typed, task-adaptive harness contract for **Gif Search**. The contract maps the skill to memory, planning, capability-orchestration, and action modules; defines bounded repair and stop behavior; and records skill-specific verification evidence.

```bash
python3 scripts/validate_harness.py
python3 scripts/run_harness.py examples/task.json
python3 -m unittest discover -s tests -p 'test_*.py'
```

The included runner performs validation and dry-run planning only. Live tool or service execution requires a separately reviewed adapter and measured evidence.

- [Task-adaptive harness guide](docs/JIT-HARNESS.md)
- [Typed harness manifest](harness/manifest.json)
- [JSON Schema](harness/harness.schema.json)
- [Example task](examples/task.json)
<!-- JIT-HARNESS:END -->
