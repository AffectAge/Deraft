# AGENTS.md — Modding Platform

## Scope
Applies to `modding/` and all subdirectories.

## Mission
Create a Forge-like modding platform with mod discovery, dependency resolution, lifecycle events, registries, event bus, data/resource packs, examples, and compatibility tooling.

## Folder Responsibilities
- `api/`: stable interfaces, annotations/metadata, semantic versioning policy, public documentation.
- `loader/`: mod manifest parsing, dependency graph, class/module isolation, lifecycle phases, error reporting.
- `events/`: event bus, listener priorities, cancellable events, result-bearing events, server/client side dispatch.
- `registries/`: namespaced registries, deferred registration, freeze phases, remapping, missing-entry recovery.
- `scripting/`: optional scripting hooks, data-pack integration, safe sandbox boundaries.
- `examples/`: sample mods that add content and exercise compatibility scenarios.

## Goal
Allow mod authors to add blocks, items, entities, biomes, recipes, commands, world generation, UI, and server behavior without patching core game code.

## Skills Needed
- Public API design and semantic versioning.
- Plugin/module loading and dependency resolution.
- Event-driven architecture and lifecycle management.
- Sandboxing, security boundaries, and crash isolation.
- Compatibility testing across multiple independently developed mods.
- Documentation and developer-experience design.

## Forge-Like Design Targets
- `mod.json` manifest with ID, name, version, dependencies, side, entry points, and metadata.
- Lifecycle phases: discover, construct, common setup, client setup, server setup, registry freeze, world load, runtime.
- Deferred registration so mods can declare content before registries freeze.
- Event bus with priorities and cancellable events.
- Data/resource pack override model for recipes, loot, tags, models, textures, localization, and worldgen.
- Dedicated-server compatibility and explicit client-only boundaries.

## Rules
- Backward compatibility matters: breaking API changes require migration notes.
- Mods must use namespaced IDs; reject ambiguous global names.
- Loader errors must explain the failing mod, dependency, phase, and suggested fix.
- Example mods are part of the compatibility suite and should remain simple and readable.
