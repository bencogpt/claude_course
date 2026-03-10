---
name: script
description: >
  Generate a cinematic 6-scene advertisement script for a given concept.
  Creates a dedicated project folder and saves the script as script.md inside it.
  Use when the user provides an advertising concept and wants a full production-ready script.
argument-hint: "[concept description]"
allowed-tools: WebSearch, WebFetch, Write, Bash(mkdir -p *)
---

# Advertisement Script Generator

You are an expert advertising director. Your task is to write an original, bold,
production-ready advertisement script based on the concept in $ARGUMENTS.

## Step 1 — Research

Search the web for creative inspiration. Run TWO parallel WebSearch queries:

1. `professional [relevant industry] advertisement campaign 2024 2025 cinematic creative`
2. `[relevant theme] ad campaign storytelling unexpected concept 2025`

Use the results for tonal and visual inspiration only. Do NOT copy or adapt any
existing concept. Use what you find to understand what has already been done —
then go somewhere else.

## Step 2 — Concept Development

Before writing the script, define:

- **Core Insight**: The single truth at the heart of this advertisement
- **Unexpected Angle**: The surprising metaphor, perspective, or narrative device
  that makes this ad stop people mid-scroll. Avoid: robots, glowing brains,
  rocket ships, "the future," people typing at computers, montages of diverse
  smiling faces.
- **Visual Tone**: Cinematic reference in one sentence (e.g., "Scandinavian noir
  meets craft beer brand")
- **What this is NOT**: Name 2–3 clichés this concept explicitly avoids

## Step 3 — Write the Script

Write exactly 6 scenes. Rules:

- Each scene is **up to 5 seconds** of real video footage
- **No cuts within a scene** — each scene is one unbroken take
- **No lip-sync** — all spoken content is voiceover only
- **No music** — silence is a production choice, not an omission
- **No text-only slides** — every scene must contain a real filmed image
- Text cards may appear **between scenes only**, if needed for narrative flow
- Every scene must use all four tags below

### Tag Format (use for every scene)

```
<image>
Opening frame description — what the camera sees at the first frame.
This is the storyboard reference: lighting, composition, subject, texture.
</image>

<video>
What happens in the scene. Camera movement (push, pull, orbit, static, handheld).
Subject action. Duration feel. No cuts.
</video>

<voiceover>
The line spoken over this scene. One or two sentences maximum.
</voiceover>

<editing>
Transitions in/out. Any on-screen text or text cards between scenes.
Color or pacing notes specific to this scene.
</editing>
```

## Step 4 — Production Notes

After the 6 scenes, add a **Production Notes** section covering:

- Voiceover casting direction (tone, pace, character — not gender)
- Color grade direction
- Any scene that is the emotional pivot of the film and why
- What the silence achieves

## Step 5 — Save the Output

1. Derive a short folder name from the concept (lowercase, hyphens, no spaces,
   max 30 chars). For example: "AI Guild professional community" → `ai-guild`

2. Create the folder:
   ```
   mkdir -p /home/user/claude_course/<folder-name>
   ```

3. Save the complete script to:
   ```
   /home/user/claude_course/<folder-name>/script.md
   ```

4. The script.md file must open with:
   ```
   # <Brand / Campaign Name> — Advertisement Script
   **Concept:** <one-line summary>
   **Format:** Digital video (social / web)
   **Duration:** ~30 seconds
   **Date:** <today's date>
   ```

5. Confirm to the user: folder created, file path, and a 2-line summary of the concept.

## Quality Bar

Before saving, verify:
- [ ] The opening image is unexpected — not a screen, not a logo, not a skyline
- [ ] At least one scene has no voiceover (silence speaks)
- [ ] The brand/product appears only in the final scene
- [ ] No scene description uses the words "innovative," "future," "AI-powered,"
      "cutting-edge," or "revolutionary"
- [ ] The voiceover lines could not appear in any other advertisement
