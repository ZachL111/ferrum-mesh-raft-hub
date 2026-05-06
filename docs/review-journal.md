# Review Journal

I treated `ferrum-mesh-raft-hub` as a project where the smallest useful behavior should still be inspectable.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its distributed systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `quorum health`, score 214, lane `ship`
- `stress`: `lease drift`, score 157, lane `ship`
- `edge`: `replica lag`, score 221, lane `ship`
- `recovery`: `membership churn`, score 249, lane `ship`
- `stale`: `quorum health`, score 217, lane `ship`

## Note

The useful failure mode here is a wrong decision on a named case, not a vague style disagreement.
