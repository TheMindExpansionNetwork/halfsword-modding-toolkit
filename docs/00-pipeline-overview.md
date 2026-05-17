# Pipeline Overview: From Idea to In-Game Mod

This document is not a rigid checklist. It is a map of the major phases involved in creating original mods for Half Sword using Unreal Engine 5.4.4. Use it to orient yourself and generate better questions.

## Why a Pipeline Matters

Creating a good mod (especially one with correct physics and feel) involves many interconnected steps. Understanding the full flow helps you:
- Know where you are when something breaks
- Decide what to learn next
- Build intuition that transfers to future mods

## High-Level Phases

### 1. Setup & Toolchain
- What tools and versions do you actually need?
- Why does matching the game’s Unreal Engine version (5.4.4) matter?
- What is the minimal set of tools versus the "nice to have" set?

### 2. Research & Asset Inspection
- How do you explore the game’s existing weapons and props?
- What questions should you ask when looking at a mace or hammer blueprint?
- How does FModel help you understand paths, sockets, and physics?

### 3. Asset Creation (Blender)
- Modeling, topology, and UVs for game weapons
- Proper pivot/grip placement
- Export settings for clean FBX import
- Creating simple collision meshes

### 4. Physics & Feel Design
- What makes a weapon feel good in Half Sword’s physics system?
- Center of mass, mass values, collision response
- How to test "head-heavy" vs balanced feel

### 5. Unreal Engine Import & Setup
- Creating or using a mod project that mirrors game paths
- Importing FBX with correct settings
- Assigning materials and physics assets
- Reusing or extending existing weapon behavior

### 6. Cooking & Packaging
- Cooking only what you need
- Understanding the output files (.pak, .utoc, .ucas)
- Placing files in the correct location for the game and mod manager

### 7. Testing & Iteration
- Safe ways to load and test your mod
- Using FleX Mod Manager effectively
- Capturing loadouts and rolling back changes
- Debugging common issues (missing assets, bad collision, wrong grip, etc.)

### 8. Documentation & Sharing
- How to document your process so others (and future you) can learn
- What makes a good example or guide?

## How to Use This Document

Treat each phase as a prompt for deeper exploration. Ask:

- What do I not yet understand about this phase?
- What would happen if I skipped or changed something here?
- How does this phase connect to the ones before and after it?

The goal is not speed. The goal is building real capability.