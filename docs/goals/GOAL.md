# Goal — Original Forge-Moddable Voxel Sandbox

## North Star
Create an original voxel sandbox game with a powerful Forge-like modding platform, dedicated-server support, data/resource packs, and a stable API for community-created gameplay.

## Non-Goals and Boundaries
- Do not copy Minecraft code, assets, protected names, textures, sounds, protocol details, or proprietary data.
- Do not require proprietary game files to build, test, or run.
- Do not make engine systems depend on built-in content.
- Do not treat modding as an afterthought; built-in gameplay should exercise the same extension points.

## Milestone 0 — Project Foundation
Acceptance criteria:
- Repository structure matches the folders described in root `AGENTS.md`.
- Coding standards, contribution workflow, and compatibility policy are documented.
- Minimal app boots into a blank window or headless server mode.
- CI runs formatting, linting, unit tests, and example-mod checks.

## Milestone 1 — Core Voxel Engine
Acceptance criteria:
- Chunk coordinate system and block storage exist.
- Blocks have namespaced IDs and state properties.
- World save/load supports versioning.
- Chunk meshing renders visible block faces.
- Basic movement, collision, and block raycast work.

## Milestone 2 — Client/Server Runtime
Acceptance criteria:
- Dedicated server can host a world.
- Client can connect, load chunks, and receive authoritative updates.
- Packet codecs are versioned and tested.
- Server tick is deterministic for core simulation.
- Crash reports include mod list and lifecycle phase when relevant.

## Milestone 3 — Forge-Like Mod Loader
Acceptance criteria:
- Mods declare metadata in `mod.json`.
- Loader resolves dependencies and reports conflicts clearly.
- Lifecycle phases run in deterministic order.
- Event bus supports priorities and cancellable events.
- Registries support deferred registration and freeze phases.
- Example mod adds at least one block, item, recipe, and event listener.

## Milestone 4 — Data-Driven Gameplay Baseline
Acceptance criteria:
- Built-in blocks, items, recipes, biomes, and loot are data-driven where practical.
- Tags/grouping support recipes, tools, worldgen, and mod compatibility.
- Built-in content registers through public registry APIs.
- Creative and survival loops are playable in a small test world.

## Milestone 5 — Mod Author Experience
Acceptance criteria:
- Mod template builds and runs from a clean checkout.
- API docs explain lifecycle, registries, events, data packs, and networking.
- Launcher/dev tools can enable, disable, and inspect mods.
- Compatibility suite runs multiple example mods together.
- Migration guide exists for every breaking API change.

## Milestone 6 — Alpha Release
Acceptance criteria:
- Players can create, save, load, and join worlds.
- Server operators can run a dedicated server with mods.
- Mod authors can publish content mods without patching game internals.
- Performance targets are documented and measured.
- Known limitations and roadmap are public.
