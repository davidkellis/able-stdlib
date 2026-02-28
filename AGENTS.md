# Able Standard Library — Agent Onboarding

This repository contains the Able v12 standard library, published as an independent
package for use via `able deps install`.

## Structure

- `package.yml` — Package manifest (name: able, version: 0.1.0)
- `src/` — Library source modules
  - `core/` — errors, interfaces, options, iteration, numeric
  - `collections/` — mutable and immutable collection types
  - `text/` — string, regex, ASCII, automata
  - `numbers/` — BigInt, BigUInt, Rational, primitives
  - `concurrency/` — Future, Channel, Mutex
  - `io/` — streams, filesystem
  - `math/` — math utilities
- `tests/` — Smoke test suites
- `*.able` (root) — Top-level facade re-exports (collections.able, core.able, etc.)

## Development

Primary development happens in the main Able repo at `v12/stdlib/`.
This repo is a publish target — updated source is copied here for releases.

## Guidelines

- Keep files under 1000 lines
- Follow the patterns established in existing modules
- Package name is `able` — all imports use the `able.` prefix
- The kernel package (`kernel`) provides host bridges; stdlib depends on it
