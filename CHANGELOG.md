# Changelog

All notable changes to this project are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- `/sitemap.xml` and `/robots.txt` (generated from `site`, so the Sitemap line always matches). CI checks that the
  sitemap lists exactly the built pages ([#1](https://github.com/lukasgolino/age-of-boom-website/issues/1)).
- CHANGELOG.md, a check workflow (type-check + build on every push and PR), and a release workflow that publishes
  a GitHub release for each `vX.Y.Z` tag, refusing tags that don't match package.json or have no CHANGELOG
  section ([#3](https://github.com/lukasgolino/age-of-boom-website/issues/3)).
