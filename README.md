# ferrum-mesh-raft-hub

`ferrum-mesh-raft-hub` is a SQL project in distributed systems. Its focus is to implement an SQL distributed systems project for raft graph analysis, using node-edge fixtures and cycle and reachability reports.

## Purpose

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Ferrum Mesh Raft Hub Review Notes

For a quick review, compare `membership churn` with `lease drift` before reading the middle cases.

## What Is Covered

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/ferrum-mesh-raft-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `membership churn` and `lease drift`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Implementation Notes

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `quorum health`, `lease drift`, `replica lag`, and `membership churn`.

The SQL checks add a separate view over the domain review fixture.

## Command

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Audit Path

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Limits

The fixture set is small enough to audit by hand. The next useful expansion is malformed input coverage, not extra surface area.
