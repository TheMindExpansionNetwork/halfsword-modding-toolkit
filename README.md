# Half Sword Modding Toolkit

**A living, question-driven space for building your own mods in Unreal Engine.**

We are not here to simply follow instructions. We are here to develop real understanding — so we can create original, high-quality mods for *Half Sword* (and beyond) with intention and craft.

This repository began from a conversation about crafting a custom **frying pan** weapon and grew into a broader vision: a practical toolkit that helps modders move from "I want to add something cool" to "I understand how to conceive, build, tune, package, and iterate on almost anything."

---

## The Starting Vision

- Start with a concrete first project: a properly weighted, collision-rich frying pan that feels fun and believable in Half Sword's physics-based combat.
- Build upon excellent existing community resources while creating our own clear explanations and workflows.
- Focus on **original asset creation** (Blender → FBX) rather than just editing existing game files.
- Document not just *how*, but the *why* behind collision, physics, grip, materials, and packaging so the knowledge transfers to future mods.

---

## First Concrete Goal: The Frying Pan Mod

A custom weapon asset that can be packaged as a `.pak` mod and used with FleX Mod Manager (or manually).

Key requirements we identified:

- Low-to-mid poly FBX model (pan head + handle) scaled appropriately for a short blunt weapon
- Proper pivot/grip point at the handle
- Simple **convex collision** meshes (avoid overly complex collision)
- Basic materials (dark metal, worn edges, handle)
- Physics data: mass, center of mass, head-heavy feel, blunt impact behavior
- Optional: metallic impact audio cues
- Packaged correctly for Half Sword's UE 5.4.4 Early Access structure

---

## Key Research & Context

- **Engine Version**: Half Sword Early Access currently uses **Unreal Engine 5.4.4**
- **Mod Installation**: Custom content is typically placed in `Content\Paks\~mods` (as `.pak` / `.utoc` / `.ucas` files)
- **Existing Excellent Resource**: [massclown/HalfSwordModdingResources](https://github.com/massclown/HalfSwordModdingResources) — highly recommended starting point for inspecting assets, understanding object hierarchy, and save editing
- **Community**: Active modding scene on Nexus Mods. Developers have expressed support for good mods
- **Core Tools** commonly used: FModel (asset inspection), Unreal Editor 5.4.4, Blender (modeling & export), UE4SS (when runtime logic is needed)

---

## What This Toolkit Aims to Explore

Instead of a rigid tutorial, we are building a collection of guiding questions, workflows, and examples that help you develop intuition:

- How do I model a weapon in Blender so it imports cleanly and feels right in-game?
- What makes good collision and physics for melee combat?
- How do I safely package and test changes?
- How can I reuse existing weapon behavior while swapping in my own visuals and feel?
- What questions should I ask before adding audio, icons, or more complex features?

---

## Proposed Structure (Open to Evolution)

```
halfsword-modding-toolkit/
├── README.md
├── docs/
│   ├── 01-foundations.md          # Mindset, key questions, safety
│   ├── 02-blender-asset-pipeline.md
│   ├── 03-collision-physics.md
│   ├── 04-unreal-import-setup.md
│   ├── 05-packaging-testing.md
├── examples/
│   └── frying-pan/               # Our first worked example
├── resources/
│   └── links.md                   # Curated community resources
└── CONTRIBUTING.md
```

---

## How to Contribute

This is meant to be a collaborative, living toolkit. The best contributions often come in the form of better questions, clearer explanations, or new examples that help others develop real understanding.

Feel free to open issues or pull requests with ideas.

---

*Let's build understanding, not just mods.*