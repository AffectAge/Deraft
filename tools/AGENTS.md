# AGENTS.md — Tools

## Scope
Applies to `tools/` and all subdirectories.

## Mission
Provide practical tooling for developers, mod authors, artists, testers, and server operators.

## Folder Responsibilities
- `launcher/`: local game launch profiles, mod enable/disable UX, logs, crash report collection.
- `asset-pipeline/`: validate and transform textures, models, blockstate data, audio, localization, and packs.
- `dev-server/`: local dedicated server runner, hot reload helpers, diagnostics, profiling, integration test harnesses.

## Goal
Make the game and modding workflow easy to run, debug, package, and validate from day one.

## Skills Needed
- CLI and developer-tool UX.
- Build systems, packaging, and reproducible environments.
- Asset validation and conversion.
- Crash-report processing and log diagnostics.
- Local multiplayer/server orchestration.

## Rules
- Tools should fail with actionable messages.
- Keep automation scriptable for CI and local development.
- Prefer dry-run and validation modes before destructive operations.
- Tools must not require proprietary assets or external services for basic local workflows.
