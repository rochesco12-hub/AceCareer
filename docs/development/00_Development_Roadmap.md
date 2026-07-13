# Ace Career Development Bible
# 00 · Development Roadmap

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Development Roadmap 是整个 Ace Career 项目的最高层文档。

它不定义任何具体系统。

它定义：

整个项目应该如何被开发。

所有模块。

所有数据库。

所有 Engine。

所有 UI。

都必须遵循本 Roadmap。

如果未来产生冲突。

以本文件为最高优先级。

---

# Vision

Ace Career 的目标不是制作一款网球游戏。

而是创造一个能够持续运行几十个赛季的职业网球世界。

玩家不是游戏的中心。

玩家只是世界中的一名职业球员。

整个项目所有设计，都必须围绕：

> Living Tennis World（活着的职业网球世界）

展开。

---

# Product Philosophy

Ace Career 不属于以下类型：

- Sports Arcade
- Tennis Simulator
- Story Game
- RPG

Ace Career 属于：

Career Simulation（职业生涯模拟）

玩家真正体验的是：

成为职业网球运动员。

而不是打一场网球。

---

# Core Design Principles

整个项目必须始终遵循以下原则。

### Principle 1 — World First

世界优先。

世界先存在。

玩家后进入。

所有系统必须保证：

即使没有玩家。

世界依然能够正常运行。

---

### Principle 2 — Simulation First

模拟优先。

不要脚本。

不要事件触发。

不要固定剧情。

所有事件都应该来自：

World Simulation。

---

### Principle 3 — Career First

职业优先。

比赛只是职业的一部分。

恢复。

训练。

旅行。

教练。

媒体。

新闻。

都属于 Career。

---

### Principle 4 — Choice Matters

所有选择必须拥有代价。

例如：

参加 Masters。

意味着：

恢复减少。

奖金增加。

Fatigue增加。

没有最佳答案。

---

### Principle 5 — No Grinding

Ace Career 不允许：

刷经验。

刷金币。

刷副本。

所有成长来自：

职业生涯。

---

# Project Layers

整个项目分为八层。

```text
Presentation Layer
↓
Product Layer
↓
Gameplay Layer
↓
Simulation Layer
↓
Engine Layer
↓
Database Layer
↓
Persistence Layer
↓
Cloud Layer
```

每层职责独立。

禁止跨层直接访问。

---

# Layer Responsibilities

### Presentation

负责：

UI

Animation

Haptic

Charts

Widgets

不允许：

业务逻辑。

---

### Product

负责：

页面流程。

导航。

信息架构。

交互。

不负责：

数据计算。

---

### Gameplay

负责：

训练。

比赛。

恢复。

旅行。

Career Loop。

这里只定义：

玩家怎么玩。

---

### Simulation

负责：

世界模拟。

AI。

新闻。

排名。

赛程。

整个世界运行。

---

### Engine

负责：

数学。

概率。

规则。

积分。

成长。

Fatigue。

所有算法。

---

### Database

负责：

所有数据模型。

Schema。

索引。

关系。

版本升级。

---

### Persistence

负责：

SwiftData。

CloudKit。

缓存。

离线。

存档。

---

### Cloud

负责：

同步。

排行榜。

分享。

社区。

未来 Online。

---

# Documentation Structure

整个文档永久保持如下结构。

```text
01 Engine Bible
02 Gameplay Bible
03 Development Bible
04 Product Design
05 Design System
06 Balance Sheets
07 Prompt System
08 API
09 Assets
10 Release Notes
```

任何新增文档。

必须进入对应目录。

禁止：

Documentation/

Misc/

Temp/

Unknown。

---

# Development Order

整个项目开发顺序固定。

### Phase 1 — Engine（已完成）

### Phase 2 — Gameplay（已完成）

### Phase 3 — Development（当前）

Database / Architecture / Simulation / Match Engine / Balance

### Phase 4 — Product

页面设计：Today / Career / Tournament / Ranking

### Phase 5 — UI

视觉设计 / 动画 / Apple Design

### Phase 6 — Implementation

SwiftUI / Engine / CloudKit / AI — 开始编码

### Phase 7 — Internal Alpha

功能验证 / 平衡 / 性能 / Bug

### Phase 8 — Public Beta

邀请玩家 / 收集反馈 / 调整体验

### Phase 9 — Release

正式上线。

---

# Technical Principles

### Offline First

任何功能默认支持离线。

联网只是增强，不是依赖。

### Config Driven

所有数字禁止写死。

全部配置化：成长 / Fatigue / 奖金 / 赛事。

### Data Driven

所有内容来自数据库。不是 View / SwiftUI / 硬编码。

### Deterministic Simulation

同样输入永远得到同样结果。

方便 Debug / Replay / Cloud Sync。

---

# AI Principles

AI 与玩家使用同一套规则。

AI 不会作弊。

不会无限恢复、无限成长、无限金钱。

整个世界绝对公平。

---

# Code Principles

Single Responsibility。

每个模块只负责一件事。

禁止 God Object。

---

# Folder Structure

```text
AceCareer
App/
Presentation/
Features/
Engine/
Simulation/
Models/
Database/
Persistence/
Networking/
Resources/
Config/
Assets/
Tests/
```

---

# Quality Standards

所有代码必须满足：

✓ 可测试 ✓ 可重构 ✓ 可扩展 ✓ 配置化

✓ 无循环依赖 ✓ 无重复逻辑 ✓ 无 View Business Logic

---

# Performance Goals

世界模拟（2200 球员/周）：<100ms

Career 存档：<1MB

Today 首屏：<300ms

App 冷启动：<2s

---

# Breaking Change Policy

修改 PlayerID / TournamentID / Ranking Engine / Save Format

都属于 Breaking Change。

必须：升级版本 / 迁移数据 / 更新文档。

---

# Documentation Rules

新增任何系统。

必须同时更新：Engine / Development / Product / Database 四套文档。

---

# Definition of Done

✓ 明确项目开发顺序

✓ 明确模块职责

✓ 明确架构分层

✓ 明确代码规范

✓ 明确文档规范

✓ 明确未来扩展方式

✓ 所有开发者遵循同一标准

---

# Final Principle

Ace Career 不是一次性项目。

它应该是一套能够持续迭代十年以上的职业网球模拟平台。

所有设计。所有代码。所有文档。

都必须为这个目标服务。

---

End of Document
