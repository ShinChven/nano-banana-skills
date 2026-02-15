---
name: anime-to-life
description: Transforms anime, art, or 3D rendering images into photorealistic cosplay-style photographs.
version: 1.1.0
---

# Anime to Life

## Capability
Transforms an uploaded anime, art, or 3D rendering image into a photorealistic photograph. It generates a real person (cosplayer) matching the character's features, pose, and background details in a realistic style.

## Triggers
- User uploads an anime, art, or 3D image and asks to "bring it to life", "make it real", "realistic version", or "generate a photo of this".

## Instructions
1.  **Analyze and Generate**: Perform a **one-to-one structural transformation** of the input image. The goal is to keep the composition, characters, and objects in their exact original positions while replacing every pixel with high-fidelity, photorealistic rendering.
    -   **Subject**: Transform the character into a **real human cosplayer**. They must have a pretty appearance, delicate idol-style makeup, and anime-inspired facial features (while remaining a real human). **Ethnicity must match the character: use a beautiful Japanese cosplayer for Asian characters and a beautiful Russian cosplayer for Western characters.**
    -   **Face & Feature Mapping**: Map the **face shape, jawline, eye shape, and eye color** with extreme precision. The generated face must be a 100% accurate photorealistic interpretation of the original character's unique facial structure. They must possess the **identical** physique, clothing, hair, and props as the character in the input image.
    -   **Action & Composition**: Maintain the **exact same** pose, position, framing, and facial expression. The character's silhouette and placement on the canvas must be identical to the original.
    -   **Environment**: Re-render the original background in a realistic style, ensuring it matches the source image's layout and mood perfectly.
    -   **Style (Pure Realism)**: The output must be a **photorealistic photograph**. It must look like a real human was photographed in a real set. Use high-fidelity 8k textures, realistic skin pores, and authentic fabric physics.
    -   **Negative Constraints**: Strictly forbid any traces of art, anime, CGI, 3D rendering, drawing, or painting. The result must NOT be "stylized"; it must be "real".
    -   **Reference**: Use the original image as a strict structural reference for the generation tool.

## Tools / Commands
- Image generation tool: specific inputs: `Prompt="..."`, `Reference Images=["..."]`

## Examples
User: [Uploads image of detailed anime girl] "Bring this to life."
Action:
1. Agent analyzes the image for character traits, pose, and background.
2. Agent calls the image generation tool to generate a photorealistic photograph following the "Analyze and Generate" logic, using the original image as a reference.
