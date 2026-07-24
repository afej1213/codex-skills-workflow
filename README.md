# Codex Skills Workflow

A small collection of reusable Codex skills for Malaysia-localized social copy,
editable presentation planning, and short-video inspiration research.

这是一组可直接安装到 Codex 的公开 skills，适合内容创作、Google Slides
演示规划与马来西亚短视频灵感研究。

## Included Skills

| Skill | Purpose |
|---|---|
| `ai-caption-title-writer` | 为马来西亚市场生成和改写 TikTok、小红书、Instagram 与 Facebook 标题、Caption、CTA 及 Hashtag。 |
| `content-to-editable-slides` | 把用户提供的内容拆解成结构清楚、可继续编辑的 16:9 Google Slides 演示规划。 |
| `viral-short-video-radar` | 筛选四个马来西亚本地热门短视频，并整理成可执行的创意参考简报。 |

## Install All Skills

Run the Codex skill installer:

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo afej1213/codex-skills-workflow \
  --path skills/ai-caption-title-writer \
         skills/content-to-editable-slides \
         skills/viral-short-video-radar
```

The skills will be installed under `~/.codex/skills/` and become available to
Codex on the next turn.

## Install One Skill

Replace the path with the skill you want:

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo afej1213/codex-skills-workflow \
  --path skills/ai-caption-title-writer
```

Available paths:

```text
skills/ai-caption-title-writer
skills/content-to-editable-slides
skills/viral-short-video-radar
```

## Download ZIP

1. Open this repository on GitHub.
2. Select **Code → Download ZIP**.
3. Extract the archive.
4. Copy the required folders from `skills/` into `~/.codex/skills/`.
5. Start a new Codex turn so the installed skills can be discovered.

Copy the complete skill folder, including its `SKILL.md`, `agents/`,
`references/`, `scripts/`, or `assets/` directories when present.

## Example Requests

### Caption writing

```text
请把这段产品资料改写成适合马来西亚 TikTok 和小红书的 Caption，
并提供标题、CTA 和 Hashtag。
```

### Editable slides

```text
请把这份内容整理成一套可编辑的 16:9 Google Slides 演示结构。
```

### Short-video radar

```text
帮我寻找四个适合马来西亚设计工作室参考的热门短视频方向。
```

## Repository Structure

```text
codex-skills-workflow/
├── README.md
├── LICENSE
└── skills/
    ├── ai-caption-title-writer/
    ├── content-to-editable-slides/
    └── viral-short-video-radar/
```

Each directory under `skills/` is a self-contained Codex skill.

## Validation

Every included skill has been checked with Codex's `quick_validate.py`
validator before publication.

## License

The three skills included in this repository are released under the
[MIT License](LICENSE).

Third-party skills and materials not included in this repository are not
covered by this license.
