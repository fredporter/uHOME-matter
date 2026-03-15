# uHOME-matter

## Purpose

Matter and Home Assistant integration extension for the v2 `uHOME` family.

## Ownership

- Matter-facing extension contracts
- Home Assistant bridge surfaces
- local automation integration notes and examples
- validation for repo-owned setup and contract assets

## Non-Goals

- base `uHOME-server` runtime ownership
- shared client-runtime ownership
- canonical runtime semantics owned by `uDOS-core`
- optional cloud sync ownership owned by `uHOME-empire`

## Spine

- `src/`
- `docs/`
- `tests/`
- `scripts/`
- `config/`
- `examples/`

## Family Relation

`uHOME-matter` extends `uHOME` with home automation and local-device
integration. It consumes `uHOME-server` and shared family contracts without
redefining them.

The active v2 split is:

- `uHOME-server` for the base always-on runtime, scheduling, and household
  service ownership
- `uHOME-matter` for Matter, Home Assistant, and local automation extension
  contracts
- `uHOME-client` plus app repos for shared runtime consumption and UI layers
- `uHOME-empire` for optional remote sync and container-style workflow
  extension

## Repo Setup Surface

The scaffold includes:

- `src/matter-bridge-contract.json` as the baseline extension contract
- `src/matter-clone-catalog.json` as the checked-in lane for clone targets and
  adapter profiles
- `src/home-assistant-bridge-definition.json` as the shared bridge definition
  consumed by the server runtime
- `examples/basic-matter-bridge.json` as the smallest Matter bridge example
- `examples/basic-home-assistant-clone.json` as the smallest Home Assistant
  clone mapping example
- `config/bridge-targets.example.json` as the starter local target registry
- `docs/server-runtime-handoff.md` as the runtime boundary handoff from
  `uHOME-server`
- `docs/release-policy.md` and `CHANGELOG.md` for release discipline

## Activation

The v2 repo activation path is documented in `docs/activation.md`.

Run the current repo validation entrypoint with:

```bash
scripts/run-uhome-matter-checks.sh
```
