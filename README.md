# 🛩️ Airplane Battle v3.3 — Animal Boss Edition / 飞机大战 v3.3 动物Boss版

<div align="center">

**Classic Vertical Arcade Shooter with Animal-Themed Bosses**
**经典竖版街机射击游戏 · 五章动物主题Boss**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pygame](https://img.shields.io/badge/Pygame-2.0+-green.svg)](https://www.pygame.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-3.3.0-orange.svg)]()

**EN** | [中文](#中文说明)

</div>

---

## 🎮 Gameplay Preview / 游戏画面

![Gameplay Preview](screenshots/gameplay_preview.png)

---

## 🐙 Meet the Bosses / Boss图鉴

![All Bosses](screenshots/all_bosses.png)

| Chapter | Boss | Description |
|---------|------|-------------|
| Ch.1 | **Deep Sea Octopus** ![Boss 1](screenshots/boss_ch1.png) | A massive octopus with 8 suction-cupped tentacles. Fires sweeping fan-shots while its glowing eyes track the player. |
| Ch.2 | **Mecha Tiger** ![Boss 2](screenshots/boss_ch2.png) | A purple mechanical beast with tiger stripes, glowing fangs and armored wings. Attacks with alternating rotating spiral patterns. |
| Ch.3 | **Space Shark** ![Boss 3](screenshots/boss_ch3.png) | A streamlined brown shark with dorsal fin and razor teeth. Launches split-V formations from both flanks, leaving the center safe. |
| Ch.4 | **Armored Rhino** ![Boss 4](screenshots/boss_ch4.png) | A heavily armored green rhino with a massive horn. Fires homing missiles and off-center diagonal spreads. |
| Ch.5 | **Golden Phoenix** ![Boss 5](screenshots/boss_ch5.png) | The final boss — a blazing golden phoenix with spread wings and flame crest. Uses delayed side-barrages and spinning ring patterns. |

---

## 🚀 Ships Gallery / 飞机图鉴

![Ships Gallery](screenshots/ships_gallery.png)

| Ship | Type | Description |
|------|------|-------------|
| **Player Ship** | Player | Sleek swept-wing fighter with glass canopy, wingtip navigation lights, and triple engine thrust. |
| **Small Drone** | Enemy (Tier 1) | Lightweight diamond-shaped drone with glowing energy core. Fast but fragile. |
| **Medium Fighter** | Enemy (Tier 2) | Agile swept-wing fighter with wingtip lights and dual engines. |
| **Large Bomber** | Enemy (Tier 3) | Heavily armored bomber with plate textures, weapon pylons, and quad engines. |

---

## ✨ Features / 核心特色

| Feature | EN | 中文 |
|---------|-----|------|
| **5 Story Chapters** | Each with unique theme colors, enemies, and animal-themed boss | 5章完整章节，每章独立配色、敌机和动物主题Boss |
| **5 Unique Bosses** | Octopus, Tiger, Shark, Rhino, Phoenix — each with distinct bullet patterns | 章鱼、猛虎、鲨鱼、犀牛、凤凰，各具特色弹幕 |
| **Balanced Bullet Hell** | Safe zone below each boss so players can fight back | Boss正下方留安全通道，弹幕可躲避可穿越 |
| **9 Power-Up Types** | Fire rate, extra life, shield, magnet, freeze, etc. | 火力/生命/护盾/磁铁/冰冻等9种道具 |
| **Progressive Difficulty** | Boss HP scales 80→150→250→400→600 across chapters | Boss血量逐章递增，难度渐进 |
| **Top 10 Leaderboard** | JSON-persisted with score, distance, kills, chapter | Top 10排行榜，含分数/距离/击杀/章节 |
| **100% Code-Generated Art** | All graphics drawn with Pygame API — zero external assets | 全部图形由代码绘制，零外部图片依赖 |

---

## 🕹️ Controls / 操作说明

| Key | Action | 功能 |
|-----|--------|------|
| `← → ↑ ↓` / `W A S D` | Move ship | 移动飞机 |
| `Space` (hold) | Fire (auto-repeat) | 发射子弹（长按连发） |
| `B` | Use screen-clearing bomb | 使用全屏炸弹 |
| `P` / `ESC` | Pause / Resume | 暂停/继续 |
| `R` | Restart (game over screen) | 重新开始 |
| `M` | Return to menu | 返回菜单 |
| `L` | View leaderboard | 查看排行榜 |
| Mouse click | Menu navigation | 菜单点击 |

---

## 📖 How to Play / 玩法说明

1. **Start**: Launch the game and select **Story Mode** (剧情模式)
2. **Select Chapter**: Choose any unlocked chapter (Ch.1 available from start)
3. **Survive**: Shoot down waves of enemy drones, fighters, and bombers
4. **Collect Power-Ups**: Destroyed enemies drop power-ups — grab them!
5. **Face the Boss**: After flying ~3000m, the chapter boss appears
6. **Dodge & Attack**: Each boss has a **safe zone directly below** — position yourself there, dodge side patterns, and fire upward
7. **Advance**: Defeat the boss to unlock the next chapter
8. **Beat Ch.5**: Defeat the Golden Phoenix to complete the game!

### 💡 Tips / 小贴士
- Stay **below the boss** — bullet patterns leave a gap in the center for you to fly through
- Use **bombs** wisely — save them for tight situations during boss fights
- Collect **fire rate upgrades** early — they stack and make boss fights much easier
- Watch for **homing missiles** in Ch.4 — dodge them early before they accelerate

---

## 📊 Boss Pattern Details / Boss弹幕设计

```
Chapter 1 — Deep Sea Octopus (HP: 80):
  Phase 0: 5-way fan spread (skipping center) + left/right scatter (skipping center)
  Phase 1: Alternating left/right diagonal sweeps

Chapter 2 — Mecha Tiger (HP: 150):
  Phase 0: 2/3 arm alternating spiral rotation (natural gap in center)
  Phase 1: 12-bullet ring barrage

Chapter 3 — Space Shark (HP: 250):
  Phase 0: Split-V formation (2 shots each side, center empty)
  Phase 1: V formation + 3-way forward shots

Chapter 4 — Armored Rhino (HP: 400):
  Phase 0: Homing missiles (140-frame cooldown) + 4 off-center diagonal shots
  Phase 1: Homing missiles + wide cross-pattern + diagonal sweep

Chapter 5 — Golden Phoenix (HP: 600):
  Phase 0: Delayed side barrages (±0.6 radians from center) + spinning ring
  Phase 1: Rapid ring bursts + spinning pattern overlay
```

---

## ⚡ Quick Start / 快速开始

### Requirements / 环境要求
```
Python 3.8+
Pygame >= 2.0.0
```

### Install & Run / 安装运行
```bash
# Clone the repo
git clone https://github.com/Deeplearning67/airplanebattlev3.3.git
cd airplanebattlev3.3

# Install dependencies
pip install -r requirements.txt

# Run the game
python airplane_battle3.py

# Or on Windows, double-click
run.bat
```

---

## 📁 Project Structure / 项目结构

```
airplanebattlev3.3/
├── airplane_battle3.py      # Main game source (~3000+ lines, single file)
├── README.md                 # Documentation (this file)
├── requirements.txt          # Python dependencies
├── run.bat                   # Windows one-click launcher
├── LICENSE                   # MIT License
├── .gitignore                # Git ignore rules
└── screenshots/              # In-game screenshots & boss gallery
    ├── gameplay_preview.png   # Gameplay screenshot
    ├── all_bosses.png         # All 5 bosses collage
    ├── boss_ch1.png           # Ch.1 Deep Sea Octopus
    ├── boss_ch2.png           # Ch.2 Mecha Tiger
    ├── boss_ch3.png           # Ch.3 Space Shark
    ├── boss_ch4.png           # Ch.4 Armored Rhino
    ├── boss_ch5.png           # Ch.5 Golden Phoenix
    └── ships_gallery.png      # Player + enemy ships
```

---

## 📈 Version History / 版本演进

### v3.3.0 — Safe Zone Edition (Current / 当前版本)

**Changes from v3.2:**
- ✅ Boss bullet patterns now leave a **safe corridor directly below** — no more impassable bullet walls
- ✅ Each chapter's bullet angles explicitly skip the center ±17° zone
- ✅ Tweaked fire intervals for smoother difficulty curve

**Major Changes from v3.0 → v3.3:**

| Feature | v3.0 | v3.3 |
|---------|------|------|
| **Boss Design** | Geometric circles with eyes | 🐙🐯🦈🦏🔥 Full animal-themed art |
| **Player Ship** | Simple polygon | Sleek swept-wing fighter with canopy & engine flames |
| **Enemy Ships** | Basic polygon (3 identical tiers) | 3 distinct designs: Drone / Fighter / Bomber |
| **Bullet Density** | Extremely dense (hundreds/second) | Balanced with fire-rate cooldowns & safe zones |
| **Center Passage** | Blocked by bullets (unbeatable) | ✅ Safe corridor below boss for positioning |
| **Difficulty** | Nearly impossible | Challenging but beatable |
| **Bullet Patterns** | Centered on player (wall of death) | Safe zone below boss for player positioning |

**Technical Improvements:**
- ✅ All graphics redrawn with `pygame.draw` API — animal-themed boss art, detailed player/enemy ships
- ✅ Boss fire-rate limited to 18-22 frame intervals (from per-frame firing)
- ✅ Bullet speed reduced 30-40% across all chapters
- ✅ Safe zone design: each boss's bullet pattern explicitly skips the area directly below (±17°)
- ✅ New `_fire_chapter_pattern()` with per-chapter pattern balancing
- ✅ `_is_safe_zone()` method for bullet angle validation
- ✅ Pre-cached boss/enemy/player surfaces for performance

### v3.0.0 — Chapter Boss Edition
- ✅ 5-chapter system with unique bosses
- ✅ Boss HP scaling: 80→150→250→400→600
- ✅ Chapter progress tracking & unlock system
- ✅ Boss entrance warning animation

### v2.3.0 — Stability Fix
- ✅ Emoji font crash fix
- ✅ Post-death HUD safety
- ✅ PowerUp.apply reference fix
- ✅ Asteroid rotation cache limit

---

## 🛠️ Technical Specs / 技术规格

| Item | Spec |
|------|------|
| Engine | Pygame SDL2 |
| Target FPS | 60 |
| Resolution | 540×780 (Portrait / 竖屏) |
| Code Size | ~3000+ lines (single file) |
| Graphics | 100% procedural (pygame.draw API) |
| Data | JSON leaderboard, JSON chapter progress |
| Dependencies | Python 3.8+, Pygame ≥ 2.0.0 |

---

## 🔒 Security / 安全说明

This game runs **100% locally** with no network communication or data transmission.
Leaderboard and progress data are stored in local JSON files only.

本游戏为纯本地运行程序，无任何网络通信或数据外传行为。
排行榜与进度数据仅存储在本地JSON文件中。

---

<div align="center">

**Author / 作者**: 🦞 AZhua (阿爪)
**Date / 日期**: 2026.04
**License / 许可**: [MIT](LICENSE)

### ⭐ If you enjoy it, please Star! / 如果喜欢，欢迎 Star！⭐

</div>

---

## 中文说明

### 简介
**飞机大战 v3.3** 是基于 Pygame 的经典竖版街机射击游戏的最新版本。本版本最大的亮点是 **5个全新设计的动物主题Boss**：深海章鱼、机甲猛虎、太空鲨鱼、装甲犀牛和黄金凤凰。同时全面重绘了玩家飞机和三级敌机的外观，并对Boss弹幕进行了平衡性调整。v3.3版本进一步优化了弹幕设计，在Boss正下方留出安全通道，彻底解决了弹幕堵路的问题。

### 操作方式
- **WASD / 方向键**：移动飞机
- **空格键**：射击（长按连发）
- **B键**：使用炸弹（全屏清弹）
- **P / ESC键**：暂停
- **R键**：重新开始（游戏结束后）
- **M键**：返回主菜单
- **鼠标**：点击菜单按钮

### 五章Boss
1. **第一章 · 深海章鱼**（HP 80）— 扇形弹幕 + 两侧散射
2. **第二章 · 机甲猛虎**（HP 150）— 旋转螺旋弹幕 + 环形弹幕
3. **第三章 · 太空鲨鱼**（HP 250）— 左右V形弹幕，正下方安全
4. **第四章 · 装甲犀牛**（HP 400）— 追踪弹 + 偏心散射
5. **第五章 · 黄金凤凰**（HP 600）— 侧翼延时弹 + 旋转弹幕

### Boss弹幕安全区
每个Boss的正下方约±17°范围内留有**安全通道**，玩家可以站在Boss正下方躲避弹幕并向上攻击。这是本版本最重要的改进之一。

### v3.3 相比 v3.0 的提升
- **弹幕安全通道**：Boss正下方±17°留有安全缺口，玩家可穿越到Boss下方攻击
- **视觉全面升级**：Boss从简单圆形变为精细的动物造型；玩家飞机从简单多边形变为流线型战斗机；敌机三级各有独特外观
- **难度大幅降低**：弹幕频率从"每帧发射"改为"18-22帧间隔"，子弹速度降低30-40%
- **游戏体验优化**：从"几乎不可能打赢"变为"有挑战但可以通关"

### 运行方法
```bash
pip install pygame
python airplane_battle3.py
```
或直接双击 `run.bat`。
