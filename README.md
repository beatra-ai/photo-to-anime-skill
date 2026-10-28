# Photo to Anime Skill

English | [简体中文](./README.zh-CN.md) | [日本語](./README.ja.md)

> 👉 See also [AI Headshot Generator Skill](https://github.com/beatra-ai/ai-headshot-generator-skill)

Turn a photo into anime, manga, comic, cartoon, watercolor, clay, or 3D character art while the subject stays recognizable, and reuse the same look across a whole set, from inside Claude Code, Cursor, Codex, Windsurf, Cline, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=photo-to-anime-skill) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn a photo into anime, manga, comic, cartoon, watercolor, clay, or 3D character art while the subject stays recognisable, and repeat the same look across a whole set. |
| **Models** | Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="A photo of a fictional young man with his corgi in a park (the source photo is itself AI-generated) restyled as anime, watercolor, and clay 3D art with his face, hair, clothes, and the dog&#x27;s markings kept recognizable. AI-generated with Beatra."></p>

*A photo of a fictional young man with his corgi in a park (the source photo is itself AI-generated) restyled as anime, watercolor, and clay 3D art with his face, hair, clothes, and the dog's markings kept recognizable. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-photo-restyler`](skills/ai-photo-restyler) | [SKILL.md](skills/ai-photo-restyler/SKILL.md) | 0.2.5 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-photo-restyler). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/photo-to-anime-skill
```

As a Claude Code plugin:

```bash
claude plugin marketplace add beatra-ai/photo-to-anime-skill
claude plugin install ai-photo-restyler@photo-to-anime-skill
```

As a Codex plugin:

```bash
codex plugin marketplace add beatra-ai/photo-to-anime-skill
codex plugin add ai-photo-restyler@photo-to-anime-skill
```

As a GitHub Copilot CLI plugin:

```bash
copilot plugin marketplace add beatra-ai/photo-to-anime-skill
copilot plugin install ai-photo-restyler@photo-to-anime-skill
```

As a Gemini CLI extension:

```bash
gemini extensions install https://github.com/beatra-ai/photo-to-anime-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/photo-to-anime-skill ai-photo-restyler
```

Or clone this repository and copy `skills/ai-photo-restyler` into `~/.claude/skills/` for Claude Code,
`~/.cursor/skills/` for Cursor, `~/.agents/skills/` for Codex, `~/.codeium/windsurf/skills/` for Windsurf,
`~/.cline/skills/` for Cline, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the ai-photo-restyler skill from https://github.com/beatra-ai/photo-to-anime-skill (folder skills/ai-photo-restyler), then follow its SKILL.md to connect my Beatra account.
```

## Technical Specifications & Output Limits

As of 2026-10-18. Live list: https://docs.beatra.ai/en/docs/models

- **Uploads** — up to 100 MB per file; the per-model input limits below also apply
- **Image editing** — 6 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro); PNG; up to 4 images per request; canvas up to 4.2 MP
  - 4.2 MP (2K tier): Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro (up to 4 images per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP
- **Image to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live); PNG; up to 4 images per request; canvas up to 16.8 MP
  - 16.8 MP (4K tier): GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2 (1 image per request)
  - Input images: up to 4 per request, 10–20 MB each; BMP, GIF, JPEG, PNG, TIFF, WEBP

## Why use Beatra instead of calling model APIs directly

- **One account for every model this skill uses** — Image editing 6; Image to image 10 (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live) (as of 2026-10-18), behind one Beatra sign-in; no keys from individual model providers to manage.
- **You decide what gets paid for** — Paid renders run only when you ask for that exact render or approve its card, which shows the live credit estimate.
- **Direction before rendering** — the skill plans, directs, and reviews the work, then renders it on Beatra.
- **Files you can verify** — every file under `skills/` matches the release archive on cdn.beatra.ai byte for byte, checked by SHA-256 before each push.
- **Updates you control** — no self-updater; update with the tool you installed it with.
- **Runs in your agent** — Claude Code, Cursor, Codex, Windsurf, Cline, OpenClaw.

## What you get

- **Still looks like the subject** — Keep the face, hairstyle, clothing, pet markings, or product label recognisable through the restyle.
- **Anchor the exact look you want** — Add your own style reference images so the result follows the palette, line weight, and shading you had in mind.
- **Match a whole set** — Lock in the first result you like, and every other photo in the set comes back in that same style.

## Use cases

- **Avatars and profile pictures** — Turn a selfie or portrait into an anime, cartoon, or comic avatar for social profiles and communities.
- **Sticker and emoji sets** — Draw one character in a shared style across a set of poses and expressions for chat stickers.
- **Pet, couple, and family portraits** — Redraw a favourite photo as illustration art for prints, gifts, and merchandise.

## FAQ

### What kinds of photos work well for an anime or cartoon restyle?

Clear selfies, portraits, pet photos, group shots, product pictures, and travel scenes all work well when the subject is easy to see.

### Can I match a specific art style I already like?

Yes. Add one to three style reference images alongside your photo and say what each should contribute, such as palette, line weight, or shading.

### How do I keep a whole set of photos in the same style?

Pick the result you like best first, then the rest of the photos come back in that same style so the series matches.

## Updates and security

Since the 2026-10 release, this skill contains no self-updater: it runs only the
files you installed and never replaces them on its own. Update it with the tool
you installed it with — `npx skills update ai-photo-restyler` or `gh skill update ai-photo-restyler`.
Details: `references/updates-and-security.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.

## Links

- Website — https://beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=photo-to-anime-skill
- Docs — https://docs.beatra.ai?utm_source=github&utm_medium=flagship&utm_campaign=photo-to-anime-skill
- Console — https://console.beatra.ai
- For AI agents — https://beatra.ai/llms.txt (index) · https://beatra.ai/llms-full.txt (every skill in one file)
