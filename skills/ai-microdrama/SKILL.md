---
name: ai-microdrama
description: AI短剧/AI漫剧制作工作流。Use when the user wants to create, adapt, or improve AI microdramas, AI漫剧, AI短剧, Seedance 2.0 prompts, 即梦/可灵/灵矢 video prompts, scripts, episode outlines, 分幕, 分镜, image prompts, character/prop/scene consistency sheets, camera movement prompts, dubbing/lip-sync/music plans, or an end-to-end workflow from story idea to generated images/videos and final edit.
---

# AI Microdrama

Use this skill to turn a story idea, novel excerpt, product concept, character design, or rough prompt into an AI short drama production package.

The bundled source library is in `assets/source-materials/`. Load references only as needed:

- `references/workflow.md`: end-to-end production workflow and quality gates.
- `references/prompt-patterns.md`: script, shot, image, video, and consistency prompt patterns.
- `references/production-architecture.md`: layered architecture for story, visual style, prompt libraries, generation, and post-production.
- `references/tool-links.md`: remembered tools and URLs, including the Doubao watermark-removal link.
- `references/source-index.md`: extracted index of all imported source files; search it when the concise references are not enough.
- `references/source-overview-v2.md`: human-readable overview of the updated source library and how to use each category.
- `references/source-index-v2.md`: updated extracted index for the expanded 732-file source library.
- `references/artist-index.txt`: artist/director/style reference names from the visual dictionary.
- `references/seg-terms.json`: SEG material and semantic terms for scene/prop consistency.

## Default Workflow

1. Clarify the deliverable: episode outline, full script, 分幕, 分镜, image prompts, video prompts, dubbing plan, editing plan, or full pipeline.
2. Build the story spine first: genre, audience, hook, protagonist desire, conflict, twist, episode length, and desired platform ratio.
3. For serial work, create an episode bible before shots: recurring characters, world rules, visual style, key props, continuity constraints, and cliffhanger logic.
4. Split each episode into scenes, then split scenes into shots. Keep every shot tied to a narrative beat.
5. Produce image prompts before video prompts when visual consistency matters. Lock subject, scene, lighting, composition, color, and style.
6. For image prompts, choose vocabulary from the correct layer: subject, scene, light, lens, composition, color grade, style, quality, and negative constraints.
7. Produce video prompts with time ranges, camera motion, subject motion, environment motion, transitions, sound, and reference-material syntax.
8. Add post-production notes: voice/dubbing, music, lip sync, subtitles, watermark/subtitle removal only for authorized material, and final edit order.

## Output Shape

For a complete AI漫剧 package, output in this order:

1. `项目设定`: title, genre, target platform, aspect ratio, visual style.
2. `人物/道具/场景一致性表`: stable names, appearance, costume, props, locations, and reference image needs.
3. `分集/分幕`: hook, conflict, reversal, ending or cliffhanger.
4. `分镜脚本`: shot number, duration, frame content, camera movement, action, dialogue/voiceover, sound, generation notes.
5. `图片提示词`: one prompt per key frame or shot, with consistency tokens.
6. `视频提示词`: Seedance/即梦/可灵/灵矢-ready prompts using time ranges and references.
7. `制作清单`: assets to generate, upload order, dubbing/music/lip-sync/editing steps, and QA checks.

## Consistency Rules

- Preserve character identity across all prompts: face type or non-realistic style, age, body shape, hairstyle, outfit, color palette, signature prop, and emotional range.
- Preserve scene identity: location geometry, time of day, light direction, weather, key background objects, and color temperature.
- Preserve style identity: film style, lens language, texture, color grade, render level, and aspect ratio.
- Use 360-degree or multi-angle references when available. If not available, ask for or generate front/side/back/three-quarter references before producing many shots.
- For long stories, create four key frames per sequence: opening frame, ending frame, one important middle frame, and an adjacent continuity frame before/after a major change.
- Use SEG/semantic terms for scene and prop stability when prompts need concrete environmental anchors.
- Use artist/director/style references as inspiration labels, but prefer describing transferable visual traits. Avoid direct imitation of living artists when generating final prompts.

## Seedance/Video Prompt Core

Use this structure unless the user requests another platform format:

```text
【风格】{style}，{duration}秒，{aspect_ratio}，{mood}
【主体】{character/subject locked description}
【场景】{location, light, weather, era, props}
【时间轴】
0-X秒：{shot size + camera movement}，{frame content}，{subject action}，{effect/transition}
X-Y秒：...
【声音】{music + sound effects + dialogue/voiceover}
【参考】@图片1 {purpose}，@视频1 {camera/action reference}，@音频1 {voice/music reference}
【一致性】保持人物、服装、道具、场景、色调、镜头语言一致
```

## Important Constraints

- Do not claim a tool can access private Feishu/wiki/course links unless the content has actually been downloaded or provided locally.
- For watermark/subtitle removal tools, use them only on material the user owns or is authorized to edit.
- Seedance source notes mention limits such as up to 12 reference files, images/videos/audio as references, and avoiding realistic real-person face material; check current platform limits if the exact limit matters.
- If the user asks to "丰富 skill", add concise reusable knowledge to `references/`, keep raw source files in `assets/source-materials/`, and validate the skill after edits.
