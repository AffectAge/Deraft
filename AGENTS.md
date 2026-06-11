# AGENTS.md — Project Guide

## Product Vision
Build an original voxel sandbox game inspired by block-building survival games, with a first-class Forge-like modding platform. The project must use original code, names, gameplay extensions, art, audio, and data formats; do not copy proprietary Minecraft assets, identifiers, networking protocols, EULA-restricted content, or implementation details.

## Repository Structure

```text
.
├── engine/                 # Reusable low-level runtime systems
│   ├── core/               # App lifecycle, ECS/services, platform abstraction
│   ├── rendering/          # Voxel meshing, shaders, lighting, cameras, UI render hooks
│   ├── world/              # Chunks, world storage, terrain generation, block access
│   ├── physics/            # Collision, raycasts, movement, fluids, interactions
│   ├── networking/         # Client/server sync, packets, replication, auth hooks
│   └── assets/             # Runtime asset loading, packs, localization, resource reloads
├── gameplay/               # Vanilla-style game content built on the engine and mod API
│   ├── blocks/             # Built-in blocks, states, drops, interactions
│   ├── items/              # Built-in items, tools, inventories, durability
│   ├── entities/           # Players, mobs, projectiles, AI, persistence
│   ├── biomes/             # Biome definitions, climate, decoration rules
│   └── crafting/           # Recipes, workstations, smelting, data-driven crafting
├── modding/                # Forge-like extension layer
│   ├── api/                # Stable public API exposed to mods
│   ├── loader/             # Mod discovery, dependency resolution, lifecycle phases
│   ├── events/             # Event bus, cancellable events, priorities
│   ├── registries/         # Dynamic registries for blocks/items/entities/biomes/etc.
│   ├── scripting/          # Optional scripting/data-pack integration
│   └── examples/           # Example mods and compatibility tests
├── tools/                  # Developer and build tools
│   ├── launcher/           # Dev launcher, game profiles, mod list management
│   ├── asset-pipeline/     # Texture/model/audio conversion and validation
│   └── dev-server/         # Local multiplayer server tooling and diagnostics
└── docs/                   # Design, milestones, architecture, contributor skills
    ├── goals/              # Roadmaps, milestones, acceptance criteria
    ├── architecture/       # ADRs, system diagrams, technical contracts
    └── skills/             # Skills matrix and learning path for contributors
```

## Goal
Deliver a playable, moddable voxel sandbox where developers can create and distribute mods that add blocks, items, recipes, entities, world generation, UI screens, commands, and server-side behavior through a stable API and loader lifecycle.

See `docs/goals/GOAL.md` for detailed milestones and acceptance criteria.

## Required Skills
Contributors should develop or use the skills listed in `docs/skills/SKILLS.md`, especially voxel engine design, data-driven gameplay, client/server architecture, API stability, and mod-loader compatibility testing.

## Cross-Cutting Engineering Rules
- Prefer original abstractions and names over direct cloning of any proprietary game internals.
- Keep engine code independent from built-in gameplay content.
- Gameplay features must use the same public modding extension points that third-party mods use whenever practical.
- All registries must support namespaced IDs such as `core:stone` and `example_mod:ruby_ore`.
- Every externally visible modding API change requires documentation and a compatibility note.
- Avoid hard-coded content in engine modules; content belongs in `gameplay/` or data packs.
- Design for deterministic dedicated-server simulation; clients may predict but servers are authoritative.
- Add tests or executable examples for loader, registry, serialization, and networking behavior.
