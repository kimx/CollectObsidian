---
title: "cclank/lanshu-animated-architecture-diagram: Premium hand-drawn animated architecture diagram Codex skill"
source: "https://github.com/cclank/lanshu-animated-architecture-diagram"
author:
created: 2026-07-09
description: "Premium hand-drawn animated architecture diagram Codex skill - cclank/lanshu-animated-architecture-diagram"
tags:
  - "clippings"
---
## Lanshu Animated Architecture Diagram

**岚叔动态架构图: premium hand-drawn animated architecture diagrams for articles, systems, and workflows.**

`JSON spec` -> `.excalidraw` + `.png` + animated `.gif`

[Gallery](#gallery) · [Quick Start](#quick-start) · [Features](#features) · [Spec](#spec-structure) · [Verification](#verification)

`lanshu-animated-architecture-diagram` is a Codex skill and local renderer for creating premium black-canvas technical diagrams with hand-drawn typography, editable Excalidraw output, static PNG previews, and genuinely animated GIFs.

It is designed for article explanations, system architecture diagrams, process diagrams, and DailyDoseOfDS-style black-background technical sketches.

## Gallery

The default visual system uses a dark canvas, moving flow highlights, pulsing modules, subtle grain, vignette, and a top-right hand-drawn signature.

| **Claude Loops**    [![Claude Loops animated architecture diagram](https://github.com/cclank/lanshu-animated-architecture-diagram/raw/main/assets/previews/claude-loops.gif)](https://github.com/cclank/lanshu-animated-architecture-diagram/blob/main/assets/previews/claude-loops.gif) | **Memory Pack**    ![Memory Pack animated architecture diagram](https://github.com/cclank/lanshu-animated-architecture-diagram/raw/main/assets/previews/memory-pack.gif)  Memory Pack animated architecture diagram |
| --- | --- |

## Features

- Generates `.excalidraw`, `.png`, and animated `.gif` from one JSON spec
- Produces real animation with moving glow points and pulsing module highlights
- Keeps the `.excalidraw` source editable and text-based
- Uses local Python rendering through Pillow
- Does not require Excalidraw, browser automation, ImageMagick, remote APIs, or external icon libraries
- Includes frame-diff verification to prove GIF motion
- Uses a fixed high-quality layout for clean technical storytelling

## Outputs

Each render produces:

```
<basename>.excalidraw
<basename>.png
<basename>.gif
```

The default canvas is:

```
1210 x 1138
20 fps
41 frames
2.05 seconds
```

## Quick Start

```
git clone https://github.com/cclank/lanshu-animated-architecture-diagram.git
cd lanshu-animated-architecture-diagram
python3 -m pip install -r requirements.txt
python3 scripts/render_animated_diagram.py \
  --spec assets/default-spec.json \
  --outdir outputs \
  --basename sample \
  --verify
```

## Installation

Place this folder in your Codex skills directory:

```
~/.codex/skills/lanshu-animated-architecture-diagram
```

Typical local install path:

```
${CODEX_HOME:-$HOME/.codex}/skills/lanshu-animated-architecture-diagram
```

Install the runtime dependency:

```
python3 -m pip install -r requirements.txt
```

## Use With Codex

Invoke the skill by name:

```
Use $lanshu-animated-architecture-diagram to turn this article into a premium hand-drawn animated architecture GIF.
```

Chinese prompt example:

```
用 $lanshu-animated-architecture-diagram 把这篇文章整理成岚叔动态架构图，输出 GIF、PNG 和 Excalidraw。
```

## CLI Usage

Start from the bundled template:

```
cp assets/default-spec.json work/my-diagram-spec.json
```

Render:

```
python3 scripts/render_animated_diagram.py \
  --spec work/my-diagram-spec.json \
  --outdir outputs \
  --basename my-diagram \
  --verify \
  --check
```

The `--verify` flag prints sampled frame differences. Nonzero changed pixels confirm that the GIF is genuinely animated.

The `--check` flag validates the generated PNG, GIF, and Excalidraw output contract and exits nonzero if a required property fails. It checks dimensions, GIF frame count and frame duration, sampled GIF motion, unique Excalidraw IDs, text font family, and that no external files are embedded.

## Spec Structure

The renderer uses `assets/default-spec.json` as a compact art-directed template.

Most edits happen in these fields:

```
signature
title.prefix
title.highlight
title.subtitle
inputs
core.cards
decision
output
left_panel
center_panel
right_panel
```

Supported icon keys:

```
folder
file
scan
shield
db
hash
package
```

For details, see [references/spec-format.md](https://github.com/cclank/lanshu-animated-architecture-diagram/blob/main/references/spec-format.md).

## Verification

Validate the skill structure:

```
python3 ${CODEX_HOME:-$HOME/.codex}/skills/.system/skill-creator/scripts/quick_validate.py \
  ${CODEX_HOME:-$HOME/.codex}/skills/lanshu-animated-architecture-diagram
```

Validate GIF media parameters:

```
ffprobe -v error -select_streams v:0 -count_frames \
  -show_entries stream=width,height,r_frame_rate,avg_frame_rate,nb_read_frames \
  -show_entries format=duration \
  -of default=noprint_wrappers=1 outputs/my-diagram.gif
```

Validate animation:

```
python3 scripts/render_animated_diagram.py \
  --spec assets/default-spec.json \
  --outdir outputs \
  --basename sample \
  --verify \
  --check
```

## Dependencies

Required:

- Python 3.9+
- Pillow 10.0.0+

Install Python packages with:

```
python3 -m pip install -r requirements.txt
```

Optional:

- `ffprobe` for media inspection
- Excalidraw web app or editor plugin for manual editing of generated `.excalidraw` files

## Project Layout

```
lanshu-animated-architecture-diagram/
├── SKILL.md
├── README.md
├── LICENSE
├── requirements.txt
├── agents/
│   └── openai.yaml
├── assets/
│   ├── default-spec.json
│   └── previews/
│       ├── claude-loops.gif
│       └── memory-pack.gif
├── references/
│   └── spec-format.md
└── scripts/
    └── render_animated_diagram.py
```

## Design Notes

This project intentionally keeps the visual system narrow:

- Dark canvas
- Hand-drawn title treatment
- Top input strip
- Middle core pipeline
- Bottom source, layer, and pack panels
- Top-right signature
- Clean static diagram with motion added only in GIF overlays