# Ferrum Mesh Raft Hub Walkthrough

I use this file as a small checklist before changing the SQL implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 214 | ship |
| stress | lease drift | 157 | ship |
| edge | replica lag | 221 | ship |
| recovery | membership churn | 249 | ship |
| stale | quorum health | 217 | ship |

Start with `recovery` and `stress`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The useful comparison is `membership churn` against `lease drift`, not the raw score alone.
