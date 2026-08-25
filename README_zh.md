<p align="center">
  <a href="README.md">English</a> · <strong>中文</strong>
</p>

<h1 align="center">小布鲁 🐾 · Codex 宠物</h1>

<p align="center">
  <strong>一只耳朵很大、权限很小的代码监工</strong><br>
  Codex 忙时他跑，看到你时他挥爪，工资只收关注和摸摸。
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Codex-Pet%20v2-111827?style=flat-square" alt="Codex Pet v2">
  <img src="https://img.shields.io/badge/%E5%9B%BE%E9%9B%86-1536%C3%972288-2F8F83?style=flat-square" alt="1536 × 2288 图集">
  <img src="https://img.shields.io/badge/%E5%8A%A8%E4%BD%9C-9%20%E7%A7%8D%E7%8A%B6%E6%80%81-E76F51?style=flat-square" alt="9 种动作状态">
  <img src="https://img.shields.io/badge/%E7%8E%AF%E8%A7%86-16%20%E4%B8%AA%E6%96%B9%E5%90%91-F4A261?style=flat-square" alt="16 个环视方向">
  <img src="https://img.shields.io/badge/%E5%BC%80%E6%BA%90%E8%AE%B8%E5%8F%AF-MIT-7C3AED?style=flat-square" alt="MIT 开源许可证">
</p>

<p align="center">
  <a href="#认识小布鲁">认识小布鲁</a> ·
  <a href="#猫猫上班实录">猫猫上班实录</a> ·
  <a href="#给爱看数字的人">技术参数</a> ·
  <a href="#把小布鲁领回家">领养指南</a> ·
  <a href="#猫包里有什么">仓库内容</a> ·
  <a href="#mit猫不爱填表">MIT</a>
</p>

<a id="认识小布鲁"></a>
## 认识小布鲁 🐈

小布鲁的英文名是 **BLUE**，原型就是我家的蓝色阿比西尼亚猫。他有大耳朵、琥珀色眼睛、青绿金黄串珠项圈，以及一种“这个 bug 反正不是我写的”的从容。

他的工作内容包括：

- Codex 工作时跑来跑去，营造大家都很忙的气氛；
- 心情好时挥爪，心情更好时继续挥爪；
- 任务失败时陪你一起蔫掉；
- 从 16 个方向盯住鼠标，防止它偷偷逃跑；
- 提供情绪价值，但不对构建结果负责。

所有动作只使用原始绘制帧，不插值、不拉伸、不把猫变成面条。胡须、爪子和猫格都还在原位。

<a id="猫猫上班实录"></a>
## 猫猫上班实录 🎬

### 一整抽屉的小布鲁

<p align="center">
  <img src="previews/contact-sheet.png?v=d2552a6" width="900" alt="小布鲁无损平滑版 Codex 宠物全部动作总览">
</p>

### 看起来很忙的员工

| 待机 | 打招呼 | 执行任务 | 等待输入 |
| --- | --- | --- | --- |
| ![小布鲁待机动画](previews/idle.gif?v=d2552a6) | ![小布鲁招手动画](previews/waving.gif?v=d2552a6) | ![小布鲁执行任务动画](previews/running.gif?v=d2552a6) | ![小布鲁等待输入动画](previews/waiting.gif?v=d2552a6) |

### 全方位监控鼠标

<p align="center">
  <img src="previews/look-directions.png?v=d2552a6" width="900" alt="小布鲁中立姿势和 16 个顺时针环视方向">
</p>

他还会向左冲、向右冲、起跳、失败后自闭，以及一本正经地审查代码。证据都在 [`previews`](previews/) 里。

<a id="给爱看数字的人"></a>
## 给爱看数字的人 🔧

| 项目 | 数值 |
| --- | --- |
| 精灵图规范 | Codex Pet v2 |
| 图集文件 | `spritesheet.webp` |
| 图集尺寸 | 1536 × 2288 px |
| 网格 | 8 列 × 11 行 |
| 单帧尺寸 | 192 × 208 px |
| 标准状态 | 9 种 |
| 动作节奏 | 无损相邻帧平滑回环 |
| 环视方向 | 16 个，以 22.5° 为步长顺时针排列 |
| 透明格式 | RGBA WebP |
| 清单文件 | `pet.json`，包含 `spriteVersionNumber: 2` |
| 验证结果 | 0 个错误、0 个警告 |

有个猫门尺寸问题：这个仓库只适用于 Codex 桌面端/CLI v2。ChatGPT 网页版宠物入口采用另一种 1536 × 1872 排版，需要另行转换精灵图；这张 `spritesheet.webp` 不能原样硬塞进去。

<a id="把小布鲁领回家"></a>
## 把小布鲁领回家 🏠

### 1. 把猫包带回家

```bash
git clone https://github.com/rudykon/codex-pet-blue.git
cd codex-pet-blue
```

### 2. 给小布鲁腾个窝

#### Windows PowerShell

```powershell
$petDir = "$env:USERPROFILE\.codex\pets\xiaobulu"
New-Item -ItemType Directory -Force -Path $petDir | Out-Null
Copy-Item .\pet.json, .\spritesheet.webp -Destination $petDir
```

#### macOS / Linux

```bash
mkdir -p ~/.codex/pets/xiaobulu
cp pet.json spritesheet.webp ~/.codex/pets/xiaobulu/
```

### 3. 开门放猫

文件夹保持叫 `xiaobulu`，Codex 里显示的 **小布鲁** 则来自 `pet.json`。刷新或重启 Codex，他就会自动出现在宠物选择器里。Codex CLI 输入 `/pets`，可以点名查看本地猫口。

<a id="猫包里有什么"></a>
## 猫包里有什么 📦

| 路径 | 用途 |
| --- | --- |
| [`pet.json`](pet.json) | 宠物 ID、显示名称、简介、精灵图版本和图集路径 |
| [`spritesheet.webp`](spritesheet.webp) | 完整透明 v2 动画图集 |
| [`previews/contact-sheet.png`](previews/contact-sheet.png) | 全部动画行的视觉总览 |
| [`previews/look-directions.png`](previews/look-directions.png) | 中立姿势和 16 方向注视循环 |
| [`previews/`](previews/) | 各状态的动画 GIF 预览 |
| [`validation.json`](validation.json) | 机器可读的图集验证结果 |
| [`LICENSE`](LICENSE) | 适用于整个仓库的 MIT 许可证条款 |

<a id="mit猫不爱填表"></a>
## MIT，猫不爱填表 📜

小布鲁的美术、动画、预览、配置和文档都采用 [MIT 许可证](LICENSE)。你可以把他领走、修改、分发、教新动作，或者放进自己的项目里，包括商业项目。记得保留版权声明和许可证文本就好。

Codex、ChatGPT 和 OpenAI 是 OpenAI 的商标。小布鲁是社区猫，不是 OpenAI 员工，请不要拿 API 账单找他报销。
