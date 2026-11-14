# Contributing

## Changelogs and releases

Every merged user-facing change adds an entry to the relevant CHANGELOG.md (root, website/, or the public repo). Releases (TestFlight, site deploy, tags) fail without one. Batch site deploys into releases.

The Changelog PR check requires a new nonempty entry under `## [Unreleased]` and a standard category, compared with the base branch. A dated-section addition does not satisfy the PR check. Existing entry text must be preserved; moving or editing an old entry is not a new entry. Documentation in docs/, tests, CI files and contribution policy are excluded; mixed product changes still require an entry. A maintainer can set `no-changelog` for changes with no user-facing effect. This label is not a release waiver.
