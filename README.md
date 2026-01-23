# Nano Banana Skills

This project is a collection of AI agent skills designed for **Nano Banana**, focusing on advanced image generation capabilities.

## How to use this agent skills in Gemini App

1. Create a `git repo` with your skills.
2. Create a `gem` in the Gemini app and add the skills repo as `Knowledge`.
3. **Say the name** of the skill to use it.

## Project Structure

- **`skills/`**: This directory contains the individual agent skills. Each skill is a self-contained folder with its own instructions and scripts.
- **`GEMINI.md`**: The comprehensive guide for creating and structuring new skills for this project.

## Available Skills

| Name | Description |
| :--- | :--- |
| [anime-to-life](skills/anime-to-life/SKILL.md) | Transforms anime, art, or 3D rendering images into photorealistic cosplay-style photographs using a specific JSON-based prompt structure. |
| [character-reference-sheet](skills/character-reference-sheet/SKILL.md) | Generates character reference sheets with research-backed details. Supports split-screen (default), 2x2, and 3x3 layouts with mandatory front/back views and dynamic poses. |
| [photo-restoration](skills/photo-restoration/SKILL.md) | Restores vintage and blurry photos to high-definition 8k images while preserving identity. |
| [figure-to-life](skills/figure-to-life/SKILL.md) | Converts figure photos to photorealistic human cosplayer images using a strict JSON-based reasoning mandate. |
| [real-mecha](skills/real-mecha/SKILL.md) | Converts 2D/anime mecha art into photorealistic 3D/real-world visualizations with high-fidelity material textures. |

## Contributing

To create a new skill for this project, please refer to the [GEMINI.md](GEMINI.md) guide. It outlines the required directory structure, `SKILL.md` format, and drafting rules.
