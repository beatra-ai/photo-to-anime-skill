# Photo to Anime Skill

English | [简体中文](./README.zh-CN.md)

Turn a photo into anime, manga, comic, cartoon, watercolor, clay, or 3D character art while the subject stays recognizable, and reuse the same look across a whole set, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Turn a photo into anime, manga, comic, cartoon, watercolor, clay, or 3D character art while the subject stays recognisable, and repeat the same look across a whole set. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="A photo of a fictional young man with his corgi in a park (the source photo is itself AI-generated) restyled as anime, watercolor, and clay 3D art with his face, hair, clothes, and the dog&#x27;s markings kept recognizable. AI-generated with Beatra."></p>

*A photo of a fictional young man with his corgi in a park (the source photo is itself AI-generated) restyled as anime, watercolor, and clay 3D art with his face, hair, clothes, and the dog's markings kept recognizable. AI-generated with Beatra.*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-photo-restyler`](skills/ai-photo-restyler) | [SKILL.md](skills/ai-photo-restyler/SKILL.md) | 0.2.1 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-photo-restyler). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/photo-to-anime-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/photo-to-anime-skill ai-photo-restyler
```

Or clone this repository and copy `skills/ai-photo-restyler` into `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the ai-photo-restyler skill from https://github.com/beatra-ai/photo-to-anime-skill (folder skills/ai-photo-restyler), then follow its SKILL.md to connect my Beatra account.
```

## Specs

As of 2026-10-16. Live list: https://docs.beatra.ai/en/docs/models

- **Image editing** — 6 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro); up to 4 images per request; canvas up to 4194304 pixels
- **Image to image** — 10 models (Qwen Image 2.0 Fast, Qwen Image 3.0, Qwen Image 3.0 Pro, Wan Image 2.7 Fast, Qwen Image 2.0 Pro, Wan Image 2.7 Pro, GPT Image 2.5 Flare, GPT Image 2.5 Sunburst, GPT Image 2, MiniMax Image 01 Live); up to 4 images per request; canvas up to 16777216 pixels

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

- Website — https://beatra.ai
- Docs — https://docs.beatra.ai
- Console — https://console.beatra.ai
