---
name: anime-to-life
description: Transforms anime, art, or 3D character images into photorealistic cosplay photos.
version: 1.0.0
---

# Anime to Life

## Capability
Transforms an uploaded anime, art, or 3D rendering image into a photorealistic photograph featuring the same character in the same background, rendered as a real person cosplayer.

## Triggers
- User uploads an image and asks to "turn this into a real person".
- "Make this realistic".
- "Anime to real life".
- "Cosplay version of this character".

## Instructions
1.  **Analyze the User's Request and Image**:
    - Identify the character in the uploaded image. Search if necessary to determine ethnicity (Russian or Japanese default).
    - Note the character's physique, posture, expression, pose, position, props, eye color, and clothing.
    - Note the camera angle and framing.
    - Note the background details.

2.  **Construct the Image Generation Prompt**:
    - **Subject**: "A photorealistic photo of a [Russian/Japanese] cosplayer cosplaying as [Character Name] from [Source Material]..."
    - **Details**: "...having the same physique, posture, expression, pose, position, props, eye color, and clothing as the original character."
    - **Face**: "Facial features should retain an anime-inspired aesthetic—like those of a cosplayer idol with refined makeup and an elegant appearance."
    - **Angle**: "Match the angle and framing of the uploaded image."
    - **Background**: "Background matching the original image but rendered in a realistic style."
    - **Style**: "Photorealistic, high quality, 8k, realistic texture, realistic lighting."

3.  **Generate the Image**:
    - Use the `generate_image` tool.
    - Pass the constructed prompt.
    - Pass the user's uploaded image path in `ImagePaths` to use as a reference/control.

## Tools / Commands
- `generate_image`: To generate the photorealistic image.

## Examples
User: "Turn this anime picture into a real photo." (User attaches `character.png`)
Action:
1. Identify character (e.g., Hatsune Miku).
2. Determine ethnicity (Japanese).
3. Construct prompt: "A photorealistic photo of a Japanese cosplayer cosplaying as Hatsune Miku, same physique, posture, teal twin-tails, school uniform, holding a leek, dynamic pose, happy expression. Anime-inspired aesthetic face, refined makeup. Matching camera angle and framing. Detailed realistic stage background."
4. Call `generate_image(Prompt="...", ImagePaths=["/path/to/character.png"], ImageName="real_miku")`
