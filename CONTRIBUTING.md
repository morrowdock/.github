# Contributing

## Changelogs and releases

Every merged user-facing change adds an entry to the relevant CHANGELOG.md (root, website/, or the public repo). Releases (TestFlight, site deploy, tags) fail without one. Batch site deploys into releases.

The Changelog PR check covers all files except workflow configuration, tests, and contribution policy. A maintainer can set `no-changelog` for changes with no user-facing effect. This label is not a release waiver.
