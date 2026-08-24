# 小布鲁 · Codex Pet

一只好奇、聪明又黏人的暖棕色阿比西尼亚猫，戴着青绿金黄串珠项圈和圆形「布鲁」名牌。

![小布鲁动作总览](previews/contact-sheet.png)

## 兼容性

- Codex Pet v2
- 图集：`1536 × 2288` WebP（8 列 × 11 行）
- 单帧：`192 × 208`
- 包含 9 种标准状态和 16 个环视方向

## 安装

下载本仓库后，将 `pet.json` 和 `spritesheet.webp` 放进同一个宠物目录。

Windows：

```powershell
$petDir = "$env:USERPROFILE\.codex\pets\xiaobulu"
New-Item -ItemType Directory -Force -Path $petDir | Out-Null
Copy-Item .\pet.json, .\spritesheet.webp -Destination $petDir
```

macOS / Linux：

```bash
mkdir -p ~/.codex/pets/xiaobulu
cp pet.json spritesheet.webp ~/.codex/pets/xiaobulu/
```

安装完成后重启或刷新 Codex，在宠物选择器里选择「小布鲁」。Codex CLI 中可使用 `/pets` 查看和切换本地宠物。

## 动作预览

| 待机 | 打招呼 | 执行任务 | 等待输入 |
|---|---|---|---|
| ![待机](previews/idle.gif) | ![打招呼](previews/waving.gif) | ![执行任务](previews/running.gif) | ![等待输入](previews/waiting.gif) |

完整动作 GIF、左右移动和 16 个环视方向见 [`previews`](previews/) 目录。

## 文件

- `pet.json`：Codex 宠物清单
- `spritesheet.webp`：v2 动画图集
- `previews/`：动作和方向预览
- `validation.json`：图集结构验证结果

## 使用说明

本仓库提供个人使用和 Codex 宠物安装展示。小布鲁角色形象及美术素材保留所有权利；未经作者明确许可，请勿用于商业销售、再授权、训练数据集或冒充原创发布。

---

## English

Xiao Bulu is a curious and affectionate Abyssinian cat made as a Codex Pet v2. Download the repository, copy `pet.json` and `spritesheet.webp` into `~/.codex/pets/xiaobulu/`, then refresh Codex and select “小布鲁”. Character artwork is shared for personal Codex use; all other rights are reserved.
