# AGENTS.md — Gameplay

## Scope
Applies to `gameplay/` and all subdirectories.

## Mission
Implement the built-in game experience using the engine and the public modding APIs, proving that third-party mods can extend the same systems.

## Folder Responsibilities
- `blocks/`: built-in block definitions, block states, drops, interactions, hardness, collision behavior.
- `items/`: tools, consumables, equipment, inventory behavior, durability, item use actions.
- `entities/`: player controller, creatures, projectiles, AI behaviors, persistence and spawn rules.
- `biomes/`: climate model, terrain decoration, biome-specific spawn and resource rules.
- `crafting/`: recipes, recipe serializers, crafting stations, smelting/cooking, data-driven unlocks.

## Goal
Ship a coherent survival/creative sandbox baseline that is fun by itself while remaining fully extendable by mods.

## Skills Needed
- Data-driven gameplay design.
- Entity-component or behavior-tree patterns.
- Balancing progression, resources, crafting, and survival loops.
- Content validation and automated gameplay regression tests.
- Designing APIs from the perspective of mod authors.

## Rules
- Built-in content should register through `modding/registries` rather than hidden engine hooks.
- Keep content definitions data-driven where possible.
- Avoid names, textures, models, sounds, recipes, and lore that copy proprietary games directly.
- Every built-in feature should have an extension point or a documented reason why it does not.
