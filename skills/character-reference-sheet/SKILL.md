---
name: character-reference-sheet
description: Generates a 1:1 split-screen (front/back) character reference sheet, mirroring facial, physical, and costume details from an uploaded image.
version: 1.0.0
---

# Character Reference Sheet

## Capability
Analyzes an attached character image to perform deep feature extraction (facial physiognomy, physical attributes, costume details) and generates a split-screen image containing two full-body views (Front and Back) on a simple color background, maintaining the exact visual style of the source.

## Triggers
- "Create a character reference sheet."
- "Generate a front and back view of this character."
- "Make a split-screen character sheet."
- "Analyze this character and create a reference image."

## Instructions
1.  **Analyze the User's Request and Image**:
    - **Facial Physiognomy**: Identify exact eye color/shape, nose structure, jawline, and facial proportions.
    - **Physical Attributes**: Identify hair texture, hair color, skin tone, and body type.
    - **Costume Details**: Identify specific texture, material properties, and color palette of the clothing.

2.  **Construct the Image Generation Prompt**:
    - **Subject**: "A split-screen character reference sheet featuring [Character Description]..."
    - **Views**: "...showing two full-body views: Left Side is Front view, Right Side is Back view."
    - **Background**: "...on a simple color background."
    - **Details**: "Exact mirror of facial features (eyes, nose, jawline), physical attributes (hair, skin, body), and costume details (texture, material, colors) from the source."
    - **Visual Constraints**: "Aspect Ratio 1:1. Style Fidelity: Retain the exact visual style, rendering technique, and lighting quality of the source image."

3.  **Generate the Image**:
    - Use the image generation tool.
    - Pass the constructed prompt.
    - Pass the user's uploaded image path in the reference image parameter to use as a reference.

## Tools / Commands
- Image generation tool: To generate the reference sheet.

## Examples
User: "Create a reference sheet for this character." (User attaches `[image]`)
Action:
1. Analyze `[image]`: "Male, spiky blue hair, scar on left cheek, silver armor with gold trim..."
2. Construct Prompt: "A split-screen character reference sheet featuring a male warrior with spiky blue hair and a scar on his left cheek, wearing silver armor with gold trim. Left side: Front view. Right side: Back view. Simple color background. High fidelity to source style and details."
3. Call the image generation tool with the constructed prompt and image paths.
