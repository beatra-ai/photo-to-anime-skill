# Photo to Anime Skill

[English](./README.md) | 简体中文

把照片转成漫画、动漫、卡通、水彩、黏土或 3D 角色画风，保住人物、宠物和商品的辨识度，同一套画风还能批量复用，在 Claude Code、Codex 或 OpenClaw 里直接完成。

> [!IMPORTANT]
> 生成需要 [Beatra](https://beatra.ai) 账号并消耗积分，安装本身不收费。

| 问题 | 回答 |
| --- | --- |
| **能做什么** | 把照片转成漫画风、动漫风、卡通、水彩、黏土或 3D 角色画风，保住人物、宠物和商品的辨识度，同一套画风还能批量复用。 |
| **运行要求** | Python 3.10+，以及能加载 `SKILL.md` 的 Agent |
| **费用** | 安装免费。每次生成消耗 Beatra 账号积分，只有你明确要求这次生成或批准确认卡后才会付费。 |
| **支持的 Agent** | Claude Code、Codex、OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-photo-restyler`](skills/ai-photo-restyler) | [SKILL.md](skills/ai-photo-restyler/SKILL.md) | 0.1.3 |

本仓库由 [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-photo-restyler) 自动发布，问题请到那里反馈。

## 安装

使用 [`skills`](https://skills.sh) CLI：

```bash
npx skills add beatra-ai/photo-to-anime-skill
```

使用 GitHub CLI：

```bash
gh skill install beatra-ai/photo-to-anime-skill ai-photo-restyler
```

也可以克隆本仓库，把 `skills/ai-photo-restyler` 复制到 `~/.claude/skills/`（Claude Code）、`~/.agents/skills/`（Codex）或 `~/.openclaw/skills/`（OpenClaw）。

或者把下面这段话发给你的 Agent：

```text
从 https://github.com/beatra-ai/photo-to-anime-skill 安装 ai-photo-restyler skill（目录 skills/ai-photo-restyler），然后按它的 SKILL.md 连接我的 Beatra 账号。
```

## 你能得到什么

- **画完还是那个人** — 五官、发型、衣着、宠物花纹、商品标识这些辨识点会被保留下来。
- **用参考图锁定画风** — 把你喜欢的画风参考图一起给，配色、线条粗细和上色方式都跟着走。
- **整批画风统一** — 第一张满意之后，后面每张都按同一个画风出，整组看着像一套的。

## 适用场景

- **社交头像与个人主页图** — 自拍或人像转成漫画风、动漫风、卡通头像，用在各类社交账号上。
- **表情包与贴纸套图** — 同一个角色按统一画风画出多个动作和表情，做成整套聊天表情。
- **宠物、情侣与全家福** — 把喜欢的合影重画成插画，用于打印、送礼和周边定制。

## 常见问题

### 什么样的照片适合转成漫画风或动漫风？

主体看得清就行：自拍、人像、宠物照、合影、商品图和旅行照都很合适。

### 能照着我喜欢的某种画风来画吗？

可以。把 1 到 3 张画风参考图和原图一起给，并说明每张负责配色、线条还是上色方式。

### 怎么让一整组照片保持同一个画风？

先挑出你最满意的那一张，后面的照片都按它的画风出，整组就统一了。

## 更新

安装后的 skill 每天最多检查一次新版本，替换前先校验官方归档，任何一步失败都不会动你已安装的版本。
随时可以关闭，见 skill 内的 `references/automatic-updates-and-safety.md`。

## 许可证

[MIT-0](LICENSE)：可自由使用、修改和再分发，包括商用，无需署名；与这些 skill 在 ClawHub 上的条款一致。
