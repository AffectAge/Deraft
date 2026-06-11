# Skills Matrix

## Engine Skills
- Voxel data structures: chunks, sections, palettes, compression, coordinate transforms.
- Meshing and rendering: greedy meshing, occlusion, texture atlases/arrays, lighting, shader debugging.
- World persistence: versioned save formats, migrations, region files, async IO.
- Physics: AABB collision, raycasts, movement integration, fluids and climbable materials.
- Networking: authoritative servers, packet codecs, replication, prediction, rollback-aware design.

## Gameplay Skills
- Data-driven content: schemas, validation, tags, loot tables, recipes, localization.
- Entity systems: components, AI, spawn rules, persistence, animation hooks.
- Progression design: resource loops, crafting chains, survival balance, creative tooling.
- Accessibility and UX: input remapping, readable UI, feedback, onboarding.

## Modding Skills
- API design: small stable interfaces, semantic versioning, deprecation policy.
- Loader design: manifests, dependency graphs, side separation, lifecycle phases.
- Event systems: listener ordering, cancellable events, result events, thread-safety.
- Registries: namespaced IDs, deferred registration, remapping, missing-content recovery.
- Compatibility: example mods, integration tests, diagnostics, migration guides.
- Security: sandboxing, trust boundaries, server/client separation, safe scripting.

## Tools and Operations Skills
- Build automation and CI.
- CLI and launcher UX.
- Asset pipelines for textures, models, audio, localization, and packs.
- Profiling CPU, GPU, memory, startup, IO, and network traffic.
- Crash report symbolication, log analysis, and issue triage.

## Documentation Skills
- Architecture decision records.
- Public API references with examples.
- Milestone planning and acceptance criteria.
- Contributor onboarding guides.
- Mod-author tutorials and troubleshooting pages.

## Recommended Learning Path
1. Implement namespaced IDs and registries.
2. Build chunk storage and block state access.
3. Render a small chunk with placeholder original textures.
4. Add save/load and deterministic server ticks.
5. Introduce mod manifests, lifecycle phases, and deferred registration.
6. Convert built-in blocks/items to public registry usage.
7. Add example mods and compatibility tests.
8. Document APIs and migration policies before alpha release.
