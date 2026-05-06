# Field Notes

`ferrum-mesh-raft-hub` is easiest to review by starting with the fixture, not the prose.

The domain cases cover `quorum health`, `lease drift`, `replica lag`, and `membership churn`. They sit beside the smaller starter fixture so the project has both a compact scoring check and a domain-flavored review check.

The widest spread is between `membership churn` and `lease drift`, so those are the first two cases I would preserve during a refactor.

The point is not to make the repository bigger. The point is to make the important judgment testable.
