# Version policy (beta)

- Each published Windows installer must have a **distinct version string** (example: `0.1.1-beta.1`).
- Do not reuse the same `0.1.0` filename/version for two different binaries.
- `release_sequence` is a strictly increasing integer used for anti-rollback.
- Interrupted publication must not appear as a valid `latest.json` update.
- Replacing Release assets in-place is forbidden; publish a new release identity instead.
