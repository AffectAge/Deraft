# AGENTS.md — Engine

## Scope
Applies to `engine/` and all subdirectories.

## Mission
Create reusable, content-agnostic runtime systems for a voxel sandbox: lifecycle, rendering, world storage, physics, networking, and assets.

## Folder Responsibilities
- `core/`: application lifecycle, dependency injection/service registry, job scheduling, platform abstraction, logging, configuration.
- `rendering/`: chunk meshing, render graph, shader/material abstractions, lighting, camera systems, debug visualization.
- `world/`: chunk coordinates, block access interfaces, terrain storage, serialization, generation pipelines, save formats.
- `physics/`: broadphase/narrowphase collision, block collision shapes, raycasts, movement helpers, fluid interactions.
- `networking/`: protocol abstraction, packet codecs, replication, login handshake hooks, server-authoritative state sync.
- `assets/`: resource packs, asset reload lifecycle, localization, texture/model/audio loading, validation.

## Goal
Provide stable low-level services that `gameplay/` and `modding/` can depend on without introducing gameplay-specific concepts into engine internals.

## Skills Needed
- Real-time rendering and GPU profiling.
- Chunked voxel meshing and light propagation.
- Deterministic simulation and fixed-tick loops.
- Binary serialization and versioned save migration.
- Client/server networking and packet compatibility.
- Performance profiling, memory layout, and cache-aware data structures.

## Rules
- Do not import from `gameplay/`; engine modules must be content-agnostic.
- Do not expose proprietary protocol or asset assumptions.
- Public interfaces must be documented before gameplay or modding uses them.
- Prefer data-oriented designs for hot paths such as chunk meshing, lighting, and collision.
- Networking code must treat the dedicated server as authoritative.
