# AI漫剧生产架构

Use this architecture when turning the source library into repeatable work. Keep the core pipeline separate from prompt-resource libraries.

## Layer 1: Story Engine

Purpose: decide what happens and why the viewer keeps watching.

- Inputs: idea, novel excerpt, product concept, genre, audience, platform.
- Outputs: logline, world rules, character desire, conflict, twist, episode outline, cliffhanger.
- Checks: each episode has a hook, emotional escalation, reversal, and a clear next-episode pull.

## Layer 2: Continuity Bible

Purpose: lock identity before generating images or video.

- Character card: name, age, body type, face style, hair, clothing, color palette, signature prop, personality, expression range.
- Prop card: shape, material, color, scale, usage, symbolic function.
- Scene card: location geometry, era, time of day, weather, light direction, key background objects, color temperature.
- For major characters or reusable environments, create front, side, back, and three-quarter references.

## Layer 3: Visual Prompt Vocabulary

Purpose: choose precise image-language ingredients.

Use the updated source library as a vocabulary reservoir:

- SD/MJ prompt packs: composition, lens, lighting, quality, texture, color, subject, costume, negative prompt terms.
- SEG semantic terms: concrete environment and prop anchors such as roads, bridges, rooms, furniture, vehicles, signs, lamps, water, rock, plants.
- Artist/style dictionary: inspiration and visual direction names. Translate names into traits whenever possible: line quality, palette, composition, era, texture, mood.
- Element Codex / keyword packs: fantasy, material, creature, environment, and effect words for richer worldbuilding.

Prompt layer order:

```text
subject -> identity details -> action -> scene -> light -> camera/lens -> composition -> color/style -> quality -> consistency -> negative constraints
```

## Layer 4: Image Generation

Purpose: create stable key frames and references.

- Generate character sheets before story shots.
- Generate environment references before multi-shot scenes.
- Generate key frames in this order: opening frame, ending frame, middle action frame, continuity bridge frame.
- For each image prompt, repeat essential identity and scene tokens. Do not rely on memory from earlier prompts.

## Layer 5: Video Generation

Purpose: turn key frames into short controllable shots.

- Generate by shot, not by whole episode.
- Each shot prompt needs duration, starting frame, ending state, camera movement, subject movement, environmental movement, transition, sound notes.
- Use the time-axis pattern for Seedance-style prompts.
- Keep video references short and explicit: `@图片1 as character reference`, `@图片2 as scene reference`, `@视频1 as camera/action reference`, `@音频1 as voice/music reference`.

## Layer 6: Audio And Lip Sync

Purpose: make scenes feel acted, not only animated.

- Split audio into narration, dialogue, ambient sound, action sound effects, and BGM.
- Mouth-sync shots should be short and have simple face/camera motion.
- Emotional beats should specify voice tone, pause, breath, and emphasis.

## Layer 7: Editing And QA

Purpose: make generated clips into a coherent short drama.

- Edit order follows the storyboard, not the generation order.
- Check visual continuity: same character, same scene geometry, same light direction, same color grade.
- Check motion continuity: action starts where previous shot ended.
- Check story clarity: every shot should add information, tension, emotion, or payoff.
- Authorized cleanup tools may remove subtitles or watermarks from user-owned material only.

## Retrieval Guide

- Need general AI漫剧 workflow: read `workflow.md`.
- Need prompt formulas: read `prompt-patterns.md`.
- Need resource inventory: search `source-index-v2.md`.
- Need style names: read `artist-index.txt`, then convert names into visual traits.
- Need scene/prop anchors: read `seg-terms.json`.
