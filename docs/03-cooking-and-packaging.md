# Cooking & Packaging Deep Dive

Cooking is where your creative work becomes something the game can actually load. This document explores the cooking and packaging process through questions so you can build real intuition.

## What Cooking Actually Does

When you cook content, Unreal Engine processes your assets, compiles shaders, optimizes data, and packages everything into efficient runtime formats (`.pak` and often IoStore `.utoc`/`.ucas`).

**Core Questions:**
- What gets optimized or stripped during cooking that might affect your mod?
- Why can’t you usually just copy `.uasset` files from the editor into a cooked game?
- How does cooking affect collision, physics, materials, and references?

## Project Setup for Mod Cooking

Successful mod cooking usually requires your project to understand the game’s content structure.

**Questions to Explore:**
- Why is it powerful to create a UE project whose folder structure mirrors the paths inside Half Sword?
- What problems arise when your mod assets live at different paths than the game expects?
- How much of the original game’s Content folder do you need to replicate?

## What to Cook

You don’t always need to cook everything.

**Key Questions:**
- What are the advantages of cooking only the specific assets for your frying pan (mesh, materials, physics) versus cooking a broader set?
- How does "Cook only modified content" or similar options affect your iteration speed?
- What files are typically generated after cooking (`.pak`, `.utoc`, `.ucas`, `.sig`)?

## Output & Placement

After cooking, the files need to end up in the right place for the game and mod manager to find them.

**Important Considerations:**
- Why does the `Content/Paks/~mods` (or similar) location often work for custom content?
- What happens if your pak has the wrong internal folder structure?
- How can you verify that your mod actually loaded?

## Iteration & Safety

Cooking is part of a fast feedback loop.

**Questions:**
- What is a safe, low-risk way to test a newly cooked mod?
- How do you quickly roll back if collision feels wrong or the weapon doesn’t appear?
- What signs indicate that your pak loaded successfully versus being ignored or conflicting?

## Connection to Our Pipeline

Cooking sits near the end of the pipeline but influences earlier decisions:
- Good Blender export and import settings reduce cooking problems.
- Clean collision and physics setup pays off during cooking and testing.
- Understanding paths early prevents painful packaging issues later.

---

*The goal of understanding cooking is not to become a packaging expert. It is to remove friction between your ideas and the game.*