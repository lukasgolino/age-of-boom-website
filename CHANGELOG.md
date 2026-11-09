# Changelog

All notable changes to this project are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.3.0] - 2026-11-09

### Added

- Umami analytics alongside Cloudflare Web Analytics: cookieless, so still no consent banner, and it adds
  per-visit page journeys (entry page, pages in order, exit), which Cloudflare's aggregate counts can't show.
  All our sites share one Umami website; the Host filter separates them.

## [0.2.0] - 2026-11-06

### Added

- A standard icon set: `favicon.ico` (16/32/48 px), a 96 px icon, a 180 px apple-touch icon and `site.webmanifest`
  with 192/512 px and maskable icons, so search results, tabs, bookmarks and home-screen shortcuts all show the
  icon ([#8](https://github.com/lukasgolino/age-of-boom-website/issues/8)).
- schema.org structured data (JSON-LD) on the home page, an `llms.txt` summary for AI assistants, and robots.txt
  content signals allowing search and AI use; the home page title names what the site is for
  ([#9](https://github.com/lukasgolino/age-of-boom-website/issues/9)).

### Changed

- CI checks are cheap, so they run on every push (and on demand).
  Deploys skip pushes that only touch the changelog, README or CI-only workflows.
- Dependency updates.

## [0.1.0] - 2026-11-05

### Added

- Cloudflare Web Analytics beacon on every page (cookieless, production builds only); CI checks it's on each
  built page ([#2](https://github.com/lukasgolino/age-of-boom-website/issues/2)).
- `/sitemap.xml` and `/robots.txt` (generated from `site`, so the Sitemap line always matches). CI checks that the
  sitemap lists exactly the built pages ([#1](https://github.com/lukasgolino/age-of-boom-website/issues/1)).
- CHANGELOG.md, a check workflow (type-check + build on every push and PR), and a release workflow that publishes
  a GitHub release for each `vX.Y.Z` tag, refusing tags that don't match package.json or have no CHANGELOG
  section ([#3](https://github.com/lukasgolino/age-of-boom-website/issues/3)).

[Unreleased]: https://github.com/lukasgolino/age-of-boom-website/compare/v0.3.0...HEAD
[0.3.0]: https://github.com/lukasgolino/age-of-boom-website/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/lukasgolino/age-of-boom-website/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/lukasgolino/age-of-boom-website/releases/tag/v0.1.0
