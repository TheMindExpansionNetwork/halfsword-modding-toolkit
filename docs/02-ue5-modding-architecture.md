# Unreal Engine 5 Modding Architecture (for Packaged Games)

This document explores the underlying architecture that makes modding possible in cooked Unreal Engine games like Half Sword. The goal is understanding, not memorization.

## Core Idea: Content Mounting & Override

Unreal Engine loads content from multiple sources at runtime. The order in which these sources are mounted determines which version of an asset wins.

**Key Questions:**
- Why does placing custom content in a `~mods` folder often give it higher priority than the base game?
- What does this tell us about how the engine resolves asset references?
- If two assets share the exact same object path, which one is used and why does this matter for weapon replacement?

## Asset Identity in Cooked Games

In a cooked game, assets are referenced by their cooked package paths. Mods usually work by providing assets at the same (or compatible) paths.

**Questions to Consider:**
- What are the implications of overriding a weapon’s Static Mesh, Physics Asset, and Materials versus creating an entirely new Blueprint?
- How much of a weapon’s behavior is defined in its Blueprint versus its data assets (Physics Asset, Collision settings, etc.)?
- When is simple asset replacement enough, and when do we need to extend or replace logic?

## Collision and Physics in the Architecture

Half Sword relies heavily on physics simulation for melee combat. This makes the Physics Asset and collision setup especially important.

**Deep Questions:**
- Why are simple convex collision shapes often preferred for swung weapons over highly detailed meshes?
- How do Center of Mass and mass distribution affect the "feel" of a weapon during swings and impacts?
- What happens to physics behavior when you override only the mesh and physics asset while keeping the original weapon’s Blueprint?

## Cooking, Pak, and IoStore

Cooking transforms editor assets into optimized runtime data. The resulting `.pak` (and IoStore) files are what the game actually loads.

**Important Questions:**
- What is lost or optimized away during cooking that a modder should be aware of?
- Why does folder structure inside the pak matter so much?
- How does IoStore change the modding workflow compared to traditional paks?
- What makes a mod "load cleanly" versus causing conflicts or crashes?

## Runtime Extension Points

Some mods only replace assets. Others need to influence behavior at runtime.

**Questions:**
- What extension points does Unreal expose for modders without source access?
- When might tools like UE4SS become valuable, and what problems do they solve?
- How does the architecture support (or limit) adding new weapons, effects, or mechanics?

## Implications for Our Work

Understanding this architecture helps us make better decisions when building the frying pan and future mods:

- We can focus our energy on what the architecture makes easy (mesh + physics + material overrides).
- We can anticipate where things might break (path mismatches, cooking settings, collision complexity).
- We can design our workflow to work *with* the engine rather than against it.

---

*Architecture is not just technical detail. It is the hidden structure that determines what is possible.*