# 游乐园奖品射击摊 / Prize Shooting

一个单文件 HTML5 Canvas 射击小游戏：在游乐园奖品摊里射击移动玩偶、积累分数和彩票、进入国王的小店购买武器，并解锁隐藏的小祥超市与国王对话档案。

A single-file HTML5 Canvas shooting gallery game: shoot moving carnival prizes, earn score and tickets, buy weapons from the King's shop, and unlock the hidden Xiaoxiang Market plus the King's dialogue archive.

---

## 中文说明

### 项目特点

- **单文件运行**：游戏主体、样式、脚本、国王图像与 Web Audio 音效都写在一个 HTML 文件中，不需要构建工具。
- **Canvas 街机玩法**：移动奖品在三条传送带上穿梭，玩家点击或拖拽射击，追求高分和更高连击。
- **移动端适配**：手机端会提示横屏游玩，并尝试进入全屏与锁定横屏。
- **商店与成长**：用彩票购买基础气枪、连发气枪、弧弹枪、皇家权杖、火星枪，以及幸运挂件、稳定挂件和狂热沙漏。
- **狂热模式**：积累分数后触发狂热，生成更密集，武器性能强化，国王可能混入奖品。
- **隐藏内容**：买空商店后可触发小祥超市，抽取国王的秘密纸条；成就界面收录玩偶、国王对话、游戏成就和私密小对话。
- **本地存档**：最高分、彩票、债务、已购商品、当前武器和已解锁秘密通过 `localStorage` 保存在浏览器本地。

### 快速开始

把游戏 HTML 文件放进仓库根目录，并建议改名为：

```text
index.html
```

然后直接用浏览器打开，或者启动一个本地静态服务器：

```bash
python -m http.server 8000
```

访问：

```text
http://localhost:8000
```

### 推荐仓库结构

```text
.
├── index.html
├── README.md
└── GAME_GUIDE.md
```

### GitHub Pages 发布

1. 把 `index.html`、`README.md`、`GAME_GUIDE.md` 提交到 GitHub 仓库。
2. 打开仓库的 **Settings → Pages**。
3. Source 选择 **Deploy from a branch**。
4. Branch 选择 `main`，目录选择 `/root`。
5. 保存后等待 GitHub Pages 构建完成。

### 基本操作

| 操作 | 说明 |
|---|---|
| 鼠标左键 / 触屏点击 | 射击、点击按钮、购买商品 |
| 长按鼠标 | 连发气枪、火星枪等武器会自动攻击 |
| 弧弹枪普通模式 | 按下并拖出一条足够长的线，松开后扇形射击 |
| 空格 | 标题界面开始；结算后进入商店；商店内开始下一局；对话中加速 |
| `M` | 开关音乐 / 音效 |
| 右键 | 国王对话中加速 / 跳过 |
| 成就界面拖动 | 滚动档案内容 |

### 开发备注

- 游戏不依赖 npm、Vite、Webpack 或外部图片资源。
- 当前版本主要面向现代浏览器，推荐 Chrome、Edge、Safari 或 Firefox 的较新版本。
- 如果手机浏览器仍显示顶部地址栏，可以把页面“添加到主屏幕”后再打开。
- 本仓库未默认声明开源许可证；如果公开发布，请按你的需求补充 `LICENSE`。

---

## English

### Features

- **Single-file runtime**: the game, styles, scripts, King sprites, and Web Audio sounds are embedded in one HTML file. No build step is required.
- **Canvas arcade gameplay**: prizes move across three conveyor lanes. Click, hold, or drag depending on the equipped weapon.
- **Mobile-friendly layout**: the game prompts landscape play on mobile and attempts fullscreen / landscape lock.
- **Shop progression**: spend tickets on the Basic Air Gun, Rapid Air Gun, Arc Gun, Royal Scepter, Mars Gun, Lucky Charm, Stable Charm, and Fever Hourglass.
- **Fever mode**: score accumulation triggers a powered-up phase with denser spawns, enhanced weapons, and a disguised King prize.
- **Hidden content**: after buying out the shop, players can unlock the Xiaoxiang Market, draw secret notes, and reveal private King dialogue.
- **Local save data**: best score, tickets, debt, owned items, equipped weapon, and revealed secrets are saved with browser `localStorage`.

### Quick Start

Place the game HTML file in the repository root and preferably rename it to:

```text
index.html
```

Open it directly in a browser, or run a local static server:

```bash
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

### Recommended Repository Structure

```text
.
├── index.html
├── README.md
└── GAME_GUIDE.md
```

### Deploying with GitHub Pages

1. Commit `index.html`, `README.md`, and `GAME_GUIDE.md` to the GitHub repository.
2. Open **Settings → Pages**.
3. Set Source to **Deploy from a branch**.
4. Select the `main` branch and `/root` folder.
5. Save and wait for GitHub Pages to finish deploying.

### Controls

| Input | Action |
|---|---|
| Left click / tap | Shoot, select buttons, buy shop items |
| Hold click | Auto-fire with compatible weapons |
| Arc Gun in normal mode | Press, drag a long enough chord, then release to fire a fan burst |
| Space | Start from title, enter shop after a run, start next run from shop, accelerate dialogue |
| `M` | Toggle music / audio |
| Right click | Accelerate or skip King dialogue |
| Drag in archive screen | Scroll archive content |

### Notes for Developers

- No npm, Vite, Webpack, or external image assets are required.
- The current build targets modern browsers. Recent Chrome, Edge, Safari, or Firefox versions are recommended.
- On mobile, adding the page to the home screen may give a more app-like fullscreen experience.
- No license is declared by default. Add a `LICENSE` file before public distribution if needed.
