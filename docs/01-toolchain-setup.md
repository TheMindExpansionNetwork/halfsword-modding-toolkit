# Toolchain & Installation Exploration

This is not a list of things to install blindly. It is an invitation to understand **why** certain tools matter and what questions you should ask before setting up your environment.

## Core Principle

For Half Sword modding (UE 5.4.4), your tools should help you:
- Inspect the game’s existing assets
- Create original content (models, collision, physics)
- Import and configure assets correctly in Unreal
- Package them reliably
- Test safely and iterate quickly

## Key Questions About Your Toolchain

### Unreal Engine
- Why is it important to install the **exact same engine version** the game uses (currently 5.4.4)?
- What problems can occur if you use a newer or older editor?
- Do you need the full editor, or are there lighter ways to work?

### Blender
- What version of Blender offers the most reliable FBX export for Unreal?
- What export settings are most critical for weapons (pivot, scale, normals, etc.)?
- How can you set up Blender so your models are "UE-ready" from the start?

### Asset Inspection Tools
- Why is FModel (or similar) almost essential for understanding paths, sockets, physics assets, and Blueprints?
- What specific things should you look for when inspecting a blunt weapon?

### Mod Management & Testing
- How does FleX Mod Manager (or similar tools) fit into your workflow?
- What other tools help with save editing, quick testing, or rolling back changes?

### Optional but Powerful
- When might UE4SS become useful?
- Do you need Visual Studio / C++ toolchain, or can you stay asset-only for now?
- How does Git fit into documenting and versioning your mod work?

## Suggested Starting Mindset

Instead of installing everything at once, consider:

1. What is the smallest set of tools that lets me create and test a simple mesh override?
2. What tool would give me the biggest insight right now (e.g., being able to see the game’s weapon Blueprints)?
3. What can I learn by inspecting before I start modeling?

## Next Steps for You

- Which tool are you most curious (or confused) about?
- What questions do you have about versions or installation order?
- Would you like to explore the installation and configuration of one specific tool in more depth through questions?

The best toolchain is the one you understand, not just the one you have installed.