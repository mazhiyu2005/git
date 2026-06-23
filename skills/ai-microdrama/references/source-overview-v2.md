# 更新资料总览 v2

The source library now contains 732 files, copied into `assets/source-materials/` and indexed under `references/source-index-v2.md`.

## 文件组成

- 408 JPG: mostly artist/director/style visual reference images.
- 148 SKM: SEG material and semantic reference files for environments, outdoor scenes, indoor furniture, and prop anchors.
- 57 XLSX and 33 XLS: Stable Diffusion, Midjourney, keyword, style, and prompt dictionaries.
- 23 TXT, 18 DOCX, 3 DOC: prompt templates, script and storyboard methods, character/prop/scene extraction, copywriting notes.
- 19 PDF: Stable Diffusion guidebooks, Midjourney prompt books, artist dictionary, Seedance tutorial, lens/person/costume prompt books.
- Archives: ZIP/RAR/7z split files are preserved as source assets but not fully unpacked in this pass.

## 新增知识模块

### Stable Diffusion / MJ 词库层

Use these as vocabulary, not as final prompts by themselves:

- lens/camera terms
- character terms
- costume terms
- scene and environment terms
- material and texture terms
- quality terms
- negative prompt terms
- bilingual prompt dictionaries

### SEG 语义层

Use `seg-terms.json` to stabilize scenes and props. The current categories include:

- 建筑环境: land, tower, wall, cabin, path, dust, mountains, rocks, buildings, roads, water, desert, river, ocean, lake, waterfall, fields, flowers, grass.
- 室外场景: traffic lights, sidewalks, buses, signs, animals, trucks, stairs, branding, fountains, boats, tents, flags, poles, benches, fences, rails, cars, pools, docks, lamps, planes.
- 室内家具: books, shelves, desks, cabinets, light sources, refrigerator, stools, toilets, kitchen islands, chandeliers, coffee tables, cushions, screens, beds, seats, microwaves, pillows, sofas, sinks, washing machines, bathtubs, posters, mirrors, counters.

When a scene is unstable, add 3-8 concrete SEG anchors to the prompt rather than only saying "same room" or "same city".

### 艺术家/风格参考层

The visual dictionary contains 306 unique names. Use `artist-index.txt` for lookup.

Best practice:

- Use the artist list for direction-finding and internal vocabulary.
- Convert names into concrete visual traits before final output: palette, line weight, composition, texture, subject treatment, lighting, era, mood.
- Avoid final prompts that directly imitate living artists; use "inspired by" only when appropriate and prefer descriptive traits.

### ComfyUI / 动态提示词层

ComfyUI and dynamic prompt resources belong to the generation-support layer:

- style presets
- prompt randomization patterns
- reusable keyword blocks
- SD/MJ bridging language

Use them when the user asks for batch generation, prompt variation, or a reusable template.

## How To Use This In AI漫剧 Work

1. Start with `production-architecture.md` to decide which layer is needed.
2. For story/script/storyboard tasks, use `workflow.md` and `prompt-patterns.md`.
3. For image quality or style tasks, search `source-index-v2.md` and `artist-index.txt`.
4. For scene and prop consistency, use `seg-terms.json`.
5. For large prompt-library mining, search the copied source assets rather than loading all references into context.
